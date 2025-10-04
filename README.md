# 📚 Assistant de Relecture IA - Relecture_du_Livre

Un assistant intelligent pour la relecture et la correction de contenu, directement intégré avec **Notion** et **Claude AI**.

## 🚀 Installation Rapide

### Option 1: Installation Locale

```bash
# 1. Télécharger le code source
git clone https://github.com/Hypnose-Patrick/Relecture_du_Livre.git
cd Relecture_du_Livre

# 2. Installer les dépendances
npm install

# 3. Configurer vos clés API
cp .env.example .env
# Éditez .env avec vos vraies clés

# 4. Lancer l'application
npm run dev
```

## 🔑 Configuration des Clés API

### Notion API
1. Allez sur [https://www.notion.so/my-integrations](https://www.notion.so/my-integrations)
2. Créez une nouvelle intégration
3. Copiez le token (commence par `secret_`)
4. Partagez votre base "Centre de documents Livre" avec cette intégration

### Claude API
1. Créez un compte sur [https://console.anthropic.com/](https://console.anthropic.com/)
2. Ajoutez des crédits (minimum 5$)
3. Générez une clé API (commence par `sk-ant-`)

## 🖥️ Option 2: Application Desktop (Electron)

```bash
# Créer une application desktop
npm run electron:build

# L'installateur sera généré dans dist-electron/
```

## 🌐 Option 3: Déploiement Web

### Vercel (Gratuit)
```bash
npm i -g vercel
vercel
# Configurez les variables d'environnement dans le dashboard
```

### Netlify
```bash
npm run build
# Glissez-déposez le dossier dist/ sur netlify.com
```

## 🌐 Intégration dans votre Site Web

### Iframe Simple
```html
<iframe 
  src="https://votre-app.vercel.app" 
  width="100%" 
  height="800px"
  frameborder="0">
</iframe>
```

### Widget Popup
```html
<button onclick="openRelectureApp()">Assistant de Relecture</button>

<div id="relecture-modal" style="display:none;">
  <iframe src="https://votre-app.vercel.app"></iframe>
</div>
```

## 📁 Fichiers Fournis

### 📋 Guides Complets
- `INSTALLATION_GUIDE.md` - Guide d'installation pas à pas
- `DEPLOYMENT_GUIDE.md` - Guide de déploiement détaillé
- `.env.production` - Template de configuration production

### 🔧 Scripts Automatisés
- `deploy.sh` - Script de déploiement automatique
- `electron/main.js` - Configuration application desktop
- Scripts npm personnalisés dans `package.json`

### ⚙️ Configuration
```bash
# Scripts disponibles
npm run deploy:local      # Test local
npm run deploy:staging    # Déploiement test
npm run deploy:production # Déploiement production
npm run electron:build   # Application desktop
```

## 🛡️ Sécurité et Bonnes Pratiques

### ✅ Sécurité Intégrée
- Variables d'environnement pour les clés API
- Aucune clé exposée dans le code client
- Communication HTTPS uniquement
- Validation des entrées utilisateur

### 📊 Fonctionnalités de Production
- Mode démo automatique si clés manquantes
- Gestion d'erreurs robuste
- Logs de débogage
- Interface responsive
- Support multi-navigateurs

## 🎯 Prochaines Étapes

1. Testez avec vos données en configurant vos clés API
2. Choisissez votre méthode de déploiement (local, web, ou desktop)
3. Intégrez dans votre workflow existant
4. Formez votre équipe à utiliser l'assistant

## 📞 Support

- 📖 Documentation complète dans les fichiers MD
- 🔧 Configuration détaillée dans `.env.example`
- 🚀 Scripts prêts à l'emploi pour tous les déploiements

Votre assistant de relecture IA est maintenant prêt à optimiser vos contenus avec vos vraies données ! 🚀📚✨

## 🏗️ Architecture Technique

- **Frontend**: Vue.js 3 avec Composition API
- **Desktop**: Electron
- **APIs**: Notion API + Claude AI (Anthropic)
- **Déploiement**: Vercel/Netlify compatible
- **Sécurité**: Variables d'environnement, validation stricte

## 📄 Licence

MIT License - Voir le fichier [LICENSE](LICENSE) pour plus de détails.
