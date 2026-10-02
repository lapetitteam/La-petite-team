# La Petite Team — version refaite

Version Cloudflare Pages + D1.

## Fonctionnalités
- Boutique et panier
- Commandes
- Page client privée avec lien personnel
- Suivi des commandes et messages client
- Réponses des créateurs
- Espace créateurs protégé par mot de passe
- Ajout/modification/suppression des produits et photos
- Ajout/suppression des membres et photos

## Sécurité
Les données créateurs (commandes, messages, gestion) ne sont jamais renvoyées par l'API sans authentification créateur. Le lien client donne uniquement accès aux données du client concerné.

Mot de passe temporaire si `ADMIN_PASSWORD` n'est pas défini : `Lateam181025`

## Déploiement
1. Créer une base D1 nommée `la-petite-team-db`.
2. Remplacer `A_REMPLACER_APRES_CREATION_D1` dans `wrangler.toml` par l'ID de la base.
3. Ajouter `ADMIN_PASSWORD` dans les variables/secrets Cloudflare.
4. Déployer avec `npx wrangler pages deploy .`.
