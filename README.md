# api documentation for  [google-trends-api (v4.1.0)](https://github.com/pat310/google-trends-api#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-google-trends-api.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-google-trends-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-google-trends-api.svg)](https://travis-ci.org/npmdoc/node-npmdoc-google-trends-api)
#### an API layer on top of google trends

[![NPM](https://nodei.co/npm/google-trends-api.png?downloads=true)](https://www.npmjs.com/package/google-trends-api)

[![apidoc](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-google-trends-api_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-google-trends-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Patrick Trasborg",
        "email": "patrick.trasborg@gmail.com",
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
            "name": "pat310",
            "email": "bacon7473@gmail.com"
        }
    ],
    "name": "google-trends-api",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module google-trends-api](#apidoc.module.google-trends-api)
1.  [function <span class="apidocSignatureSpan">google-trends-api.</span>interestByRegion (t, r)](#apidoc.element.google-trends-api.interestByRegion)
1.  [function <span class="apidocSignatureSpan">google-trends-api.</span>interestOverTime (t, r)](#apidoc.element.google-trends-api.interestOverTime)
1.  [function <span class="apidocSignatureSpan">google-trends-api.</span>relatedQueries (t, r)](#apidoc.element.google-trends-api.relatedQueries)
1.  [function <span class="apidocSignatureSpan">google-trends-api.</span>relatedTopics (t, r)](#apidoc.element.google-trends-api.relatedTopics)



# <a name="apidoc.module.google-trends-api"></a>[module google-trends-api](#apidoc.module.google-trends-api)

#### <a name="apidoc.element.google-trends-api.interestByRegion"></a>[function <span class="apidocSignatureSpan">google-trends-api.</span>interestByRegion (t, r)](#apidoc.element.google-trends-api.interestByRegion)
- description and source-code
```javascript
interestByRegion = function (t, r){var o=(0,n.constructObj)(t,r),i=o.cbFunc,u=o.obj;return u instanceof Error?Promise.reject(i(u)):(0,n.getResults)(
e,u).then(function(e){return i(null,e)})["catch"](function(e){return Promise.reject(i(e))})}
```
- example usage
```shell
...

<hr>

#### interestByRegion
*See in which location your term was most popular during the specified time frame. Values are calculated on a scale from 0 to 100
, where 100 is the location with the most popularity as a fraction of total searches in that location.*

#####Syntax
'googleTrends.interestByRegion({keyword: string, startTime: Date, endTime: Date, geo: string, resolution: string}, cbFunc)'

Requires an 'object' as the first parameter with the following keys:
* 'keyword' - **required** - type 'string' or 'array' - the search term(s) of interest
* 'startTime' - *optional* - type 'Date' object - the start of the time range of interest (defaults to 'new Date('2004-01-01')'
if not supplied)
* 'endTime' - *optional* - type 'Date' object - the end of the time range of interest (defaults to 'new Date(Date.now())' if not
 supplied)
* 'geo' - *optional* - type 'string' - geocode for a country, region, or DMA depending on the granularity required (defaults to
worldwide).  For example, 'geo: 'US-CA-800'' will target the Bakersfield, California, United States or 'geo: 'US'' will just target
 the US.
* 'resolution' - *optional* - type 'enumerated string' either 'COUNTRY', 'REGION', 'CITY' or 'DMA'.  Resolution is selected by default
 otherwise.  Trying to select a resolution larger than a specified 'geo' will return an error.
...
```

#### <a name="apidoc.element.google-trends-api.interestOverTime"></a>[function <span class="apidocSignatureSpan">google-trends-api.</span>interestOverTime (t, r)](#apidoc.element.google-trends-api.interestOverTime)
- description and source-code
```javascript
interestOverTime = function (t, r){var o=(0,n.constructObj)(t,r),i=o.cbFunc,u=o.obj;return u instanceof Error?Promise.reject(i(u)):(0,n.getResults)(
e,u).then(function(e){return i(null,e)})["catch"](function(e){return Promise.reject(i(e))})}
```
- example usage
```shell
...
<hr>

## API

### Promises
By default, all the API's return a promise for the results.  Example:
'''js
googleTrends.interestOverTime({keyword: 'Women\'s march'})
.then(function(results){
  console.log('These results are awesome', results);
})
.catch(function(err){
  console.error('Oh no there was an error', err);
});
'''
...
```

#### <a name="apidoc.element.google-trends-api.relatedQueries"></a>[function <span class="apidocSignatureSpan">google-trends-api.</span>relatedQueries (t, r)](#apidoc.element.google-trends-api.relatedQueries)
- description and source-code
```javascript
relatedQueries = function (t, r){var o=(0,n.constructObj)(t,r),i=o.cbFunc,u=o.obj;return u instanceof Error?Promise.reject(i(u)):(0,n.getResults)(
e,u).then(function(e){return i(null,e)})["catch"](function(e){return Promise.reject(i(e))})}
```
- example usage
```shell
...

<hr>

#### relatedQueries
*Users searching for your term also searched for these queries.*

#####Syntax
'googleTrends.relatedQueries({keyword: string, startTime: Date, endTime: Date, geo: string}, cbFunc)'

Requires an 'object' as the first parameter with the following keys:
* 'keyword' - **required** - type 'string' or 'array' - the search term(s) of interest
* 'startTime' - *optional* - type 'Date' object - the start of the time range of interest (defaults to 'new Date('2004-01-01')'
if not supplied)
* 'endTime' - *optional* - type 'Date' object - the end of the time range of interest (defaults to 'new Date(Date.now())' if not
 supplied)
* 'geo' - *optional* - type 'string' - geocode for a country, region, or DMA depending on the granularity required (defaults to
worldwide).  For example, 'geo: 'US-CA-800'' will target the Bakersfield, California, United States or 'geo: 'US'' will just target
 the US.
* 'hl' - *optional* - type 'string' - preferred language code for results (defaults to english)
...
```

#### <a name="apidoc.element.google-trends-api.relatedTopics"></a>[function <span class="apidocSignatureSpan">google-trends-api.</span>relatedTopics (t, r)](#apidoc.element.google-trends-api.relatedTopics)
- description and source-code
```javascript
relatedTopics = function (t, r){var o=(0,n.constructObj)(t,r),i=o.cbFunc,u=o.obj;return u instanceof Error?Promise.reject(i(u)):(0,n.getResults)(
e,u).then(function(e){return i(null,e)})["catch"](function(e){return Promise.reject(i(e))})}
```
- example usage
```shell
...

<hr>

#### relatedTopics
*Users searching for your term also searched for these topics*

#####Syntax
'googleTrends.relatedTopics({keyword: string, startTime: Date, endTime: Date, geo: string}, cbFunc)'

Requires an 'object' as the first parameter with the following keys:
* 'keyword' - **required** - type 'string' or 'array' - the search term(s) of interest
* 'startTime' - *optional* - type 'Date' object - the start of the time range of interest (defaults to 'new Date('2004-01-01')'
if not supplied)
* 'endTime' - *optional* - type 'Date' object - the end of the time range of interest (defaults to 'new Date(Date.now())' if not
 supplied)
* 'geo' - *optional* - type 'string' - geocode for a country, region, or DMA depending on the granularity required (defaults to
worldwide).  For example, 'geo: 'US-CA-800'' will target the Bakersfield, California, United States or 'geo: 'US'' will just target
 the US.
* 'hl' - *optional* - type 'string' - preferred language code for results (defaults to english)
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
