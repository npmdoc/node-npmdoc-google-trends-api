# npmdoc-google-trends-api

#### api documentation for  [google-trends-api (v4.1.0)](https://github.com/pat310/google-trends-api#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-google-trends-api.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-google-trends-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-google-trends-api.svg)](https://travis-ci.org/npmdoc/node-npmdoc-google-trends-api)

#### an API layer on top of google trends

[![NPM](https://nodei.co/npm/google-trends-api.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/google-trends-api)

- [https://npmdoc.github.io/node-npmdoc-google-trends-api/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Patrick Trasborg",
        "url": "http://trasb.org"
    },
    "bugs": {
        "url": "https://github.com/pat310/google-trends-api/issues"
    },
    "dependencies": {},
    "description": "an API layer on top of google trends",
    "devDependencies": {
        "babel": "6.3.13",
        "babel-core": "6.1.18",
        "babel-eslint": "5.0.0",
        "babel-loader": "6.1.0",
        "babel-plugin-add-module-exports": "0.1.2",
        "babel-plugin-transform-es2015-destructuring": "^6.23.0",
        "babel-plugin-transform-object-rest-spread": "^6.23.0",
        "babel-preset-es2015": "6.3.13",
        "chai": "3.4.1",
        "coveralls": "^2.11.15",
        "eslint": "1.7.2",
        "eslint-loader": "1.1.0",
        "istanbul": "^0.4.5",
        "json-loader": "^0.5.4",
        "mocha": "2.3.4",
        "mocha-lcov-reporter": "^1.2.0",
        "nyc": "^10.1.2",
        "webpack": "1.12.9",
        "yargs": "3.32.0"
    },
    "directories": {},
    "dist": {
        "shasum": "79ee1b41d0e1b1c15b984911062ee839f232dfa5",
        "tarball": "https://registry.npmjs.org/google-trends-api/-/google-trends-api-4.1.0.tgz"
    },
    "gitHead": "0e6f58692aea006e179211fbaab81db626e1c286",
    "homepage": "https://github.com/pat310/google-trends-api#readme",
    "keywords": [
        "google",
        "trends",
        "API",
        "keyword",
        "search",
        "google-trends"
    ],
    "license": "MIT",
    "main": "lib/google-trends-api.min.js",
    "maintainers": [
        {
            "name": "pat310"
        }
    ],
    "name": "google-trends-api",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pat310/google-trends-api.git"
    },
    "scripts": {
        "build": "webpack --mode=build",
        "cover": "nyc --reporter=lcov mocha --compilers js:babel-core/register --colors ./test/*.spec.js",
        "coverage": "nyc mocha --compilers js:babel-core/register --colors ./test/*.spec.js",
        "coveralls": "npm run cover && nyc report --reporter=text-lcov | coveralls",
        "dev": "webpack --progress --colors --watch --mode=dev",
        "preversion": "npm run build",
        "start": "npm run dev",
        "test": "mocha --compilers js:babel-core/register --colors ./test/*.spec.js",
        "test:watch": "mocha --compilers js:babel-core/register --colors -w ./test/*.spec.js"
    },
    "version": "4.1.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
