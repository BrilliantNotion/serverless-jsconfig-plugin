Serverless JS Config Plugin
===



**Note:** Requires Serverless v0.5.0 or higher.

Setup
===

* Install via npm in the root of your Serverless Project:
```
npm install serverless-jsconfig-plugin --save
```

* Add the plugin to the `plugins` array in your Serverless Project's `s-project.json`, like this:

```
plugins: [
    "serverless-jsconfig-plugin"
]
```

* Enter your project folder and use the following command to build all assets:

```
sls jsconfig build
```

* All done!

