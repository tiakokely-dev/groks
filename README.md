# Chat Groq avec deep-chat - Version Améliorée

Une interface de chat moderne et complète utilisant **deep-chat** avec l'API Groq.

## ✨ Nouvelles Fonctionnalités

### 🎨 Interface Moderne
- **Design responsive** qui s'adapte à tous les écrans
- **Mode sombre/clair** avec persistance des préférences
- **Animations fluides** et transitions élégantes
- **Barre de statut** en temps réel avec indicateur de connexion

### ⚙️ Configuration Simplifiée
- **Formulaire de configuration intégré** (plus besoin de modifier le code)
- **Sélection de modèle** avec limites affichées (RPM, TPM)
- **Stockage local** de la clé API et des préférences
- **Changement de modèle à la volée** sans rechargement

### 🛠️ Fonctionnalités Avancées
- **Bouton d'effacement** de conversation avec confirmation
- **Export de conversation** (en cours d'amélioration)
- **Raccourcis clavier** :
  - `Ctrl+S` : Sauvegarder la configuration
  - `Ctrl+E` : Exporter la conversation
- **Indicateur visuel** de statut de connexion

### 📱 Support Multi-Modèles
11 modèles IA disponibles organisés par catégorie :
- **Llama** (Meta) : 3.1 8B, 3.3 70B, Llama 4 Scout
- **GPT-oss** (OpenAI) : 20B, 120B
- **Qwen** : Qwen3 32B
- **Whisper** : Transcription audio (Large v3, Turbo)
- **Autres** : Allam 2, Groq Compound

## 🚀 Installation Ultra-Rapide

Aucune installation nécessaire ! Le projet utilise un CDN pour charger `deep-chat`.

### Démarrage en 3 étapes :

1. **Ouvrez** le fichier `index.html` dans votre navigateur
2. **Entrez** votre clé API Groq dans le champ dédié
3. **Cliquez** sur "Sauvegarder" et commencez à chatter !

## 🔑 Comment obtenir votre clé API Groq

1. Rendez-vous sur [console.groq.com](https://console.groq.com/)
2. Créez un compte ou connectez-vous
3. Allez dans la section **API Keys**
4. Cliquez sur **"Create API Key"**
5. Copiez votre clé et collez-la dans l'interface

> 🔒 **Sécurité** : Votre clé est stockée localement dans le navigateur (localStorage) et n'est jamais envoyée à nos serveurs.

## 🆓 Modèles Gratuits et Leurs Limites

| Modèle | RPM | TPM | TPD | Usage Recommandé |
|--------|-----|-----|-----|------------------|
| llama-3.1-8b-instant | 30 | 6K | 500K | Réponses rapides |
| llama-3.3-70b-versatile | 30 | 12K | 100K | Tâches complexes |
| meta-llama/llama-4-scout | 30 | 30K | 500K | Raisonnement avancé |
| openai/gpt-oss-20b | 30 | 8K | 200K | Usage général |
| openai/gpt-oss-120b | 30 | 8K | 200K | Tâches intensives |
| qwen/qwen3-32b | 60 | 6K | 500K | Multilingue |
| whisper-large-v3 | 20 | - | - | Transcription audio |
| whisper-large-v3-turbo | 20 | - | - | Transcription rapide |
| allam-2-7b | 30 | 6K | 500K | Arabe/anglais |
| groq/compound | 30 | 70K | - | Workflows complexes |
| groq/compound-mini | 30 | 70K | - | Workflows légers |

### Légende :
- **RPM** : Requêtes par minute
- **TPM** : Tokens par minute  
- **TPD** : Tokens par jour

> ⚠️ Les limites s'appliquent au niveau de l'organisation. Une erreur 429 indique que vous avez atteint une limite.

## 🎯 Utilisation

### Configuration Initiale
1. Cliquez sur le bouton **⚙️ Config** pour afficher le panneau
2. Collez votre clé API Groq
3. Sélectionnez le modèle de votre choix
4. Cliquez sur **💾 Sauvegarder**

### Changer de Modèle
- Utilisez le menu déroulant pour sélectionner un autre modèle
- La configuration est automatiquement appliquée
- Les limites du modèle s'affichent en dessous

### Mode Sombre
- Cliquez sur **🌙 Thème** pour basculer entre mode clair et sombre
- Votre préférence est sauvegardée automatiquement

### Effacer la Conversation
- Cliquez sur **🗑️ Effacer**
- Confirmez la suppression
- L'historique est entièrement effacé

## 🏗️ Architecture Technique

### Technologies Utilisées
- **HTML5** : Structure sémantique
- **CSS3** : Variables CSS, Flexbox, animations
- **JavaScript Vanilla** : Aucun framework requis
- **deep-chat** : Bibliothèque de chat via CDN
- **localStorage** : Persistance des données utilisateur

### Avantages de Cette Approche
- ✅ **Zéro dépendance** : Pas de npm, yarn ou build system
- ✅ **Portable** : Un seul fichier HTML suffit
- ✅ **Rapide** : Chargement instantané
- ✅ **Maintenable** : Code propre et documenté
- ✅ **Extensible** : Facile à personnaliser

## 🎨 Personnalisation

### Modifier les Couleurs
Éditez les variables CSS dans la section `:root` :

```css
:root {
    --accent-color: #6366f1;      /* Couleur principale */
    --bg-primary: #ffffff;         /* Fond principal */
    --chat-height: 600px;          /* Hauteur du chat */
}
```

### Ajouter de Nouveaux Modèles
Ajoutez des options dans le `<select id="modelSelect">` :

```html
<option value="nouveau-modele">Nom du Modèle</option>
```

Puis mettez à jour `modelLimitsData` dans le JavaScript.

## ⚠️ Notes de Sécurité

**Important pour la production :**

1. **Ne commitez jamais** votre clé API dans un dépôt Git public
2. Pour un usage professionnel, utilisez un **backend proxy** pour masquer votre clé
3. Cette application est conçue pour un **usage personnel/local**

### Bonnes Pratiques
- ✅ Utiliser en localhost ou environnement sécurisé
- ✅ Effacer le localStorage après utilisation sur ordinateur partagé
- ✅ Régénérer régulièrement votre clé API
- ❌ Ne pas déployer sur un serveur public sans protection

## 📚 Ressources Utiles

- [Documentation Groq](https://console.groq.com/docs)
- [deep-chat Documentation](https://deepchat.dev/)
- [Gestion des limites Groq](https://console.groq.com/docs/rate-limits)
- [Playground Groq](https://console.groq.com/playground)

## 🤝 Contribution

Suggestions d'améliorations futures :
- [ ] Export complet des conversations (JSON, TXT, PDF)
- [ ] Historique des conversations précédentes
- [ ] Support du markdown enrichi
- [ ] Upload de fichiers pour analyse
- [ ] Personnalisation avancée (couleurs, polices)
- [ ] Mode hors ligne avec cache

## 📄 Licence

Ce projet est fourni à titre éducatif. Utilisez-le responsibly !

---

**Développé avec ❤️ pour démontrer la puissance de Groq + deep-chat**
