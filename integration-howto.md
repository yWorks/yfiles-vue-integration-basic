# How to integrate yFiles into a Vue application

This is a step-by-step description of how to add a yFiles graph component to a basic Vue application.

TL;DR Add `yfiles` as a dependency in the `package.json`,
[include your license](https://docs.yworks.com/yfileshtml/#/dguide/licensing#_general_concept),
and start importing yFiles classes in your project.

## Create a default create-vue application

At first, create a basic `create-vue` app by running `> npm init vue@latest`, e.g., with
the following options:

- `Project name:` yfiles-vue-integration-basic
- `Add TypeScript?` Yes
- `Add JSX Support?` No
- `Add Vue Router for Single Page Application development?` No
- `Add Pinia for state management?` No
- `Add Vitest for Unit testing?` No
- `Add an End-to-End Testing Solution?` No
- `Add ESLint for code quality?` Yes
- `Add Prettier for code formatting?` No

## Add yFiles as a dependency

Adding yFiles as a dependency is almost as easy as installing an external library from the npm registry:

1. Add yFiles for HTML as npm dependency to the created project, for example, like this:

   ```
   "dependencies": {
     ...
     "yfiles": "../yFiles-for-HTML-Complete-2.6.0.4-Evaluation/lib-dev/yfiles-26.0.4+eval-dev.tgz"
   },
   ```

2. Install the newly added dependency with `npm install`.

3. Include your yFiles license by copying the `license.json` file into your project. For more options,
   see the [developer's guide](https://docs.yworks.com/yfileshtml/#/dguide/licensing#_general_concept)

After installing the dependency, you can import classes from `yfiles` in your project. Since yFiles
is installed as proper npm dependency, IDEs provide full code-completion and automatic imports out
of the box to easily work with the library.

## Integrate a basic yFiles graph component

With the yFiles dependency, you can easily create a new Vue component with a yFiles graph component.

1. Create a new `GraphComponent.vue` file in `/src/components/` which instantiates a new yFiles
   graph component and optionally add an input mode for basic editing and a sample graph.

   See the contents of `/src/components/GraphComponent.vue` in this repository for the implementation.

   Make sure to configure your license data as described above. This project assumes that there is
   a yFiles evaluation package with a license file next to the project's root. Otherwise, you need
   to change the setting of the license data in `GraphComponent.vue`.

2. Add the new Vue component to the `App.vue` that was created by the Vue CLI.

And that's it. Run `npm run dev` to serve the application with a basic yFiles component.

## Development Mode

This project uses the yFiles development library from the yFiles package. The development library
adds additional type runtime checks to yFiles related method calls and yields readable exception
messages to identify problems in JavaScript code more easily.
For more details, see the [Development Mode section](http://docs.yworks.com/yfileshtml/#/dguide/yfiles_development_mode).

Please note that these additional checks slightly affect the performance of the application,
therefore it should only be used during development.
See also [Preparing the Development Mode Library for Production](https://docs.yworks.com/yfileshtml/#/dguide/deployment#dev-deployment)
in Webpack to learn how to switch between development and production mode.
