# HSR.Metristic.Plugin.Web
Metristic web check plugin (HTML, CSS, JavaScript).


## Lisence
![Apache License Version 2.0](https://www.apache.org/img/asf_logo.png)
[Apache License Version 2.0](./LICENSE)


## Releases / Production

⬇ Download on the [Release page](https://github.com/wasabideveloper/HSR.Metristic.Plugin.Web/releases)


## Installation

* Install [node.js](https://nodejs.org/en/)
* Extract archive
* Enter the extracted directory, e.g. `cd Metristic-1.0`.
* Run `npm install --production` to install the dependencies.


## Usage

Import the plugins in the project.js of your main project:
```javascript
"use strict";

var HtmlW3cValidator = require("metristic-plugin-web").HtmlW3cValidator;
var HtmlMetric = require("metristic-plugin-web").HtmlMetric;
var CssMetric = require("metristic-plugin-web").CssMetric;
var JsStyleCheck = require("metristic-plugin-web").JsStyleCheck;

module.exports = {
	...
	
	"webMetrics": {
		name: 'Web project metrics',
		description: 'Show metrics of HTML, CSS',
		checks: [StructureMetric, HtmlMetric, CssMetric],
		options: {}
	},
	"webCheck": {
		name: 'Web project checking',
		description: 'Validate HTML by W3C and check JS code style',
		checks: [StructureMetric, HtmlW3cValidator, JsStyleCheck],
		options: {}
	},
	...
};
```


## How to build the project from source

### Global dependencies

* Node.js / npm
* Typescript Compiler ```npm install tsc --global```
* Typings ```npm install typings --global```

### Installation

* Install global dependencies
* Clone project
* Run `npm install` to install the dependencies.
* Install typings depencency `tsd install`

### Commands

Deploy app to directory `app`:
```shell
gulp deploy
```

Compile TS and run tests:
```shell
gulp test
# or
npm test
```

### Install new type declarations:
```shell
# jasmine example
tsd query jasmine --action install --save
```
