# Act-W Website

### Setup
**Note:** This project assumes you've installed [Node](https://nodejs.org/en/) (`brew install node`) and [Postgres](http://www.postgresql.org/) via your method of choice. Instructions on how to install with Homebrew can be viewed [here](https://www.learnhowtoprogram.com/lessons/installing-postgres).

1. Run `npm install -g gulp` to install [Gulp](http://gulpjs.com/) globally
2. Run `npm install` to get all of the project dependencies listed in `package.json`
3. Finally create `app/config.json` file in the actw/app directory and replace the username of the postgres connection string with your postgres username settings. You'll need to contact a collaborator for the config details.
 
### Database setup:
  1. Run `psql` to access the Postgres server. This is where you will set up your dev database and tables.
  2. Run `CREATE DATABASE actw_development;` to create the database;
  3. Run `\c actw_development` to connect to the database;
  4. Create Blog table
  5. Add placeholder data for blogs `insert into "Blogs" ("username", "title", "blogContent", "createdAt", "updatedAt") values ('shaelyn', 'Actw is the best', 'Actw is the best because it just is.', '2016-03-15', '2016-03-15');`


### To run

```bash
$ gulp
```

### Environment
If everything is working properly, you should see Gulp spinning up Nodemon (which then triggers app.js) and BrowserSync. It will open up a new browser tab and start watching (and actively updating you on) any changes made to any files, and injecting those changes right into the browser without having to refresh. When you first run `gulp`, you'll see some "Access URLs" listed. Local is what you'll need most of the time, UI is the URL for looking at BrowserSync options, and their respective External URLs are for any outside devices you are testing.

### Troubleshooting
- Every once and awhile, dependencies don't install or update properly. The recommended solution is to delete the project's `node_modules` folder and run `npm install`

