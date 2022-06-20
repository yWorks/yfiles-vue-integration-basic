# How to integrate yFiles into a Vue application

This is a step-by-step description of how to add a yFiles graph component to a basic Vue application.

TL;DR Add yFiles as a dependency in the `package.json` and start importing yFiles classes in your project.

## Create a default Vue CLI application

At first, create a default Vue CLI app by running `> vue create yfiles-vue-integration-basic` with the default option: `default ([Vue 2] babel, eslint)`.

## Add yFiles as a dependency

Adding yFiles as a dependency is as easy as installing an external library from the npm registry:

1. Add yFiles for HTML as npm dependency to the created project:

   - If you have a fresh yFiles for HTML package, you need to prepare the library package first by running `npm install` in the
     package folder. This creates the development library and a tarball that can be installed as npm dependency in
     other projects. See also [Working with the yFiles npm Module](https://docs.yworks.com/yfileshtml/#/dguide/yfiles_npm_module#yfiles_npm_module).

     Note: This sample project runs `npm install` as `preinstall` script in the `package.json`.

   - Reference the packed library in the `package.json` of the project:
     ```
     "dependencies": {
       ...
       "yfiles": "../yFiles-for-HTML-Complete-2.4.0.6-Evaluation/lib-dev/es-modules/yfiles-24.0.6-eval-dev.tgz"
     },
     ```

2. Now install the newly added dependency with `npm install`.

After installing the dependency, you can import classes from `yfiles` in your project. Since yFiles is installed as proper npm dependency, IDEs provide full code-completion and automatic imports out of the box to easily work with the library.

## Integrate a basic yFiles graph component

With the yFiles dependency, you can easily create a new Vue component with a yFiles graph component.

1. Create a new `GraphComponent.vue` file in `/src/components/` which instantiates a new yFiles graph component and optionally add an input mode for basic editing and a sample graph.

   See the contents of `/src/components/GraphComponent.vue` in this repository for the implementation.

   There are two things to look out for:

   - Make sure to configure your `license.json` for the library. This project assumes that there is a yFiles package next to the project's root. Therefore, you may need to change the referenced path in `GraphComponent.vue`.

2. Add the new Vue component to the `App.vue` that was created by the Vue CLI.

And that's it. Run `npm run serve` to serve the application with a basic yFiles component.

## Development Mode

This project uses the yFiles development library from the yFiles package. The development library adds additional
type runtime checks to yFiles related method calls and
yields readable exception messages to identify problems in JavaScript code more easily.
For more details see [Development Mode](http://docs.yworks.com/yfileshtml/#/dguide/yfiles_development_mode).

Please note that these additional checks degrade the performance of the application slightly, therefore it should only be used during development. See also [Preparing the Development Mode Library for Production](https://docs.yworks.com/yfileshtml/#/dguide/deployment#dev-deployment) in Webpack to learn how to switch between development and production mode.
