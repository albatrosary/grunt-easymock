# grunt-easymock

[node-easymock](https://npmjs.org/package/easymock) for Grunt.

## Note

*This plugin is Experimental*.
Because grunt-easymock use forked grunt-easymock. ([Pull Request](https://github.com/CyberAgent/node-easymock/pull/19))

## Getting Started
This plugin requires Grunt `~0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-easymock --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-easymock');
```

## Documentation

Add the task config to the grunt initConfig.

```js
grunt.initConfig({
  easymock: {
    api1: {
      options: {
        port: 30000,
        path: 'easymock/api1',
        config: {
          routes: [
            "/users/:id",
          ],
        },
      },
    },
    api2: {
      options: {
        keepalive: true,
        port: 30010,
        path: 'easymock/api2',
      },
    },
  },
})
```

### Options

#### options.keepalive
-Type: `Boolean`
-Default: `false`

Keep the easymock server alive indefinitely. Note that if this option is enabled, any tasks specified after this task will never run. By default, once grunt's tasks have completed, the web server stops. This option changes that behavior.

#### options.config
-Type: `Object` or `String`

Specifiy config.json's path or config.json's value(object).

#### other options

Other optoins will be passed to easymock server.
See easymock [document](https://npmjs.org/package/easymock)

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History

* 2013-12-08   v0.0.1  Initial release, not yet officially released.
* 2013-12-17   v0.0.2  Removed unnecessary files. use Cyberagent/node-easymock#develop
