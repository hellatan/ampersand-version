# ampersand-version

* Add ampersand-version to `"dependencies"` in package.json
* Add browserify transform as per below:

```json
{
    "name": "some-ampersand-module",
    "dependencies": {
        "ampersand-version": "^1.0.1"
    },
    "browserify": {
        "transform": ["ampersand-version"]
    }
}
```

* Add `/*$AMPERSAND_VERSION*/` to the top of the module's main file.

## why?

Now it will use a browserify transform to create if necessary and add its version to the `window.ampersand` object just for reporting purposes. 

You can then open the console on any ampersand site and see what ampersand modules it's using:

![ampersand-version-demo](https://i.cloudup.com/B8SuBDceTH-3000x3000.png)


## license

MIT
