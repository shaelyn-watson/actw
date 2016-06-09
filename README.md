# Act-W Website

### Setup
**Note:** This project assumes you've installed [Node](https://nodejs.org/en/) v5.9.1 and [Postgres](http://www.postgresql.org/).

1. Run `npm install -g gulp` to install [Gulp](http://gulpjs.com/) globally
2. Run `npm install` to get all of the project dependencies listed in `package.json`
 
### Postgres Database setup:
  1. Create the Postgres database `CREATE DATABASE actw_development;`
  2. Connect to the Postgres server ` \c actw_development`
  3. User tables are created automatically
  4. Finally create `app/config.json` file in the actw/app directory. You'll need to contact a collaborator for the config details.

### To run hot reloading dev environment
```bash
$ gulp
```

### Environment
If everything is working properly, you should see Gulp spinning up Nodemon (which then triggers app.js) and BrowserSync. It will open up a new browser tab and start watching (and actively updating you on) any changes made to any files, and injecting those changes right into the browser without having to refresh. When you first run `gulp`, you'll see some "Access URLs" listed. Local is what you'll need most of the time, UI is the URL for looking at BrowserSync options, and their respective External URLs are for any outside devices you are testing.

### Troubleshooting
- Every once and awhile, dependencies don't install or update properly. The recommended solution is to delete the project's `node_modules` folder and run `npm install`

