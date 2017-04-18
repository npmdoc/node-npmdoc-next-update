# npmdoc-next-update

#### api documentation for  [next-update (v1.5.1)](https://github.com/bahmutov/next-update)  [![npm package](https://img.shields.io/npm/v/npmdoc-next-update.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-next-update) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-next-update.svg)](https://travis-ci.org/npmdoc/node-npmdoc-next-update)

#### Tests if module's dependencies can be updated to the newer version without breaking the tests

[![NPM](https://nodei.co/npm/next-update.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/next-update)

- [https://npmdoc.github.io/node-npmdoc-next-update/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-next-update/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-next-update/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-next-update/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-next-update/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-next-update/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Gleb Bahmutov"
    },
    "bin": {
        "next-update": "bin/next-update.js"
    },
    "bugs": {
        "url": "https://github.com/bahmutov/next-update/issues"
    },
    "config": {
        "pre-git": {
            "commit-msg": "validate-commit-msg",
            "pre-commit": [
                "npm run build",
                "npm test"
            ],
            "pre-push": [
                "npm run size"
            ],
            "post-commit": [],
            "post-merge": []
        }
    },
    "contributors": [],
    "dependencies": {
        "changed-log": "0.11.0",
        "chdir-promise": "0.2.1",
        "check-more-types": "2.22.0",
        "cli-color": "1.1.0",
        "console.json": "0.2.1",
        "console.table": "0.7.0",
        "debug": "2.2.0",
        "deps-ok": "1.1.0",
        "easy-table": "0.3.0",
        "is-online": "5.1.2",
        "lazy-ass": "1.5.0",
        "lodash": "3.10.1",
        "npm-utils": "1.7.1",
        "optimist": "0.6.1",
        "q": "2.0.3",
        "quote": "0.4.0",
        "request": "2.74.0",
        "semver": "5.3.0",
        "update-notifier": "0.5.0"
    },
    "description": "Tests if module's dependencies can be updated to the newer version without breaking the tests",
    "devDependencies": {
        "condition-node-version": "1.3.0",
        "coveralls": "2.11.4",
        "git-issues": "1.2.0",
        "grunt": "0.4.5",
        "grunt-bump": "0.7.3",
        "grunt-cli": "0.1.13",
        "grunt-complexity": "0.3.0",
        "grunt-contrib-jshint": "0.11.3",
        "grunt-deps-ok": "0.9.0",
        "grunt-help": "0.5.0",
        "grunt-jshint-solid": "0.1.1",
        "grunt-jsonlint": "1.1.0",
        "grunt-lineending": "1.0.0",
        "grunt-nice-package": "0.10.2",
        "grunt-readme": "0.4.5",
        "gt": "0.10.0",
        "jshint-stylish": "2.2.1",
        "matchdep": "1.0.1",
        "mocha": "3.0.2",
        "mockery": "1.7.0",
        "pre-git": "1.4.0",
        "publish": "0.6.0",
        "semantic-release": "4.3.5",
        "stop-build": "1.0.1",
        "time-grunt": "1.4.0"
    },
    "directories": {},
    "dist": {
        "shasum": "c6ac37636fef2919324d78d476712b49a201b0ef",
        "tarball": "https://registry.npmjs.org/next-update/-/next-update-1.5.1.tgz"
    },
    "engines": {
        "node": ">= 0.8.0"
    },
    "files": [
        "bin",
        "index.js",
        "src",
        "!src/test"
    ],
    "gitHead": "230d136b5c68dadb1fd5459619df8f7678d28429",
    "homepage": "https://github.com/bahmutov/next-update",
    "keywords": [
        "javascript",
        "node",
        "npm",
        "testing",
        "update",
        "version"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "bahmutov"
        }
    ],
    "name": "next-update",
    "next-update-stats": "http://next-update.herokuapp.com",
    "optionalDependencies": {},
    "preferGlobal": true,
    "release": {
        "verifyConditions": {
            "path": "condition-node-version",
            "node": "4"
        }
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/bahmutov/next-update.git"
    },
    "scripts": {
        "2npm": "publish",
        "build": "grunt",
        "commit": "git-issues && commit-wizard",
        "coveralls": "cat cover/lcov.info | ./node_modules/coveralls/bin/coveralls.js",
        "dont-break": "dont-break",
        "e2e": "npm run install-for-tests && gt test/*.coffee --output",
        "install-for-tests": "cd test/test-next-updater && npm install",
        "issues": "git-issues",
        "limited": "gt --filter 'allow major' --output src/test/*.coffee",
        "mocha": "mocha test/*-spec.js",
        "posttest": "npm run mocha && npm run e2e",
        "pretest": "npm run build",
        "self-update": "node bin/next-update.js -k true",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "size": "t=\"$(npm pack .)\"; wc -c \"${t}\"; tar tvf \"${t}\"; rm \"${t}\";",
        "test": "npm run unit",
        "unit": "gt src/test/*.js src/test/*.coffee --output"
    },
    "version": "1.5.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
