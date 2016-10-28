#To Start a new Ember app
When cloning the project

```
npm install
npm bower install
npm ember-cli
```

If I don't have any bower install

```
npm install -g bower
npm install -g ember-cli
```

```
Start project

$ ember new project-name

- $ ember --help (commandname)
```

- Once we have a new project in place, we can confirm everything is working by launching the Ember development serve:

```
$ ember server
or
$ ember s

Then We can navigate to localhost:4200

*************** SET UP ROUTE ********************
1. CREATE ABOUT ROUTE & load _about_ route handler.
$ ember g route [name-of-route]
  1) ember g route about
  - then can enter about the website description
  - ember s & open localhost:4200/about

  2) ember g route contact

  3) add at bottom of each .hbs page{{#link-to 'contact'}}Click here to contact us.{{/link-to}}

  4) ember g route index

  5) update the index & add both previously created links at bottom of the page

  6) _app/routes/index.js_ add hard-coded & model hook
  ** can add debugger; anywhere in index.js once ember Inspector is installed

  7) _app/templates/index.hbs_ add {{each}}

  8) $ember g model rental  (to generat ember data model)

  9) Install: $ ember install emberfire (for Ember to communicate to Firebase)

  10) sign in to firebase account https://console.firebase.google.com/

  11) on firebase.com create new project using the same project-name

  12) get apikey from firebase's project

  13) Create a temporary seed file called projects.json

  14) update index.js w/model

  15) run ember g component rental-tile

  16) run ember g component new-rental

  17) run ember g update-rental

  18) run ember g route rental (to add view more detail to each rental need to create new route b/c this will not show on the index)

  19) run ember g component rental-detail

  20) run ember install ember-bootstrap

  21) run ember g template application

  22) run ember g model review

  23) update rentals.json w/ reviews database

  24) import rentals.json to Firebase

  25) run ember g component new-review

  26) add review to rental model

  27) run ember g component review-tile



```

### Ember auto create support structures: The Ember CLI Directory Structure
- The new command generates a project structure with the following files and directories:

```
|--app
|--bower-components
|--config
|--dist
|--node_modules
|--public
|--tests
|--tmp
|--vendor

bower.json
ember-cli-build.js
package.json
README.md
testem.json
```

### version 2.6 or later of ember-cli. These versions no longer include an application.hbs file automatically when you create a new project. We'll build one manually. Otherwise Before we build these first three pages we'll need to remove the contents of the app/templates/application.hbs file (if it exists), leaving only the {{outlet}} line of code.