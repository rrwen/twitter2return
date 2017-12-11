# twitter2return

Richard Wen  
rrwen.dev@gmail.com  

* [Documentation](https://rrwen.github.io/twitter2return)

Module for extracting Twitter data using option objects

[![npm version](https://badge.fury.io/js/twitter2return.svg)](https://badge.fury.io/js/twitter2return)
[![Build Status](https://travis-ci.org/rrwen/twitter2return.svg?branch=master)](https://travis-ci.org/rrwen/twitter2return)
[![npm](https://img.shields.io/npm/dt/twitter2return.svg)](https://www.npmjs.com/package/twitter2return)
[![GitHub license](https://img.shields.io/github/license/rrwen/twitter2return.svg)](https://github.com/rrwen/twitter2return/blob/master/LICENSE)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/rrwen/twitter2return.svg?style=social)](https://twitter.com/intent/tweet?text=Module%20for%20extracting%20Twitter%20data%20using%20option%20objects:%20https%3A%2F%2Fgithub.com%2Frrwen%2Ftwitter2return%20%23nodejs%20%23npm)

## Install

1. Install [Node.js](https://nodejs.org/en/)
2. Install [twitter2return](https://www.npmjs.com/package/twitter2return) via `npm`

```
npm install --save twitter2return
```

For the latest developer version, see [Developer Install](#developer-install).

## Usage

It is recommended to use a `.env` file at the root of your project directory with the following contents:

* Obtain the keys below from https://apps.twitter.com/
* `TWITTER_CONSUMER_KEY`:
* `TWITTER_CONSUMER_SECRET`:
*` TWITTER_ACCESS_TOKEN_KEY`:
* `TWITTER_ACCESS_TOKEN_SECRET`=***

```
TWITTER_CONSUMER_KEY=***
TWITTER_CONSUMER_SECRET=***
TWITTER_ACCESS_TOKEN_KEY=***
TWITTER_ACCESS_TOKEN_SECRET=***
```

The environmental variables defined above can then be loaded into your script by using [dotenv](https://www.npmjs.com/package/dotenv) (`npm install --save dotenv`):

```
require('dotenv').config();
```

See [Documentation](https://rrwen.github.io/twitter2return) for more details.

### REST API

```
var twitter2return = require('twitter2return');
```

## Contributions

### Report Contributions

Reports for issues and suggestions can be made using the [issue submission](https://github.com/rrwen/twitter2return/issues) interface.

When possible, ensure that your submission is:

* **Descriptive**: has informative title, explanations, and screenshots
* **Specific**: has details of environment (such as operating system and hardware) and software used
* **Reproducible**: has steps, code, and examples to reproduce the issue

### Code Contributions

Code contributions are submitted via [pull requests](https://help.github.com/articles/about-pull-requests/):

1. Ensure that you pass the [Tests](#tests)
2. Create a new [pull request](https://github.com/rrwen/twitter2return/pulls)
3. Provide an explanation of the changes

A template of the code contribution explanation is provided below:

```
## Purpose

The purpose can mention goals that include fixes to bugs, addition of features, and other improvements, etc.

## Description

The description is a short summary of the changes made such as improved speeds or features, and implementation details.

## Changes

The changes are a list of general edits made to the files and their respective components.
* `file_path1`:
	* `function_module_etc`: changed loop to map
	* `function_module_etc`: changed variable value
* `file_path2`:
	* `function_module_etc`: changed loop to map
	* `function_module_etc`: changed variable value

## Notes

The notes provide any additional text that do not fit into the above sections.
```

For more information, see [Developer Install](#developer-install) and [Implementation](#implementation).

## Developer Notes

### Developer Install

Install the latest developer version with `npm` from github:

```
npm install git+https://github.com/rrwen/twitter2return
```
  
Install from `git` cloned source:

1. Ensure [git](https://git-scm.com/) is installed
2. Clone into current path
3. Install via `npm`

```
git clone https://github.com/rrwen/twitter2return
cd twitter2return
npm install
```

### Tests

1. Clone into current path `git clone https://github.com/rrwen/twitter2return`
2. Enter into folder `cd twitter2return`
3. Ensure [devDependencies](https://docs.npmjs.com/files/package.json#devdependencies) are installed and available
4. Run tests with a `.env` file (see [tests/README.md](tests/README.md))
5. Results are saved to [tests/log](tests/log) with each file corresponding to a version tested

```
npm install
npm test
```

### Documentation

Use [documentationjs](https://www.npmjs.com/package/documentation) to generate html documentation in the `docs` folder:

```
npm run docs
```

See [JSDoc style](http://usejsdoc.org/) for formatting syntax.

### Upload to Github

1. Ensure [git](https://git-scm.com/) is installed
2. Inside the `twitter2return` folder, add all files and commit changes
3. Push to github

```
git add .
git commit -a -m "Generic update"
git push
```

### Upload to npm

1. Update the version in `package.json`
2. Run tests and check for OK status  (see [tests/README.md](tests/README.md))
3. Generate documentation
4. Login to npm
5. Publish to npm

```
npm test
npm run docs
npm login
npm publish
```

### Implementation

The module [twitter2return](https://www.npmjs.com/package/twitter2return) uses the following [npm](https://www.npmjs.com/) packages for its implementation:

npm | Purpose
--- | ---
[twitter](https://www.npmjs.com/package/twitter) | Connections to the Twitter API REST and Streaming Application Programming Interfaces (APIs)
[jsonata](https://www.npmjs.com/package/jsonata) | Query language to filter Twitter JSON data

```
twitter   <-- Extract Twitter data from API
    |
jsonata   <-- Filter Twitter JSON data
```
