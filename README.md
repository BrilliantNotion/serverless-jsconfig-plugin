Serverless JS Config Plugin
===

Allows the use of JS config files within the project, which are then compiled into JSON files for use by the Serverless Framework.

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

* Enter your project folder and use the following command to create all the JS config files from the existing JSON config files:

```
sls jsconfig convert
```

* Edit your JS config files, then run the following command to build them into JSON files:

```
sls jsconfig build -o
```

* All done!

Common Pitfalls
===

### Chicken Egg Problem

Serverless still requires all JSON files to be present to operate. If you remove the JSON files from your project, then serverless will no longer run correctly. This also means the JS Config plug will also stop functioning, and you will not be able to rebuild the JSON files.

**DO NOT REMOVE YOUR JSON FILES!**
