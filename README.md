# npmdoc-swig

#### api documentation for  [swig (v1.4.2)](https://github.com/paularmstrong/swig)  [![npm package](https://img.shields.io/npm/v/npmdoc-swig.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-swig) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-swig.svg)](https://travis-ci.org/npmdoc/node-npmdoc-swig)

#### A simple, powerful, and extendable templating engine for node.js and browsers, similar to Django, Jinja2, and Twig.

[![NPM](https://nodei.co/npm/swig.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/swig)

- [https://npmdoc.github.io/node-npmdoc-swig/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-swig/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-swig/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-swig/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-swig/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-swig/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Paul Armstrong"
    },
    "bin": {
        "swig": "./bin/swig.js"
    },
    "bugs": {
        "url": "https://github.com/paularmstrong/swig/issues"
    },
    "dependencies": {
        "optimist": "~0.6",
        "uglify-js": "~2.4"
    },
    "deprecated": "This package is no longer maintained",
    "description": "A simple, powerful, and extendable templating engine for node.js and browsers, similar to Django, Jinja2, and Twig.",
    "devDependencies": {
        "blanket": "~1.1",
        "browserify": "~2",
        "expect.js": "~0.2",
        "express": "~3",
        "file": "~0.2",
        "jsdoc": "~3.2",
        "less": "~1.4",
        "lodash": "~1.3.1",
        "mocha": "1.12.0",
        "mocha-phantomjs": "~3.1",
        "nodelint": "~0.6",
        "phantomjs": "~1.9.1",
        "still": "0.0.7",
        "travis-cov": "~0.2"
    },
    "directories": {},
    "dist": {
        "shasum": "4085ca0453369104b5d483e2841b39b7ae1aaba5",
        "tarball": "https://registry.npmjs.org/swig/-/swig-1.4.2.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "homepage": "https://github.com/paularmstrong/swig",
    "keywords": [
        "template",
        "templating",
        "html",
        "django",
        "jinja",
        "twig",
        "express",
        "block"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "paularmstrong"
        }
    ],
    "name": "swig",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/paularmstrong/swig.git"
    },
    "scripts": {
        "prepublish": "npm prune && make build",
        "test": "make lint && make test reporter=spec && make test-browser && make coverage cov-reporter=travis-cov"
    },
    "version": "1.4.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
