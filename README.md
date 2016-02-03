# Introduction

[![Join the chat at https://gitter.im/hakandilek/servi](https://badges.gitter.im/hakandilek/servi.svg)](https://gitter.im/hakandilek/servi?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Build Status](https://travis-ci.org/hakandilek/servi.svg?branch=master)](https://travis-ci.org/hakandilek/servi)
[![Join the chat at https://gitter.im/hakandilek/servi](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/hakandilek/servi?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![Dependency Status](https://david-dm.org/hakandilek/servi.svg)](https://david-dm.org/hakandilek/servi)
[![devDependency Status](https://david-dm.org/hakandilek/servi/dev-status.svg)](https://david-dm.org/hakandilek/servi#info=devDependencies)


# How to start

**Note** that this project requires node v4.x.x or higher and npm 2.14.7.

You must have `ts-node` installed as global. If you don't, use:

```bash
npm install -g ts-node
```

In order to start the seed use:


```bash
git clone --depth 1 https://github.com/hakandilek/servi.git
cd servi
# install the project's dependencies
npm install
# watches your files and uses livereload by default
npm start
# api document for the app
npm run docs

# dev build
npm run build.dev
# prod build
npm run build.prod
```

## Using the experimental hot loader support

If you want to try the experimental [hot loading](http://blog.mgechev.com/2015/10/26/angular2-hot-loader-hot-loading-tooling/) support use:

```
npm start -- --hot-loader true
```

Note that the hot loader is still in experimental phase of development and there are some missing features. If you experience any issues with it report them at [here](https://github.com/mgechev/angular2-hot-loader/issues).

_Does not rely on any global dependencies._

# Configuration

Default application server configuration

```javascript
var PORT             = 5555;
var LIVE_RELOAD_PORT = 4002;
var DOCS_PORT        = 4003;
var APP_BASE         = '/';
```

Configure at runtime

```bash
npm start -- --port 8080 --reload-port 4000 --base /my-app/
```

# Running test

```bash
npm test

# Debug - In two different shell windows
npm run build.test.watch      # 1st window
npm run karma.start           # 2nd window

# e2e (aka. end-to-end, integration) - In three different shell windows
npm start
# npm run webdriver-update <- You may need to run this the first time
npm run webdriver-start
npm run e2e

# e2e live mode - Protractor interactive mode
# Instead of last command above, you can use:
npm run e2e-live
```
You can learn more about [Protractor Interactive Mode here](https://github.com/angular/protractor/blob/master/docs/debugging.md#testing-out-protractor-interactively)

# Change Log

You can follow the [Angular 2 change log here](https://github.com/angular/angular/blob/master/CHANGELOG.md).

# License

MIT