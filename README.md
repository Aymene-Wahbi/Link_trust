# LinkTrust 🛡️ — URL Trust & Security Intelligence

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![Languages](https://img.shields.io/badge/languages-FR%20%7C%20EN%20%7C%20ES%20%7C%20DE%20%7C%20AR-orange.svg)

> **LinkTrust** est une application web d'analyse prédictive de la fiabilité des URLs. Elle protège les utilisateurs contre le phishing, l'usurpation de marque et le typosquatting avant le moindre clic.

---

## 🎯 Pourquoi ce projet ?

Aujourd'hui, **plus de 80% des sites d'hameçonnage (phishing) utilisent un certificat HTTPS valide** (source: APWG). 

La croyance populaire selon laquelle un « cadenas dans la barre d'adresse » garantit la sécurité d'un site est obsolète et dangereuse :
* **HTTPS = Canal chiffré.** (Empêche l'écoute clandestine sur le réseau).
* **HTTPS ≠ Légitimité.** (N'assure pas que le destinataire n'est pas un pirate).

LinkTrust apporte un score de confiance global en combinant plusieurs vérifications heuristiques et structurelles.

---

## ✨ Fonctionnalités Principales

- 🎯 **Score de Confiance sur 100** : Jauge visuelle instantanée (Vert = Sûr, Jaune = Attention, Rouge = Danger).
- 🔍 **Moteur d'Analyse Heuristique** :
  - **Détection du Typosquatting** : Repérage des imitations de marques (ex: `paypa1.com`, `g00gle.com`).
  - **Analyse du Protocole** : Vérification HTTP / HTTPS.
  - **Détection des Raccourcisseurs** : Identification des URLs masquées (`bit.ly`, `tinyurl`).
- 🌐 **Support Multilingue (5 Langues)** : Français 🇫🇷, Anglais 🇬🇧, Espagnol 🇪🇸, Allemand 🇩🇪, Arabe 🇸🇦 (avec support **RTL** automatique).
- 🌓 **Thèmes Sombre & Clair** : Style *Ultra Deep* pour la nuit, et style *SaaS Minimalist* très épuré pour le jour.
- 🎓 **Section Pédagogique** : Explication claire et visuelle de la différence entre Chiffrement et Légitimité.

---

## 🚀 Installation Rapide (GitHub Pages / Local)

Aucune dépendance complexe ou compilation n'est requise. L'application est développée en architecture **Single File Web Application**.

### Déploiement Local
1. Clonez ce dépôt GitHub :
   ```bash
   git clone https://github.com/votre-compte/linktrust.git
   ```
2. Ouvrez le fichier `index.html` directement dans votre navigateur web préféré.

### Déploiement Cloud (Vercel / Netlify / GitHub Pages)
Vous pouvez directement lier votre dépôt GitHub à **GitHub Pages** ou **Vercel** :
1. Sur GitHub, allez dans **Settings > Pages**.
2. Sélectionnez la branche `main` et enregistrez.

---

## 🛠️ Architecture pour Production (Backend)

Pour faire évoluer ce prototype client vers une plateforme SaaS d'entreprise, il est recommandé de connecter le frontend aux APIs backend suivantes :

| API | Rôle dans LinkTrust |
| :--- | :--- |
| **Google Safe Browsing** | Vérification contre les listes noires globales de Google. |
| **VirusTotal API v3** | Analyse multi-scanners (plus de 70 moteurs antimalware). |
| **Whois API** | Contrôle de la date de création du domaine (< 30 jours = très suspect). |
| **urlscan.io** | Capture d'écran sécurisée et analyse du code JS de la page cible. |

---
