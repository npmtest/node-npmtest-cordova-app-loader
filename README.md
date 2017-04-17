# test coverage for  cordova-app-loader (v1.0.0)  [![npm package](https://img.shields.io/npm/v/npmtest-cordova-app-loader.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-cordova-app-loader) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-cordova-app-loader.svg)](https://travis-ci.org/npmtest/node-npmtest-cordova-app-loader)
#### Cordova App Loader - remote update your cordova app

[![NPM](https://nodei.co/npm/cordova-app-loader.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/cordova-app-loader)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-cordova-app-loader/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-cordova-app-loader/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-cordova-app-loader/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-cordova-app-loader/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-cordova-app-loader/build/test-report.html](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-cordova-app-loader/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-cordova-app-loader/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-cordova-app-loader/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-cordova-app-loader/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-cordova-app-loader/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Mark Marijnissen"
    },
    "dependencies": {
        "cordova-file-cache": "^1.1.0",
        "cordova-promise-fs": "^1.1.0"
    },
    "description": "Cordova App Loader - remote update your cordova app",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "39f6fdcc82a97149cf19f3c1ec85a1ca04560dbc",
        "tarball": "https://registry.npmjs.org/cordova-app-loader/-/cordova-app-loader-1.0.0.tgz"
    },
    "gitHead": "f4a995ccc2af1d9e9f6c8d22aff1443e5b638fc7",
    "keywords": [
        "cordova",
        "app",
        "loader",
        "remote",
        "update"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "markmarijnissen"
        },
        {
            "name": "objectivetruth"
        }
    ],
    "name": "cordova-app-loader",
    "optionalDependencies": {},
    "scripts": {
        "autoupdate": "cp autoupdate.js www/autoupdate.js",
        "bootstrap": "cp bootstrap.js www/bootstrap.js",
        "bundle": " webpack bundle.js dist/cordova-app-loader-complete.js && cp dist/cordova-app-loader-complete.js www/lib/cordova-app-loader-complete.js",
        "copy-tests": "cp pegasus.js www/test/pegasus.js && cp node_modules/cordova-promise-fs/test/tests.js www/test/cordova-promise-fs-tests.js && cp node_modules/cordova-file-cache/test/tests.js www/test/cordova-file-cache-tests.js",
        "copy-to-dist": "cp www/lib/CordovaAppLoader.js dist/ && cp www/lib/CordovaPromiseFS.js dist/ && cp www/bootstrap.js dist/ && cp www/autoupdate.js dist/",
        "cordova-app-loader": "webpack index.js www/lib/CordovaAppLoader.js --output-library CordovaAppLoader --output-library-target var",
        "cordova-promise-fs": "npm run-script cordova-promise-fs prepublish && cp node_modules/cordova-file-cache/node_modules/cordova-promise-fs/dist/CordovaPromiseFS.js www/lib/CordovaPromiseFS.js",
        "minify-dist": " uglifyjs -c -m --screw-ie8 dist/bootstrap.js -o dist/bootstrap.min.js && uglifyjs -c -m --screw-ie8 dist/autoupdate.js -o dist/autoupdate.min.js && uglifyjs -c -m --screw-ie8 dist/CordovaPromiseFS.js -o dist/CordovaPromiseFS.min.js && uglifyjs -c -m --screw-ie8 dist/CordovaAppLoader.js -o dist/CordovaAppLoader.min.js && uglifyjs -c -m --screw-ie8 dist/cordova-app-loader-complete.js > dist/cordova-app-loader-complete.min.js",
        "prepublish": "npm run copy-tests && npm run autoupdate && npm run bootstrap && npm run cordova-app-loader && npm run copy-to-dist && npm run bundle && npm run minify-dist",
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "version": "1.0.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
