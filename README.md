# natours
**Pour installer les dépendances node_modules
# npm install 
**Migrer les données vers mongoDB (vous devez avoir mongoDB installé sur votre système)
- Etape1:
# npm run ./dev-data/data/import-dev-data.js --delete
- Etape 2:
# npm run ./dev-data/data/import-dev-data.js --import

## API:
-URL: http://127.0.0.1:8000/
**Tours
-GET: {{URL}}api/v1/touts/ :retourne tout les visites ( vous devez vous authentifier pour d'abord )
-GET: {{URL}}api/v1/touts/:id :retourne une visite
-GET: {{URL}}api/v1/touts/top-5-cheap : retourne les 5 visites les moins chers
-GET: {{URL}}api/v1/touts/tour-stats :retourne un statistique des visites
-GET: {{URL}}api/v1/touts//monthly-plan/:year :retourne les visites de chaque mois dans une année
-POST: {{URL}}api/v1/touts/ :creer une visite
-DEL: {{URL}}api/v1/touts/ :supprimer une visite

**Users
-POST: {{URL}}api/v1/users/signup :créer une compte et se connecter
--exemple de corps JSON pour la création de compte:
{
    "name": "admin",
    "email": "admin@gmail.com",
    "password": "pass12345",
    "passwordConfirm": "pass12345",
    "role": "admin"
}
-POST: {{URL}}api/v1/users/login :se connecter à un compte existant
--exemple de corps JSON pour la connexion:
{
    "email": "admin@gmail.com",
    "password": "pass12345"
}
-POST: {{URL}}api/v1/users/forgotPassword :mdp oublié
--exemple de corps JSON pour un mdp oublié:
{
    "email": "jonasuser@gmail.com"
}
-PATCH: {{URL}}api/v1/users/resetPassword :change mdp
