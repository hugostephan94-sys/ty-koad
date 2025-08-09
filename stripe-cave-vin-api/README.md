# stripe-cave-vin-api

API minimaliste pour créer un lien Stripe Checkout en fonction des réponses Google Forms.

## Déploiement rapide (Vercel)
1. Importer ce dossier dans un nouveau projet Vercel.
2. Ajouter la variable d'environnement **STRIPE_SECRET_KEY** (clé secrète).
3. (Optionnel) SUCCESS_URL et CANCEL_URL.
4. Déployer. L'endpoint sera : `https://<projet>.vercel.app/api/generate-stripe-link`

## Corps de requête attendu (POST JSON)
```json
{
  "email": "client@example.com",
  "produits": [
    {"id": "price_XXXXXXXX", "qty": 2},
    {"id": "price_YYYYYYYY", "qty": 1}
  ],
  "metadata": {"order_source": "google_forms"}
}
```
