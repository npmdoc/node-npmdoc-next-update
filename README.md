# api documentation for  [next-update (v1.5.1)](https://github.com/bahmutov/next-update)  [![npm package](https://img.shields.io/npm/v/npmdoc-next-update.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-next-update) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-next-update.svg)](https://travis-ci.org/npmdoc/node-npmdoc-next-update)
#### Tests if module's dependencies can be updated to the newer version without breaking the tests

[![NPM](https://nodei.co/npm/next-update.png?downloads=true)](https://www.npmjs.com/package/next-update)

[![apidoc](https://npmdoc.github.io/node-npmdoc-next-update/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-next-update_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-next-update/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-next-update/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-next-update/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Gleb Bahmutov",
        "email": "gleb.bahmutov@gmail.com"
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
            "name": "bahmutov",
            "email": "gleb.bahmutov@gmail.com"
        }
    ],
    "name": "next-update",
    "next-update-stats": "http://next-update.herokuapp.com",
    "optionalDependencies": {},
    "preferGlobal": true,
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module next-update](#apidoc.module.next-update)
1.  object <span class="apidocSignatureSpan">next-update.</span>next_update
1.  object <span class="apidocSignatureSpan">next-update.</span>registry
1.  object <span class="apidocSignatureSpan">next-update.</span>report
1.  object <span class="apidocSignatureSpan">next-update.</span>stats

#### [module next-update.next_update](#apidoc.module.next-update.next_update)
1.  [function <span class="apidocSignatureSpan">next-update.next_update.</span>available (moduleName, options)](#apidoc.element.next-update.next_update.available)
1.  [function <span class="apidocSignatureSpan">next-update.next_update.</span>checkAllUpdates (options)](#apidoc.element.next-update.next_update.checkAllUpdates)
1.  [function <span class="apidocSignatureSpan">next-update.next_update.</span>checkCurrentInstall (options)](#apidoc.element.next-update.next_update.checkCurrentInstall)

#### [module next-update.registry](#apidoc.module.next-update.registry)
1.  [function <span class="apidocSignatureSpan">next-update.registry.</span>cleanVersion (version, name)](#apidoc.element.next-update.registry.cleanVersion)
1.  [function <span class="apidocSignatureSpan">next-update.registry.</span>cleanVersions (nameVersionPairs)](#apidoc.element.next-update.registry.cleanVersions)
1.  [function <span class="apidocSignatureSpan">next-update.registry.</span>fetchVersions (nameVersion)](#apidoc.element.next-update.registry.fetchVersions)
1.  [function <span class="apidocSignatureSpan">next-update.registry.</span>isUrl (str)](#apidoc.element.next-update.registry.isUrl)
1.  [function <span class="apidocSignatureSpan">next-update.registry.</span>nextVersions (options, nameVersionPairs, checkLatestOnly)](#apidoc.element.next-update.registry.nextVersions)

#### [module next-update.report](#apidoc.module.next-update.report)
1.  [function <span class="apidocSignatureSpan">next-update.</span>report (updates, options)](#apidoc.element.next-update.report.report)
1.  [function <span class="apidocSignatureSpan">next-update.report.</span>reportFailure (text, useColors)](#apidoc.element.next-update.report.reportFailure)
1.  [function <span class="apidocSignatureSpan">next-update.report.</span>reportSuccess (text, useColors)](#apidoc.element.next-update.report.reportSuccess)

#### [module next-update.stats](#apidoc.module.next-update.stats)
1.  [function <span class="apidocSignatureSpan">next-update.stats.</span>colorProbability (probability, options)](#apidoc.element.next-update.stats.colorProbability)
1.  [function <span class="apidocSignatureSpan">next-update.stats.</span>getSuccessStats (options)](#apidoc.element.next-update.stats.getSuccessStats)
1.  [function <span class="apidocSignatureSpan">next-update.stats.</span>printStats (options, stats)](#apidoc.element.next-update.stats.printStats)
1.  [function <span class="apidocSignatureSpan">next-update.stats.</span>sendUpdateResult (options)](#apidoc.element.next-update.stats.sendUpdateResult)
1.  string <span class="apidocSignatureSpan">next-update.stats.</span>url



# <a name="apidoc.module.next-update"></a>[module next-update](#apidoc.module.next-update)



# <a name="apidoc.module.next-update.next_update"></a>[module next-update.next_update](#apidoc.module.next-update.next_update)

#### <a name="apidoc.element.next-update.next_update.available"></a>[function <span class="apidocSignatureSpan">next-update.next_update.</span>available (moduleName, options)](#apidoc.element.next-update.next_update.available)
- description and source-code
```javascript
function available(moduleName, options) {
    options = options || {};
    var toCheck = getDependenciesToCheck(options, moduleName);
    la(check.array(toCheck), 'expected object of deps to check, was', toCheck);
    var toCheckHash = _.zipObject(
        _.pluck(toCheck, 'name'),
        _.pluck(toCheck, 'version')
    );

    log('need to check these dependencies');
    log(toCheckHash);

    var nextVersionsPromise = nextVersions(options, toCheck);
    return nextVersionsPromise.then(function (info) {
        return reportAvailable(info, toCheckHash, options);
    }, function (error) {
        console.error('Could not fetch available modules\n', error);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.next_update.checkAllUpdates"></a>[function <span class="apidocSignatureSpan">next-update.next_update.</span>checkAllUpdates (options)](#apidoc.element.next-update.next_update.checkAllUpdates)
- description and source-code
```javascript
function checkAllUpdates(options) {
    options = options || {};
    var moduleName = options.names;
    var checkLatestOnly = !!options.latest;
    var checkCommand = options.testCommand;
    if (checkCommand) {
        verify.unemptyString(checkCommand, 'invalid test command ' + checkCommand);
    }
    var all = options.all;
    if (all) {
        checkLatestOnly = true;
        console.log('will check only latest versions because testing all');
    }

    if (check.string(moduleName)) {
        moduleName = [moduleName];
    }
    checkLatestOnly = !!checkLatestOnly;
    if (checkCommand) {
        check.verify.string(checkCommand, 'expected string test command');
    }
    var toCheck = getDependenciesToCheck(options, moduleName);
    check.verify.array(toCheck, 'dependencies to check should be an array');

    makeSureValidModule(moduleName, toCheck);

    var testVersionsBound = testVersions.bind(null, {
        modules: toCheck,
        command: checkCommand,
        all: all,
        color: options.color,
        keep: options.keep,
        allowed: options.allow || options.allowed,
        tldr: options.tldr,
        type: options.type
    });

    return isOnline()
        .then(function (online) {
            if (!online) {
                throw new Error('Need to be online to check new modules');
            }
        }).then(function () {
            if (isSingleSpecificVersion(moduleName)) {
                var nv = nameVersionParser(moduleName[0]);
                console.log('checking only specific:', nv.name, nv.version);
                var list = [{
                    name: nv.name,
                    versions: [nv.version]
                }];
                return testVersionsBound(list);
            } else {
                var nextVersionsPromise = nextVersions(options, toCheck, checkLatestOnly);
                return nextVersionsPromise.then(testVersionsBound);
            }
        });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.next_update.checkCurrentInstall"></a>[function <span class="apidocSignatureSpan">next-update.next_update.</span>checkCurrentInstall (options)](#apidoc.element.next-update.next_update.checkCurrentInstall)
- description and source-code
```javascript
function checkCurrentInstall(options) {
    options = options || {};
    var log = options.tldr ? _.noop : boundConsoleLog;
    log('checking if the current state works');

    return cleanDependencies()
        .then(checkDependenciesInstalled)
        .then(function () {
            return runTest(options, options.testCommand)();
        })
        .then(function () {
            console.log('> tests are passing at the start');
        });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.next-update.registry"></a>[module next-update.registry](#apidoc.module.next-update.registry)

#### <a name="apidoc.element.next-update.registry.cleanVersion"></a>[function <span class="apidocSignatureSpan">next-update.registry.</span>cleanVersion (version, name)](#apidoc.element.next-update.registry.cleanVersion)
- description and source-code
```javascript
function cleanVersion(version, name) {
    var originalVersion = version;
    verify.unemptyString(version, 'missing version string' + version);
    verify.unemptyString(name, 'missing name string' + name);

    if (isUrl(version)) {
        // version = version.substr(version.indexOf('#') + 1);

        // hmm, because we don't have a way to fetch git tags yet
        // just skip these dependencies
        console.log('Cannot handle git repos, skipping', name, 'at', version);
        return;
    }
    if (version === 'original' ||
        version === 'modified' ||
        version === 'created') {
        return;
    }

    version = version.replace('~', '').replace('^', '');
    var twoDigitVersion = /^\d+\.\d+$/;
    if (twoDigitVersion.test(version)) {
        version += '.0';
    }
    if (version === 'latest' || version === '*') {
        console.log('Module', name, 'uses version', version);
        console.log('It is recommented to list a specific version number');
        version = localVersion(name);
        if (!version) {
            version = '0.0.1';
        }
        console.log('module', name, 'local version', version);
    }
    try {
        version = semver.clean(version);
    } catch (err) {
        console.error('exception when cleaning version', version);
        return;
    }
    if (!version) {
        log('could not clean version ' + originalVersion + ' for ' + name);
        return;
    }
    console.assert(version, 'missing clean version ' + originalVersion + ' for ' + name);
    return version;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.registry.cleanVersions"></a>[function <span class="apidocSignatureSpan">next-update.registry.</span>cleanVersions (nameVersionPairs)](#apidoc.element.next-update.registry.cleanVersions)
- description and source-code
```javascript
function cleanVersions(nameVersionPairs) {
    check.verify.array(nameVersionPairs, 'expected array');
    var cleaned = nameVersionPairs
        .map(cleanVersionObject)
        .filter(check.object);
    return cleaned;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.registry.fetchVersions"></a>[function <span class="apidocSignatureSpan">next-update.registry.</span>fetchVersions (nameVersion)](#apidoc.element.next-update.registry.fetchVersions)
- description and source-code
```javascript
function fetchVersions(nameVersion) {
    // console.log(nameVersion);
    // TODO use check.schema
    check.verify.object(nameVersion, 'expected name, version object');
    var name = nameVersion.name;
    var version = nameVersion.version;
    check.verify.string(name, 'missing name string');
    check.verify.string(version, 'missing version string');

    var cleanVersionForName = _.partial(cleanVersionFor, name);
    function isLaterVersion(ver) {
        var later = semver.gt(ver, version);
        return later;
    }

    // console.log('fetching versions for', name, 'current version', version);
    var MAX_WAIT_TIMEOUT = 25000;
    var deferred = q.defer();

    function rejectOnTimeout() {
        var msg = 'timed out waiting for NPM for package ' + name +
            ' after ' + MAX_WAIT_TIMEOUT + 'ms';
        console.error(msg);
        deferred.reject(msg);
    }

    function escapeName(str) {
        return str.replace('/', '%2F');
    }

    registryUrl().then(function (npmUrl) {
        log('NPM registry url', npmUrl);
        la(check.webUrl(npmUrl), 'need npm registry url, got', npmUrl);

        npmUrl = npmUrl.replace(/^https:/, 'http:').trim();
        var url = npmUrl + escapeName(name);

        // TODO how to detect if the registry is not responding?

        log('getting url', url);
        request.get(url, onNPMversions);
        var timer = setTimeout(rejectOnTimeout, MAX_WAIT_TIMEOUT);

        function onNPMversions(err, response, body) {
            log('got response for', url);
            clearTimeout(timer);

            if (err) {
                console.error('ERROR when fetching info for package', name);
                deferred.reject(err.message);
                return;
            }

            if (is404(response)) {
                log('404 response for', url);
                deferred.resolve({
                    name: name,
                    versions: []
                });
                return;
            }

            try {
                log('parsing response body');
                var info = JSON.parse(body);
                log('parsed response, error?', info.error);
                if (info.error) {
                    log('error parsing\n' + body + '\n');
                    var str = formNpmErrorMessage(name, info);
                    console.error(str);

                    if (isNotFound(info.error)) {
                        deferred.resolve({
                            name: name,
                            versions: []
                        });
                        return;
                    }

                    deferred.reject(str);
                    return;
                }
                log('extracting versions');
                var versions = extractVersions(info);
                log('versions', versions);

                if (!Array.isArray(versions)) {
                    throw new Error('Could not get versions for ' + name +
                        ' from ' + JSON.stringify(info) +
                        ' response ' + JSON.stringify(response, null, 2));
                }

                var validVersions = versions.filter(cleanVersionForName);
                var newerVersions = validVersions.filter(isLaterVersion);
                log('valid versions', validVersions);
                log('newer versions', newerVersions);

                deferred.resolve({
                    name: name,
                    versions: newerVersions
                });
                return;
            } catch (err) {
                console.error(err);
                deferred.reject('Could not fetch versions for ' + name);
                return;
            }
        }
    });

    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.registry.isUrl"></a>[function <span class="apidocSignatureSpan">next-update.registry.</span>isUrl (str)](#apidoc.element.next-update.registry.isUrl)
- description and source-code
```javascript
function isUrl(str) {
  la(check.string(str), 'expected a string');
  return httpTester.test(str) || gitTester.test(str);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.registry.nextVersions"></a>[function <span class="apidocSignatureSpan">next-update.registry.</span>nextVersions (options, nameVersionPairs, checkLatestOnly)](#apidoc.element.next-update.registry.nextVersions)
- description and source-code
```javascript
function nextVersions(options, nameVersionPairs, checkLatestOnly) {
    check.verify.object(options, 'expected object with options');
    check.verify.array(nameVersionPairs, 'expected array');
    checkLatestOnly = !!checkLatestOnly;
    nameVersionPairs = cleanVersions(nameVersionPairs);

    var MAX_CHECK_TIMEOUT = 10000;

    if (!options.tldr) {
        console.log('checking NPM registry');
    }
    var fetchPromises = nameVersionPairs.map(fetchVersions);
    var fetchAllPromise = q.all(fetchPromises)
        .timeout(MAX_CHECK_TIMEOUT, 'timed out waiting for NPM');

    return fetchAllPromise.then(function (results) {
        check.verify.array(results, 'expected list of results');
        log('fetch all new version results');
        log(results);

        var available = results.filter(function (nameNewVersions) {
            return nameNewVersions &&
                check.array(nameNewVersions.versions) &&
                nameNewVersions.versions.length;
        });
        if (checkLatestOnly) {
            available = available.map(function (nameVersions) {
                if (nameVersions.versions.length > 1) {
                    nameVersions.versions = nameVersions.versions.slice(-1);
                }
                return nameVersions;
            });
        } else {
            console.log('checking ALL versions');
        }
        return available;
    }, function (error) {
        return q.reject(error);
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.next-update.report"></a>[module next-update.report](#apidoc.module.next-update.report)

#### <a name="apidoc.element.next-update.report.report"></a>[function <span class="apidocSignatureSpan">next-update.</span>report (updates, options)](#apidoc.element.next-update.report.report)
- description and source-code
```javascript
function report(updates, options) {
    options = options || {};
    var useColors = Boolean(options.useColors) && colorAvailable;
    check.verify.array(updates, 'expected array of updates');
    // sets latest working version for each module too
    var cmd = formInstallCommand(updates);

    console.log('\n> next updates:');
    updates.forEach(function (moduleVersions) {
        reportModule(moduleVersions, useColors);
    });

    var reportChanges = updates.map(function (moduleVersions) {
        return _.partial(printChangedLog, moduleVersions, useColors);
    });

    function printInstallCommand() {
        if (_.isUndefined(cmd)) {
            console.log('> nothing can be updated :(');
        } else {
            if (options.keptUpdates) {
                console.log('> kept working updates');
            } else {
                cmd = cmd.trim();
                var lines = cmd.split('\n').length;
                if (lines === 1) {
                    console.log('> use the following command to install working versions');
                } else {
                    console.log('> use the following commands to install working versions');
                }
                console.log(cmd);
            }
        }
    }

    function printError(err) {
        console.error('Error reporting changes');
        console.error(err.message);
    }
    var start = options.changedLog ?
        reportChanges.reduce(Q.when, Q()).catch(printError) :
        Q();
    return start.then(printInstallCommand);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.report.reportFailure"></a>[function <span class="apidocSignatureSpan">next-update.report.</span>reportFailure (text, useColors)](#apidoc.element.next-update.report.reportFailure)
- description and source-code
```javascript
function reportFailure(text, useColors) {
    if (colorAvailable && useColors) {
        console.log(colors.redBright(text));
    } else {
        console.log('FAIL', text);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.report.reportSuccess"></a>[function <span class="apidocSignatureSpan">next-update.report.</span>reportSuccess (text, useColors)](#apidoc.element.next-update.report.reportSuccess)
- description and source-code
```javascript
function reportSuccess(text, useColors) {
    if (colorAvailable && useColors) {
        console.log(colors.greenBright(text));
    } else {
        console.log('PASS', text);
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.next-update.stats"></a>[module next-update.stats](#apidoc.module.next-update.stats)

#### <a name="apidoc.element.next-update.stats.colorProbability"></a>[function <span class="apidocSignatureSpan">next-update.stats.</span>colorProbability (probability, options)](#apidoc.element.next-update.stats.colorProbability)
- description and source-code
```javascript
function colorProbability(probability, options) {
    if (probability === null) {
        return '';
    }

    options = options || {};
    var useColors = !!options.color && colorAvailable;
    if (probability < 0 || probability > 1) {
        throw new Error('Expected probability between 0 and 1, not ' + probability);
    }
    var probabilityStr = (probability * 100).toFixed(0) + '%';
    if (useColors) {
        if (probability > 0.8) {
            probabilityStr = colors.greenBright(probabilityStr);
        } else if (probability > 0.5) {
            probabilityStr = colors.yellowBright(probabilityStr);
        } else {
            probabilityStr = colors.redBright(probabilityStr);
        }
    }
    return probabilityStr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.stats.getSuccessStats"></a>[function <span class="apidocSignatureSpan">next-update.stats.</span>getSuccessStats (options)](#apidoc.element.next-update.stats.getSuccessStats)
- description and source-code
```javascript
function getSuccessStats(options) {
    verify.unemptyString(options.name, 'missing name');
    verify.unemptyString(options.from, 'missing from version');
    verify.unemptyString(options.to, 'missing to version');

    verify.webUrl(nextUpdateStatsUrl, 'missing next update stats server url');
    var opts = {
        uri: nextUpdateStatsUrl + '/package/' + options.name + '/' + options.from +
            '/' + options.to,
        method: 'GET',
        json: options
    };
    var defer = Q.defer();
    request(opts, function (err, response, stats) {
        if (err || response.statusCode !== 200) {
            if (response) {
                if (response.statusCode !== 404) {
                    console.error('could not get success stats for', options.name);
                    console.error(opts);
                }
                console.error('response status:', response.statusCode);
            }
            if (err) {
                console.error(err);
            }
            defer.reject(err);
            return;
        }
        defer.resolve(stats);
    });
    return defer.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.stats.printStats"></a>[function <span class="apidocSignatureSpan">next-update.stats.</span>printStats (options, stats)](#apidoc.element.next-update.stats.printStats)
- description and source-code
```javascript
function printStats(options, stats) {
    verify.object(stats, 'missing stats object');
    verify.unemptyString(stats.name, 'missing name');
    verify.unemptyString(stats.from, 'missing from version');
    verify.unemptyString(stats.to, 'missing to version');
    stats.success = +stats.success || 0;
    stats.failure = +stats.failure || 0;
    var total = stats.success + stats.failure;
    var probability = (total > 0 ? stats.success / total: 0);
    var probabilityStr = colorProbability(probability, options);
    console.log('stats:', stats.name, stats.from, '->', stats.to,
        'success probability', probabilityStr,
        stats.success, 'success(es)', stats.failure, 'failure(s)');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.next-update.stats.sendUpdateResult"></a>[function <span class="apidocSignatureSpan">next-update.stats.</span>sendUpdateResult (options)](#apidoc.element.next-update.stats.sendUpdateResult)
- description and source-code
```javascript
function sendUpdateResult(options) {
    verify.unemptyString(options.name, 'missing name');
    verify.unemptyString(options.from, 'missing from version');
    verify.unemptyString(options.to, 'missing to version');
    if (options.success) {
        options.success = !!options.success;
    }

    verify.webUrl(nextUpdateStatsUrl, 'missing next update stats server url');
    var sendOptions = {
        uri: nextUpdateStatsUrl + '/update',
        method: 'POST',
        json: options
    };
    request(sendOptions, function ignoreResponse() {});
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
