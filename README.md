# 📋 AAC — Agent Architecte Collaborateur · Journal d'Audit

> **Journal quotidien des audits de code** générés automatiquement par l'Agent Architecte Collaborateur (AAC).  
> Chaque jour, **l'ensemble des 18 dépôts** est analysé par une IA locale (Ollama), et les recommandations sont tracées ici.

---

## 🎯 Pourquoi ce journal existe

### Le problème
Quand on gère **15-20 dépôts GitHub** en parallèle (perso, pro, clients), on perd vite la vue d'ensemble :
- Des issues restent ouvertes 3 mois sans réponse
- Des PRs stagnent sur des branches oubliées
- Les bonnes pratiques (tests, documentation) s'effritent projet par projet

### La solution
Un **audit quotidien automatisé** par IA, tracé dans un journal public :

| Avant (manuel) | Après (AAC) |
|---|---|
| ❌ 30 min/jour à checker chaque repo | ✅ 0 min — l'IA le fait |
| ❌ On oublie la moitié des projets | ✅ Les 18 dépôts sont scannés |
| ❌ Pas d'historique des progrès | ✅ Chaque jour = une entrée datée |
| ❌ Critiques = corvée | ✅ Ton « Staff Engineer » constructif |

---

## 🧠 Méthodologie : les 4 phases

L'AAC suit un protocole strict à chaque session :

| Phase | Nom | Ce qui est analysé |
|---|---|---|
| **A** | Issue Audit | Vision stratégique — fonctionnalités manquantes, opportunités |
| **B** | Code Review | Architecture, sécurité, performance, conventions |
| **C** | PR Assessment | Maturité du code — prêt à merger ou pas |
| **D** | Synthèse | Top 3 des projets + prochaine étape concrète |

---

## 📊 Projets audités quotidiennement

| Projet | Langage | Type | Dernier audit |
|---|---|---|---|
| [GitHub-Auditor](https://github.com/Ruaudel-Emmanuel/GitHub-Auditor) | n8n/Ollama | Automation IA | ✅ 2026-10-05 |
| [rennesdev-vps-ops](https://github.com/Ruaudel-Emmanuel/rennesdev-vps-ops) | Shell/Docker | DevOps | ✅ 2026-10-05 |
| [Audio-Transcriber](https://github.com/Ruaudel-Emmanuel/Audio-Transcriber) | Python | IA locale | ✅ 2026-10-05 |
| [SPECTRE](https://github.com/Ruaudel-Emmanuel/SPECTRE) | JavaScript | Analyse web | ✅ 2026-10-05 |
| [Lecteur-PDF](https://github.com/Ruaudel-Emmanuel/Lecteur-PDF) | JS/Capacitor | Android | ✅ 2026-10-05 |
| [construction-site-tracker](https://github.com/Ruaudel-Emmanuel/construction-site-tracker) | HTML/JS | App métier | ✅ 2026-10-05 |
| [Fiscale-vps](https://github.com/Ruaudel-Emmanuel/Fiscale-vps) | Python | Facturation | ✅ 2026-10-05 |
| [surveillance-tarifaire](https://github.com/Ruaudel-Emmanuel/surveillance-tarifaire) | Python | Veille | ✅ 2026-10-05 |

---

## 📂 Structure du dépôt

```
aac-audit-journal/
├── README.md              ← Ce fichier
├── rapports/              ← Audits quotidiens (YYYY-MM-DD-*.md)
├── issues/                ← Issues suggérées, classées par projet
└── actions/               ← Suivi des actions exécutées (PRs mergées, bugs corrigés)
```

---

## 🏆 Impact mesuré

- **15+ audits** générés depuis le lancement
- **8 projets actifs** suivis quotidiennement
- **Dizaines de suggestions** d'amélioration appliquées (CI, docs, refacto)
- **0 régression** introduite par les suggestions (vérifié en rétrospective)

---

## 🔧 Technique

- **Déclencheur** : workflow GitHub Actions + n8n (cron quotidien 06h00)
- **Modèle IA** : Ollama local (qwen2.5:3b) — **zéro donnée vers le cloud**
- **Livraison** : commit automatique sur `main` + notification Telegram
- **Stockage** : PostgreSQL (`rapports_audit` table) pour historique structuré

---

## 👤 À propos

Généré par l'**Agent Architecte Collaborateur** — un workflow n8n créé par [Emmanuel Ruaudel](https://github.com/Ruaudel-Emmanuel).  
Ce journal est la **preuve en temps réel** d'un audit de code automatisé, privé et quotidien.
