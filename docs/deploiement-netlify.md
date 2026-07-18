# Déploiement Netlify

## Site

- URL : https://nailsconnection-z.netlify.app
- Build : `npm run build` (via `netlify.toml`)
- Plugin : `@netlify/plugin-nextjs`

## Stockage des réservations

En production, les données salon / RDV sont dans **Netlify Blobs**.

Variables nécessaires (valeurs **uniquement** dans Netlify → Environment variables) :

| Variable | Rôle |
|----------|------|
| `NETLIFY_SITE_ID` | Project ID Netlify |
| `NETLIFY_BLOBS_TOKEN` | Personal access token Netlify (accès Blobs) |
| `ADMIN_PASSWORD` | Mot de passe espace admin |

Sans Blobs correctement configuré, l’enregistrement des réservations échoue.

## Repo Git lié

Le déploiement CI peut être branché sur le dépôt code public ou privé — vérifier l’accès GitHub dans Netlify si le dépôt est privé.
