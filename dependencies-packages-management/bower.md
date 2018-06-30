# Bower

It is a cli tool based on npm for managing component like HTML, JS, CSS and fonts. It gives you flexibility to manage your dependencies without diving into node modules complexities keep an abstraction over it.

Installation is easy:

```text
npm install -g bower
```

It requires: node, npm and git.

For other languages/environments:

* [Ruby on Rails](https://bower.io/docs/tools/#rails--ruby)
* [Java](https://bower.io/docs/tools/#java)
* [Django](https://github.com/nvbn/django-bower)

it has similar way to manage componets like npm does using package.json file, it uses file called bower.json.

Adding library

```text
bower install library
```

And you can direclty refer like

```text
<script src="bower_components/lib_folder/lib.js"></script>
```

For any kind of minification or ugilify it. you need to use it with build tools like

gulp, grunt and webpack.

We will look about them in Build-Tools section.

