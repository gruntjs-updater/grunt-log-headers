# grunt-log-headers [![NPM Version](http://badge.fury.io/js/grunt-log-headers.svg)](http://badge.fury.io/js/grunt-log-headers)

> Hide the running task name header in Grunt's logger.

## Getting Started
This plugin requires Grunt `~0.4`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-log-headers --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
require('grunt-log-headers')(grunt);
```

## There is no task

### Overview
Unlike typical Grunt plugins, this one has no task. It's actually a hack that wraps a part of Grunt's core.

### Global Options

#### options.gruntLogHeader
Type: `Boolean`  
Default value: `true`  

Show the running task header or not. This can be applied to *any* task.

### Usage Example
```js
module.exports = function(grunt) {
  grunt.initConfig({
    sometask: {
      options: {
        gruntLogHeader: false,
      },
      sometarget1: {
        options: {
          gruntLogHeader: true,
        },
        …
      }
      sometarget2: {
        …
      },
    },
  });
  
  require('grunt-log-headers')(grunt);
  grunt.loadNpmTasks('sometask');
}
```

## Release History
* 1.0.1 package.json fixes
* 1.0.0 release
* 0.1.0 initial release

---

[![Analytics](https://ga-beacon.appspot.com/UA-3614308-12/stevenvachon/grunt-log-headers)](https://github.com/igrigorik/ga-beacon "Google Analytics") [![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/stevenvachon/grunt-log-headers/trend.png)](https://bitdeli.com/free)
