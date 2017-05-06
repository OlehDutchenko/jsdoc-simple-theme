# jsdoc-simple-theme

![jsdoc3 theme](https://img.shields.io/badge/JSDoc3-theme-blue.svg)
![license](https://img.shields.io/badge/License-MIT-orange.svg)

Simple theme for [gulp-jsdoc3](https://www.npmjs.com/package/gulp-jsdoc3) and [jsdoc](https://www.npmjs.com/package/jsdoc) also.

Less words, better look at these demo screenshots

[![screen-1](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-1.jpg)](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-1.jpg)

[![screen-2](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-2.jpg)](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-2.jpg)

[![screen-3](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-3.jpg)](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-3.jpg)

[![screen-4](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-4.jpg)](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-4.jpg)

[![screen-5](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-5.jpg)](https://github.com/dutchenkoOleg/jsdoc-simple-theme/blob/master/assets/screen-5.jpg)



## Installing

```shell
npm install --save jsdoc-simple-theme
# or using yarn cli
yarn add jsdoc-simple-theme
```

#### includes

- [jsdoc-ignore-code](https://www.npmjs.com/package/jsdoc-ignore-code)
- [jsdoc-sourcecode-tag](https://www.npmjs.com/package/jsdoc-sourcecode-tag)
- [jsdoc-export-default-interop](https://www.npmjs.com/package/jsdoc-export-default-interop)

## Code Syntax Highlight

[prismjs](http://prismjs.com/)

- all languages - http://prismjs.com/index.html#languages-list
- all plugins (http://prismjs.com/index.html#plugins), except _WebPlatform Docs_ and _Show Invisibles_

## Usage

Add theme and plugins to jsdoc conf.json (http://usejsdoc.org/about-configuring-jsdoc.html)

- opts > template
- templates > default > layoutFile

```json
{
	"source": {
		"includePattern": ".+\\.js(doc|x)?$",
		"excludePattern": "(^|\\/|\\\\)_"
	},
	"tags": {
		"allowUnknownTags": true,
		"dictionaries": [
			"jsdoc",
			"closure"
		]
	},
	"opts": {
		"template": "./node_modules/jsdoc-simple-theme/"
	},
	"plugins": [
		"plugins/markdown",
		"./node_modules/jsdoc-export-default-interop/dist/index",
		"./node_modules/jsdoc-ignore-code/index",
		"./node_modules/jsdoc-sourcecode-tag/index"
	],
	"markdown": {
		"parser": "gfm",
		"hardwrap": true
	},
	"templates": {
		"cleverLinks": false,
		"monospaceLinks": false,
		"default": {
			"outputSourceFiles": true,
			"layoutFile": "./node_modules/jsdoc-simple-theme/tmpl/layout.tmpl"
		}
	}
}
```



## Changelog