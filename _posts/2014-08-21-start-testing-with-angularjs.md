---
layout: post
title: "Start Testing with Angular JS"
category: "App Development"
tags: [angular, yeoman, grunt, testing]
author: ismail
---

As widely known, Angular JS is saving our lives with its practical and yet powerful functionalities. And, test driven development with Angular JS is a dream already came true. Angular JS with its sophisticated dependency injection, module structure and plain old Javascript object models is so easy to code, maintain and test.

###Let's Get Started

[Yeoman](http://yeoman.io) is a workflow scaffolder to create webapps with well known best practices. Yeoman works with generators published out there via [npm](https://www.npmjs.org/search?q=yeoman+generator).

Yeoman makes easy creating an angular app ready to testing by scaffolding via generators. To install Yeoman run the command below (after installing [node](http://nodejs.org) and npm)

{% highlight bash %}
$ npm install -g yeoman
{% endhighlight %}
  
  
###Scaffold Angular JS App

First let's install Angular generator.

{% highlight bash %}
$ npm install -g generator-angular
{% endhighlight %}

Then create a project directory in your workspace
{% highlight bash %}
$ mkdir angular-karma
{% endhighlight %}

Inside the created directory scaffold your app
{% highlight bash %}
$ yo angular
{% endhighlight %}

Following the instructions you can choose additional libraries such as Bootstrap, angular-route or angular-sanitize modules and sass. This command generates the required source files, creates a grunt file with tasks; installs required node modules, runs tasks, installs bower components and makes app ready.

###Tests
There is a test file for the Main controller under `test/spec` directory. This test ensures a model in the controller, `awesomeThings` has 3 objects.

To run tests with Jasmine install it via `npm install karma-jasmine --save-dev`.

To run written tests under `test` directory, run `grunt test` command. This command runs tests in your app through karma with Jasmine. You probably will need to launch a browser and visit karma server most likely running on `localhost:8080` manually. This process can also be automated by installing a karma browser launcher. It's best to install Phantom Js launcher since Phantom is headless webkit intended for tests. To install a launcher you can run one of these commands:

{% highlight bash %}
$ npm install karma-phantomjs-launcher --save-dev
$ npm install karma-firefox-launcher --save-dev
$ npm install karma-chrome-launcher --save-dev
{% endhighlight %}

You can set which browser to be launched on `karma.conf.js` within this line: `browsers: ['PhantomJS']`.

###Further
Yeoman Angular generator promises much more than these. There are plenty of [sub-generators](https://github.com/yeoman/generator-angular#generators) available within this generator.

For example, running `yo angular:route user` generates a controller on `/app/controllers/user.js` with name `UserCtrl`, a view under `/app/views/user.html` and a unit test on `/test/spec/controllers/main.js`. Also adds route configurations to `/app/scripts/app.js`.

You can visit [project page](https://github.com/yeoman/generator-angular#angularjs-generator-) for documentation.
