# npmtest-serializr

#### basic test coverage for  serializr (v1.1.11)  [![npm package](https://img.shields.io/npm/v/npmtest-serializr.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-serializr) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-serializr.svg)](https://travis-ci.org/npmtest/node-npmtest-serializr)

#### Serialize and deserialize complex object graphs to JSON

[![NPM](https://nodei.co/npm/serializr.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/serializr)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-serializr/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-serializr/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-serializr/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-serializr/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-serializr/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-serializr/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-serializr/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-serializr/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-serializr/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-serializr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-serializr/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-serializr/build/test-report.html](https://npmtest.github.io/node-npmtest-serializr/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-serializr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-serializr/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-serializr/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-serializr/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-serializr/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-serializr/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-serializr/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-serializr/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "serializr",
    "version": "1.1.11",
    "description": "Serialize and deserialize complex object graphs to JSON",
    "main": "serializr.js",
    "typings": "serializr.d.ts",
    "scripts": {
        "test": "npm run build-test && node test/index",
        "lint": "eslint serializr.js",
        "prepublish": "npm run small-build && npm run build-docs",
        "small-build": "uglifyjs -m sort,toplevel -c --screw-ie8 --preamble '/** serializr - (c) Michel Weststrate 2016 - MIT Licensed */' --source-map serializr.min.js.map -o serializr.min.js serializr.js",
        "build-docs": "documentation readme serializr.js --github --section API",
        "build-test": "npm run build-test-babel && npm run build-test-ts",
        "build-test-ts": "tsc -p test/typescript",
        "build-test-babel": "babel test/babel/babel.js -o test/babel/babel-compiled.js",
        "coverage": "npm run build-test && istanbul cover tape test/*.js"
    },
    "keywords": [
        "serialize",
        "deserialize",
        "graph",
        "json",
        "mobx"
    ],
    "repository": {
        "type": "git",
        "url": "https://github.com/mobxjs/serializr.git"
    },
    "author": "Michel Weststrate",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/mobxjs/serializr/issues"
    },
    "files": [
        "serializr.js",
        "serializr.min.js",
        "serializr.min.js.map",
        "serializr.d.ts"
    ],
    "devDependencies": {
        "babel-cli": "^6.11.4",
        "babel-plugin-transform-decorators-legacy": "^1.3.4",
        "babel-preset-es2015": "^6.9.0",
        "babel-preset-stage-1": "^6.5.0",
        "coveralls": "^2.11.9",
        "documentation": "^4.0.0-beta9",
        "eslint": "^2.12.0",
        "istanbul": "^0.4.4",
        "mobx": "^2.4.1 || ^3.0.0",
        "tape": "^4.5.1",
        "typescript": "^2.1.4",
        "uglify-js": "^2.6.4"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
