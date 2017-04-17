# api documentation for  [contra (v1.9.4)](https://github.com/bevacqua/contra)  [![npm package](https://img.shields.io/npm/v/npmdoc-contra.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-contra) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-contra.svg)](https://travis-ci.org/npmdoc/node-npmdoc-contra)
#### Asynchronous flow control with a functional taste to it

[![NPM](https://nodei.co/npm/contra.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/contra)

- [https://npmdoc.github.io/node-npmdoc-contra/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-contra/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-contra/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-contra/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-contra/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-contra/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nicolas Bevacqua",
        "url": "http://bevacqua.io"
    },
    "bugs": {
        "url": "https://github.com/bevacqua/contra/issues"
    },
    "dependencies": {
        "atoa": "1.0.0",
        "ticky": "1.0.1"
    },
    "description": "Asynchronous flow control with a functional taste to it",
    "devDependencies": {
        "assert": "~1.1.0",
        "browserify": "10.2.4",
        "jshint": "~2.4.1",
        "jshint-stylish": "~0.1.5",
        "jshint-tap": "0.0.1",
        "mocha": "~1.17.0",
        "uglify-js": "2.4.23"
    },
    "directories": {},
    "dist": {
        "shasum": "f53bde42d7e5b5985cae4d99a8d610526de8f28d",
        "tarball": "https://registry.npmjs.org/contra/-/contra-1.9.4.tgz"
    },
    "gitHead": "661cc16335ea6cf91f16965bea4c8930c09b2f2a",
    "homepage": "https://github.com/bevacqua/contra",
    "keywords": [
        "a",
        "async",
        "asynchronous",
        "control",
        "flow",
        "generator",
        "promises",
        "q"
    ],
    "license": "MIT",
    "main": "contra.js",
    "maintainers": [
        {
            "name": "bevacqua"
        }
    ],
    "name": "contra",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/bevacqua/contra.git"
    },
    "scripts": {
        "build": "browserify -s contra -do dist/contra.js contra.js && uglifyjs -m -c -o dist/contra.min.js dist/contra.js",
        "build-shim": "browserify -do dist/contra.shim.js contra.shim.js && uglifyjs -m -c -o dist/contra.shim.min.js dist/contra.shim.js",
        "deploy": "npm run build && npm run build-shim && npm run test && npm run deployment",
        "deployment": "git add dist && npm version ${BUMP:-\"patch\"} --no-git-tag-version && git add package.json && git commit -am \"Autogenerated pre-deployment commit\" && bower version ${BUMP:-\"patch\"} && git reset HEAD~2 && git add . && git commit -am \"Release $(cat package.json | jq -r .version)\" && git push --tags && npm publish && git push",
        "test": "mocha --reporter tap && jshint --reporter node_modules/jshint-tap/jshint-tap.js test/*.js"
    },
    "testling": {
        "browsers": {
            "android-browser": [
                4.2
            ],
            "chrome": [
                15,
                20,
                25,
                30,
                5,
                "canary"
            ],
            "firefox": [
                10,
                15,
                20,
                25,
                3.6,
                "nightly"
            ],
            "ie": [
                10,
                6,
                7,
                8,
                9
            ],
            "ipad": [
                6
            ],
            "iphone": [
                6
            ],
            "opera": [
                15,
                16,
                17,
                "next"
            ],
            "safari": [
                4,
                5.1,
                6
            ]
        },
        "files": [
            "contra.js",
            "contra.shim.js",
            "test/*.js"
        ],
        "harness": "mocha"
    },
    "version": "1.9.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
