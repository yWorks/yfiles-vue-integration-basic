<img src="./src/assets/yfiles-logo.svg" alt="yFiles logo" height="100"/>

# yFiles integration for create-vue

This sample application serves as a basic scaffold of how to integrate [yFiles for HTML](https://www.yworks.com/products/yfiles-for-html) in a [create-vue](https://vuejs.org/guide/quick-start.html#with-build-tools) application.

**To run this project, a valid [yFiles for HTML](https://www.yworks.com/products/yfiles-for-html) version is required. You can evaluate yFiles 60 days free of charge on [my.yworks.com](https://my.yworks.com/signup?product=YFILES_HTML_EVAL).**

## Version Information

- create-vue v3.3
- yFiles for HTML 2.6

## Getting Started

Just clone this repository with

```
git clone https://github.com/yWorks/yfiles-vue-integration-basic
```

Then, extract a yFiles Evaluation package beside it and run

```
npm install
```

You can serve the application on [http://localhost:5173/](http://localhost:5173/) with

```
npm run dev
```

## Under the Hood

This project is a basic create-vue application, where yFiles was added as an additional dependency to integrate a basic graph component.

A step-by-step description of how to integrate yFiles in a Vue application can be found [here](integration-howto.md).

## What's Next?

This basic yFiles integration can be used as a starting point to test the capabilities of yFiles or to implement your own use case. yFiles for HTML comes with a lot of [source-code demos](https://www.yworks.com/demos) that show different aspects of the library.

You can browse through the demos and look for features that you find interesting for your use case and integrate it in this basic component to build a more sophisticated application.

The yFiles package also contains a more extensive [Vue integration demo](https://www.yworks.com/demos/toolkit/vue/) ([GitHub](https://github.com/yWorks/yfiles-for-html-demos/blob/master/demos/toolkit/vue)), as well as a specialized [Vue.js Template Node Style](https://www.yworks.com/demos/style/vue-template-node-style/) ([GitHub](https://github.com/yWorks/yfiles-for-html-demos/tree/master/demos/style/vue-template-node-style)) that leverages the powerful data binding and conditional rendering features of Vue.js.

Furthermore, there is an extensive [Developer's Guide](https://docs.yworks.com/yfileshtml/#/dguide/introduction#top) that covers anything from graph creation and styling to automatic layouts and advanced customizations.

## Create a Diagram Application with Vue

The [App Generator](https://www.yworks.com/products/app-generator) is a tool that lets you interactively create a diagram
application prototype to visualize your data. Select features like editing, context menu, graph search, or printing
and customize the interaction with the graph. Generate Vue code for your prototype and use it with a valid
[yFiles for HTML](https://www.yworks.com/products/yfiles-for-html) version.

## Support

If you need help with your setup or a certain feature, don't hesitate to contact our support through
the [Customer Center](https://my.yworks.com/) or by email [yfileshtml@yworks.com](mailto:yfileshtml@yworks.com).
