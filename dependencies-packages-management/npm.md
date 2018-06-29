---
description: Node Package Manager
---

# npm

it is originated as a open source project for mange/package Node.js modules in 2009. It is a public registry allow to publish packages, download and provides a command line utility to interact with the registry & uses a standard JSON file named as 'package.json' to manage metadata for a project.

You can initialize a project with npm utility something simliar like 'git init' uitlity.

```text
npm init
```

At a bare minimum, a`package.json`must have:

* `"name"`
  * all lowercase
  * one word, no spaces
  * dashes and underscores allowed
* `"version"`
  * in the form of `x.x.x`
  * follows [semver spec](https://docs.npmjs.com/getting-started/semantic-versioning)

You can install dependencies in an existing project with`npm install.`Refer any module in your javascript file with keyword require.

```text
require('<ModuleName>');
```

You can refer[ npm documentation f](https://docs.npmjs.com/getting-started/what-is-npm)or detailed usage. Here, we are going to talk about a general aspect around it.

If you are doing server-side development or any application which is based on the node.js platform. You just need npm as base utility for manage/package dependencies, execute build, test, serve scripts.

Things get confusing when we are going for frontend development. Remember term **require** is not a recognizable by browser javascript engine. We need a way to use same packaging system for our frontend application as well.

npm is a base utility and required for other tools like browserify, _bower, grunt, gulp, webpack_ etc.

[**browserify**](http://browserify.org/) comes to the rescue and converts your `require('module')` to an optimize code which is recognizable by your browser. Bascially it scan your code for keyword **require** and does static analysis for building a code abstract syntax tree. Few other operations are required for better optimization like:

* Minify/Uglify
* Loadash

**Minify vs Uglify**

Minify: Compression for JS/CSS file by removing whitespace and removing some amout of reduntant code standard code.

Uglify: As name suggest makes your code look ugily but optimized. it will not only compress your code, but optimize variable naming, conditions, discard unused variables/functions. etc. It is not going to change the actual logic or flow of the code but makes it more readable for javascript parser and less readable for humans.

If you don't want to deep dive into complexity of defining your javascript libaries as a node modules and use them in the manner similar to defining script tags. You can pick other solutions like bower/yarn/webpack. Although bower is going away.

