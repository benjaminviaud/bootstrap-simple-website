# Starter theme for website
This is a starter theme based on Zurb Foundation. Tools used : gulp, webpack, ES6, BrowserSync, minified CSS and JS, images optimization, yaml config...

## Easy to start
### 1. Clone the repository and install with npm/yarn
```
$ git clone https://github.com/benjaminviaud/bootstrap-simple-website.git
$ cd bootstrap-simple-website
$ npm or yarn install
```
### 4. Configuration
#### YAML config file
This starter theme includes a config-default.yml file. To make changes to the configuration, make a copy of config-default.yml and name it config.yml and make changes to that file. The config.yml file is ignored by git so that each environment can use a different configuration with the same git repo.

At the start of the build process a check is done to see if a config.yml file exists. If config.yml exists, the configuration will be loaded from config.yml. If config.yml does not exist, config-default.yml will be used as a fallback.

#### Browsersync setup
If you want to take advantage of Browsersync (automatic browser refresh when a file is saved), simply open your config.yml file after creating it in the previous step, and put your local dev-server address and port (e.g http://localhost:8888) in the url property under the BROWSERSYNC object.

#### Static asset hashing / cache breaker
If you want to make sure your users see the latest changes after re-deploying your theme, you can enable static asset hashing. In your config.yml, set REVISIONING: true;. Hashing will work on the npm run build and npm run dev commands. It will not be applied on the start command with browsersync. This is by design. Hashing will only change if there are actual changes in the files.

### 3. Get started
```
$ npm or yarn start
```

### 4. Compile assets for production
```
npm or yarn build
```
