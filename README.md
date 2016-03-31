Serverless JS Config Plugin
===

[![serverless](http://public.serverless.com/badges/v3.svg)](http://www.serverless.com)
[![npm version](https://badge.fury.io/js/serverless-jsconfig-plugin.svg)](https://badge.fury.io/js/serverless-jsconfig-plugin)

Allows the use of JS based files within the project for configuration. These JS files are then compiled into JSON files for use natively by the Serverless Framework.

**Note:** Requires Serverless v0.5.0 or higher.

Setup
---

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

* Edit your JS config files as needed. When you are done with your modification, run the following command to build them into JSON files:

```
sls jsconfig build -o
```

* All done!

Common Pitfalls
---

### Chicken Egg Problem

Serverless still requires all JSON files to be present to operate. If you remove the JSON files from your project, then serverless will no longer run correctly. This also means the JS Config plug will also stop functioning, and you will not be able to rebuild the JSON files.

**DO NOT REMOVE YOUR JSON FILES!**
