# REPAAC — Réponse Appel À Candidature
**LAMS Consulting | Conseil en Achats & Supply Chain**

Application web de génération automatique d'offres commerciales, techniques et emails pour les appels à candidature.

---

## 🚀 Déploiement GitHub Pages

### Étape 1 — Créer le dépôt
1. Créez un nouveau dépôt GitHub (ex: `repaac`)
2. Uploadez tous les fichiers de ce dossier dans la branche `main`

### Étape 2 — Activer GitHub Pages
1. Allez dans **Settings** → **Pages**
2. Source : **GitHub Actions**
3. Le workflow `.github/workflows/pages.yml` se déclenchera automatiquement

### Étape 3 — Configurer le domaine personnalisé (CNAME)
1. Dans **Settings** → **Pages** → **Custom domain**, entrez : `repaac.lams-consulting.com`
2. Modifiez le fichier `CNAME` avec votre domaine
3. Chez votre registrar DNS, ajoutez un enregistrement CNAME :
   ```
   repaac.lams-consulting.com  →  votre-compte.github.io
   ```
4. Cochez **Enforce HTTPS**

### Étape 4 — Configurer la clé API Anthropic
1. Ouvrez l'application déployée
2. Connectez-vous avec `admin` / `Admin2024!`
3. Cliquez sur **🔑** dans la barre de navigation
4. Entrez votre clé API Anthropic (obtenue sur [console.anthropic.com](https://console.anthropic.com))
5. **Changez le mot de passe admin** immédiatement

---

## 👤 Comptes par défaut

| Compte | Login | Mot de passe |
|--------|-------|--------------|
| Admin  | `admin` | `Admin2024!` |

⚠️ **Changez le mot de passe admin dès la première connexion !**

---

## 📁 Structure du projet

```
repaac/
├── index.html              # Application complète (single-page app)
├── CNAME                   # Domaine personnalisé GitHub Pages
├── .github/
│   └── workflows/
│       └── pages.yml       # Déploiement automatique
└── README.md
```

---

## 🔧 Fonctionnalités

- ✅ **Authentification multi-utilisateurs** (admin + utilisateurs)
- ✅ **Panel Admin** : créer, modifier, supprimer des comptes
- ✅ **Formulaire complet** : tous les champs LAMS (TDR, TJM, interlocuteurs…)
- ✅ **Génération IA** : Offre Commerciale + Offre Technique + Email (via Claude API)
- ✅ **Export PDF** (impression) et **Word** (.doc téléchargeable)
- ✅ **Envoi email** : Gmail, Outlook, IONOS
- ✅ **Historique** des missions (20 dernières, par utilisateur)
- ✅ **Pièces jointes** : CV, diplômes, attestations (liste de rappel)
- ✅ **Données isolées** par utilisateur (localStorage)

---

## 🔑 Clé API Anthropic

L'application utilise l'API Claude d'Anthropic pour générer les documents.

- Créez un compte sur [console.anthropic.com](https://console.anthropic.com)
- Générez une clé API dans **API Keys**
- Entrez-la dans l'application via le bouton **🔑**
- La clé est stockée localement dans le navigateur (jamais envoyée à un tiers)

---

## 📧 Contact
LAMS Consulting | contact@lams-consulting.com | www.lams-consulting.com  
Tél : +224 627 948 649 / +33 6 99 09 59 74
