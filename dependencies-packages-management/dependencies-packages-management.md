# Chapter: Dependencies / Package Management

This section covers aspects of managing code & depaendencies in JS ecosystem. As in the previous section we have talked about it. With the introduction of node.js, it brings in the most important & missing feature of packaging JS code & exporting, sharing it effectively.

Legacy way of shipping javascript libraries is to deploy a minified version over some content delivery network and add in your code HTML using script tag's. which pulls the javascript file on the fly whenever we hit the page. Which is still validate way of pulling dependencies. As the code base grows. We might have somewhere around 10-30 script tag's in our code, pulling content from your server with specific version or refers to library content from the global content delivery network.

Managing a large code base in this maner and sharing multiple packages is a tedious process. It is not just about sharing, but when we ship code content at client side, we are sending entire javascript file which might content unused code, over the cost of performance & network.

**We need solution which provide:**

* A way to manage dependencies & versions.
* Ship minified & optimized code.
* Delivery only want is needed.
* Standard mechanism followed across the community.

Community comes with a standard pattern to match above points called as '**Modules**'. It is a design pattern which provide code isolation and re-usability. Although, module is not a reserved keyword that is defined by javascript compiler/browser js engine. Module terms comes into picture with implmentation like Asynchronous Module Definition \(AMD\) is the most popular for client-side and node.js \(an extension to CommonJS/RequireJS\) as server-side.

If you type keyword module inside Node.js:

```text
> module
Module {
  id: '<repl>',
  exports: {},
  parent: undefined,
  filename: null,
  loaded: false,
  children: [],
  paths: 
   [ '/home/usernamerepl/node_modules',
     '/home/akoserwa/node_modules',
     ..
     '/node_modules',
  ' ] }
```

You can see module is of a type 'object' defined with specific properties.

There is alot of engineering done around the term 'module' and mechanism to ship it. We are going to see following widely adopted implementations:

* npm
* yarn
* bower
* elm-packages

