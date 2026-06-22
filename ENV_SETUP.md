# Configuration des Variables d'Environnement Sécurisées

## Configuration de la Clé API Gemini

### 1. Créer le fichier `.env.local`

```bash
cp .env.local.example .env.local
```

### 2. Ajouter votre clé API Gemini

Ouvrez le fichier `.env.local` et remplacez :

```
NEXT_PUBLIC_GEMINI_API_KEY=votre_clé_api_gemini_ici
```

### 3. Sécurité

⚠️ **Important** : Ne jamais commiter le fichier `.env.local`

- Le fichier `.env.local` est automatiquement ignoré par Git (voir `.gitignore`)
- Votre clé API reste privée et ne sera pas publiée sur GitHub

### 4. En Développement

Pour lancer le serveur de développement avec les variables d'environnement :

```bash
yarn dev
```

Les variables du fichier `.env.local` seront automatiquement chargées.

### 5. En Production

- Configurez les variables d'environnement directement dans votre plateforme de déploiement (Vercel, Docker, etc.)
- Ne jamais exposer `.env.local` en production

## Variables Disponibles

| Variable | Description | Exemple |
|----------|-------------|---------|
| `NEXT_PUBLIC_GEMINI_API_KEY` | Clé API Google Gemini | `AIz...` |

---

**Note** : Les variables commençant par `NEXT_PUBLIC_` sont visibles côté client. Utilisez des variables sans ce préfixe pour les secrets sensibles côté serveur.
