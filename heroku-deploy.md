# Heroku deploy

## Git setup

* `touch .gitignore`
*  Add `node_modules/` to the `.gitignore`


* `git init`
* `git add .`
* `git commit -m "initial commit"`
* `git branch -M main`


## Heroku setup

* `heroku create`
  * check if heroku repo is linked to your repo : `git remote -v`   
* `heroku apps:rename put-your-app-name-here`
* `git push heroku main`


Ensure you have start scipt in `package.json` under scripts:

`"start" : "node index.js`

## Database setup

Create a PostgreSQL database on Heroku for you app using this command: 

```
heroku addons:create heroku-postgresql:hobby-dev
```

See more info about the created database using: `heroku pg:info`

To connect to the PostgreSQL database on Heroku by runnning: 

```heroku pg:psql``` 

## Deploy and debug your app

To deploy your app run this command: 

```
git push heroku main
```

Open the deployed app in a browser running this command : 

```
heroku open
```

To see the log files to look for deployment issue use: 

```
heroku logs --tail
```





