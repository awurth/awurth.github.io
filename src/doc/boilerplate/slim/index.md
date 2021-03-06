---
title: Installation
type: guide
category: Slim base
order: 1
github: https://github.com/awurth/Slim
---

### Create the project using Composer
``` bash
$ composer create-project awurth/slim-base [project-name]
```

### Setup environment variables

Copy `.env.dist` to a `.env` file and change the values to your needs. This file is ignored by Git so all developers working on the project can have their own configuration.

## Download client-side libraries
``` bash
$ npm install
```
This will install Gulp dependencies, and Semantic UI in `public/assets/lib/semantic/`.

### Gulp
This skeleton uses Gulp to manage assets. The CSS and Javascript files are located in `assets/`, so you have to use Gulp after creating your project to generate the minified files in `public/`, which will be ignored by Git.

### Install Gulp
You can install Gulp globally on your system with the following command if you haven't done it yet
``` bash
$ npm install -g gulp-cli
```

### Generate assets
If you just want to generate the default CSS and JS that comes with this skeleton, run the following command
``` bash
$ gulp build
```

If you want to run a watcher and begin coding, just run
``` bash
$ gulp
```

### Setup cache files permissions
The skeleton uses a cache system for Twig templates and the Monolog library for logging, so you have to make sure that PHP has write permissions on the `var/cache/` and `var/log/` directories.

### Update your database schema
First, create a database with the name you set in the `.env` file. Then you can create the tables by running this command:
``` bash
$ php bin/console db
```

If you're using [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh), you can install the symfony2 plugin, which provides an alias and autocompletion:
``` bash
# Without Symfony2 plugin
$ php bin/console db

# With Symfony2 plugin
$ sf db
```
