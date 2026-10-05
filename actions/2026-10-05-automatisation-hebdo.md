# Automatisation hebdomadaire AAC — 2026-10-05

## Objectif
Automatiser les actions de maintenance AAC **chaque lundi à 05h00** (heure de Paris).

## Ce qui est automatisé

| Action | Description |
|---|---|
| **Export workflow** | Extraction JSON du workflow « GitHub Auditor » depuis PostgreSQL n8n → push dans `GitHub-Auditor/workflow/` |
| **Nettoyage PRs** | Fermeture des PRs deps obsolètes (>14j non mergeables), merge automatique des PRs propres (CI clean) |
| **Journal AAC** | Génération d'un rapport hebdo + push vers `aac-audit-journal/rapports/` |
| **Notification** | Résumé envoyé sur Telegram @Vosmanubot |

## Architecture

```
aac-weekly-maintenance.timer (lundi 05h00)
  └── aac-weekly-maintenance.service
        └── aac-weekly-maintenance.sh
              ├── 1. PAT ← n8n DB (Config node)
              ├── 2. Export workflow JSON ← psql
              ├── 3. Push → GitHub (webhook n8n)
              ├── 4. PR cleanup ← GitHub API
              ├── 5. Journal update
              └── 6. Telegram recap
```

## Fichiers

| Fichier | Rôle |
|---|---|
| `scripts/aac-weekly-maintenance.sh` | Script de maintenance (mode oneshot) |
| `systemd/aac-weekly-maintenance.service` | Service systemd |
| `systemd/aac-weekly-maintenance.timer` | Timer → lundi 05h00 Europe/Paris |

## État

- ✅ Timer installé et activé
- ✅ Prochain déclenchement : **lundi 2026-10-12 ~05:01** (UTC+2)
- ✅ Test PAT extraction OK
- ✅ Test API GitHub OK (login: Ruaudel-Emmanuel)