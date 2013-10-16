# grunt-git-revision

> Get current Git revision

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-git-revision --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-git-revision');
```

## The "revision" task

### Overview
In your project's Gruntfile, add a section named `revision` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  revision: {
    options: {
      property: 'meta.revision',
      ref: 'HEAD',
      short: true
    }
  },
})
```

### Options

#### options.property
Type: `String`
Default value: `'meta.revision'`

What configuration property to write the revision to.

#### options.ref
Type: `String`
Default value: `'HEAD'`

What ref to read the revision from.

#### options.short
Type: `Boolean`
Default value: `true`

Fetch short revision (e.g 5b8348d) or the full revision (5b8348de6b492ca79e732b1902c489332c8d64fb)

### Usage Examples

```js
grunt.initConfig({
  preprocess: {
    options: {
      context: {
        revision: '<%= meta.revision %>'
      }
    }
  }
})
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
