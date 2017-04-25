# npmdoc-hjson

#### basic api documentation for  [hjson (v2.4.1)](http://hjson.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-hjson.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-hjson) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-hjson.svg)](https://travis-ci.org/npmdoc/node-npmdoc-hjson)

#### A user interface for JSON.

[![NPM](https://nodei.co/npm/hjson.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/hjson)

- [https://npmdoc.github.io/node-npmdoc-hjson/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-hjson/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-hjson/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-hjson/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-hjson/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-hjson/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Christian Zangl"
    },
    "bin": {
        "hjson": "./bin/hjson"
    },
    "bugs": {
        "url": "https://github.com/hjson/hjson-js/issues"
    },
    "dependencies": {},
    "description": "A user interface for JSON.",
    "devDependencies": {
        "browserify": "^13.1.1",
        "eslint": "^3.12.2",
        "uglify-js": "^2.4.24"
    },
    "directories": {},
    "dist": {
        "shasum": "b394035e9c69c4fce16394609d34e082107527f7",
        "tarball": "https://registry.npmjs.org/hjson/-/hjson-2.4.1.tgz"
    },
    "gitHead": "7fd0ab530b54b4294dce828adcb09158f29cc325",
    "homepage": "http://hjson.org",
    "keywords": [
        "json",
        "comments",
        "config",
        "hjson",
        "parser",
        "serializer",
        "human"
    ],
    "license": "MIT",
    "main": "./lib/hjson.js",
    "maintainers": [
        {
            "name": "laktak"
        }
    ],
    "name": "hjson",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/hjson/hjson-js.git"
    },
    "scripts": {
        "build": "npm run build_v1 && npm run build_v2 && npm run test && npm run lint && npm run build_bundle && npm run build_min",
        "build_bundle": "node_modules/browserify/bin/cmd.js lib/hjson.js --ignore os -s Hjson -o bundle/hjson.js",
        "build_min": "node node_modules/uglify-js/bin/uglifyjs bundle/hjson.js --comments -c -m -o bundle/hjson.min.js",
        "build_v1": "node -e 'console.log(\"module.exports=\\\"\"+eval(\"(\"+process.argv[1]+\")\").version+\"\\\";\");' -- \"'cat package.json'\" > lib/hjson-version.js",
        "build_v2": "node -e 'var v=\" * Hjson v\"+eval(\"(\"+process.argv[1]+\")\").version; if (v!==process.argv[2]) throw new Error(\"ver\");' -- \"'cat package.json'\" \"'grep -E '\\* Hjson v.*$' lib/hjson.js'\"",
        "lint": "node_modules/eslint/bin/eslint.js -f unix bin/hjson lib/*.js",
        "test": "node ./test/test.js"
    },
    "version": "2.4.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
