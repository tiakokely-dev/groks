# Chat Groq avec deep-chat

Un exemple simple d'intégration de chat utilisant **deep-chat** avec l'API Groq.

## 🚀 Installation Ultra-Rapide grâce au CDN

Aucune installation complexe nécessaire ! Ce projet utilise un **CDN (Content Delivery Network)** pour charger la bibliothèque `deep-chat` directement dans le navigateur.

### Avantages du CDN :
- **Zéro configuration** : Pas besoin de npm, yarn, ou tout autre gestionnaire de paquets
- **Démarrage instantané** : Ouvrez simplement le fichier `index.html` dans votre navigateur
- **Pas de build** : Aucun processus de compilation ou bundling requis
- **Toujours à jour** : Le CDN charge automatiquement la dernière version stable
- **Léger** : Seul le code nécessaire est chargé à la demande

```html
<!-- Une seule ligne suffit -->
<script type="module" src="https://unpkg.com/deep-chat-dev@latest/dist/deepChat.bundle.js"></script>
```

## 🔑 Comment obtenir votre clé API Groq

1. Rendez-vous sur [console.groq.com](https://console.groq.com/)
2. Créez un compte ou connectez-vous
3. Allez dans la section **API Keys** dans votre tableau de bord
4. Cliquez sur **"Create API Key"**
5. Copiez votre clé API et gardez-la secrète !

## 📝 Configuration

1. Ouvrez le fichier `index.html`
2. Remplacez `"your api key mistral"` par votre véritable clé API Groq :

```javascript
directConnection='{
    "groq": {
        "key": "gsk_votre_cle_api_ici",
        "model": "openai/gpt-oss-20b"
    }
}'
```

3. Enregistrez le fichier
4. Ouvrez `index.html` dans votre navigateur web

## 🆓 Modèles Gratuits Disponibles sur Groq

Voici les modèles disponibles avec le plan gratuit et leurs limites :

| Modèle | RPM | RPD | TPM | TPD |
|--------|-----|-----|-----|-----|
| llama-3.1-8b-instant | 30 | 14.4K | 6K | 500K |
| llama-3.3-70b-versatile | 30 | 1K | 12K | 100K |
| meta-llama/llama-4-scout-17b-16e-instruct | 30 | 1K | 30K | 500K |
| openai/gpt-oss-20b | 30 | 1K | 8K | 200K |
| openai/gpt-oss-120b | 30 | 1K | 8K | 200K |
| qwen/qwen3-32b | 60 | 1K | 6K | 500K |
| whisper-large-v3 | 20 | 2K | - | - |
| whisper-large-v3-turbo | 20 | 2K | - | - |
| allam-2-7b | 30 | 7K | 6K | 500K |
| groq/compound | 30 | 250 | 70K | - |
| groq/compound-mini | 30 | 250 | 70K | - |

### Légende des limites :
- **RPM** : Requêtes par minute
- **RPD** : Requêtes par jour
- **TPM** : Tokens par minute
- **TPD** : Tokens par jour

> ⚠️ Les limites s'appliquent au niveau de l'organisation. Si vous atteignez l'une des limites (RPM ou TPM), vous recevrez une erreur 429.

## 🎯 Utilisation

Une fois configuré, vous pouvez :
- Poser des questions aux modèles IA
- Changer de modèle en modifiant la propriété `model` dans `index.html`
- Profiter d'une interface de chat moderne et réactive

## 📚 Ressources

- [Documentation Groq](https://console.groq.com/docs)
- [deep-chat Documentation](https://deepchat.dev/)
- [Gestion des limites de taux Groq](https://console.groq.com/docs/rate-limits)

## ⚠️ Note de Sécurité

**Important** : Ne commitez jamais votre clé API dans un dépôt public. Pour un usage en production, utilisez un serveur backend pour proxyfier les requêtes vers l'API Groq.
