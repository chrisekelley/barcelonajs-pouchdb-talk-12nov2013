# Using PouchDB for PhoneGap/Cordova apps

This talk will focus on my experiences deploying Android apps that sync with CouchDB. I will focus mostly on PouchDB
but will also discuss the other frameworks I have been using to deploy Android applications (Backbone.js, Coconut, GCM/Urban Airship, PhoneGap/Cordova).

> Under Construction.

> A [Bespoke.js](http://markdalgleish.com/projects/bespoke.js) presentation, built with [generator-bespoke](https://github.com/markdalgleish/generator-bespoke)

## View slides locally

First, ensure you have the following installed:

1. [Node.js](http://nodejs.org)
2. [Bower](http://bower.io): `$ npm install -g bower`
3. [Grunt](http://gruntjs.com): `$ npm install -g grunt-cli`

Then, install dependencies and run the preview server:

```bash
$ npm install && bower install
$ grunt server
```

## To deploy to github-pages:

https://github.com/weavejester/codox/wiki/Deploying-to-GitHub-Pages

Inside your project directory, run the following commands:

    rm -rf public && mkdir public
    git clone git@github.com:chrisekelley/barcelonajs-pouchdb-talk-12nov2013.git public
    cd public
    git symbolic-ref HEAD refs/heads/gh-pages
    rm .git/index
    git clean -fdx
    cd ..
Build your documentation

    grunt server

To publish your docs to Github Pages, run the following commands:

    cd public
    git checkout gh-pages # To be sure you're on the right branch
    git add .
    git commit -am "updated ...."
    git push -u origin gh-pages
    cd ..

For subsequent updates,

    cd public
    git add index.html
    git commit -am "updated ...."
    git push -u origin gh-pages
