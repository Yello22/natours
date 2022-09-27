# natours
###To install node_modules dependencies
```# npm install``` 
###Migrate data to mongoDB (you must have mongoDB installed on your system)
- Stape 1:
```# npm run ./dev-data/data/import-dev-data.js --delete```
- Stape 2:
``# npm run ./dev-data/data/import-dev-data.js --import```

### API:
-URL: http://127.0.0.1:8000/
***
###Tours
```
-GET: {{URL}}api/v1/touts/ :returns all visits (you need to authenticate first)
-GET: {{URL}}api/v1/touts/:id :return a visit
-GET: {{URL}}api/v1/touts/top-5-cheap :returns the 5 cheapest visits
-GET: {{URL}}api/v1/touts/tour-stats :returns a statistics of visits
-GET: {{URL}}api/v1/touts//monthly-plan/:year :returns the visits of each month in a one year
-POST:{{URL}}api/v1/touts/ :create a tour
-DEL: {{URL}}api/v1/touts/ :delete a tour
```

###Users
```
-POST: {{URL}}api/v1/users/signup :create an account and log in
--example JSON body for account creation:
{
    "name": "admin",
    "email": "admin@gmail.com",
    "password": "pass12345",
    "passwordConfirm": "pass12345",
    "role": "admin"
}

-POST: {{URL}}api/v1/users/login :sign in to an existing account
--example JSON body for login:
{
    "email": "admin@gmail.com",
    "password": "pass12345"
}

-POST: {{URL}}api/v1/users/forgotPassword :password forgotten
--example JSON body for a forgotten password:
{
    "email": "jonasuser@gmail.com"
}

-PATCH: {{URL}}api/v1/users/resetPassword :change mdp
```
###Launch the project in development mode
```# npm start``` 
###Launch in production mode
```# npm start:prod```
