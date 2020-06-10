<img src="./src/assets/yfiles-logo.svg" alt="yFiles logo" height="100"/>

# yFiles integration for Vue CLI

This sample application serves as a basic scaffold of how to integrate [yFiles for HTML](https://www.yworks.com/products/yfiles-for-html) in a [Vue CLI](https://cli.vuejs.org/) application.

**To run this project, a valid [yFiles for HTML](https://www.yworks.com/products/yfiles-for-html) version is required. You can evaluate yFiles 60 days free of charge on [my.yworks.com](https://my.yworks.com/signup?product=YFILES_HTML_EVAL).**

## Version Information

- Vue CLI v4.4.1
- yFiles for HTML 2.3

## Getting Started

Just clone this repository with

```
git clone https://github.com/yWorks/yfiles-vue-integration-basic
```

Then, extract a yFiles Evaluation package beside it and run

```
npm install
```

You can serve the application on [http://localhost:8080/](http://localhost:8080/) with

```
npm run serve
```

## Under the Hood

This project is a default Vue CLI application, where yFiles was added as an additional dependency to integrate a basic graph component.

A step-by-step description of how to integrate yFiles in a Vue application can be found [here](integration-howto.md).

## What's Next?

This basic yFiles integration can be used as a starting point to test the capabilities of yFiles or to implement your own use case. yFiles for HTML comes with a lot of [source-code demos](https://live.yworks.com/demos/index.html) that show different aspects of the library.

You can browse through the demos and look for features that you find interesting for your use case and integrate it in this basic component to build a more sophisticated application.

The yFiles package also contains a bigger [Vue.js integration demo](https://live.yworks.com/demos/toolkit/vuejs/index.html) ([GitHub](https://github.com/yWorks/yfiles-for-html-demos/blob/master/demos/toolkit/vuejs)) and another [Vue CLI demo](https://live.yworks.com/demos/toolkit/vue-cli/index.html) ([GitHub](https://github.com/yWorks/yfiles-for-html-demos/tree/master/demos/toolkit/vue-cli)), as well as a specialized [Vue.js Template Node Style](https://live.yworks.com/demos/style/vuejstemplatenodestyle/index.html) ([GitHub](https://github.com/yWorks/yfiles-for-html-demos/tree/master/demos/style/vuejstemplatenodestyle)) that leverages the powerful data binding and conditional rendering features of Vue.js.

Furthermore, there is an extensive [Developer's Guide](https://docs.yworks.com/yfileshtml/#/dguide/introduction#top) that covers anything from graph creation and styling to automatic layouts and advanced customizations.

## Support

If you need help with your setup or a certain feature, don't hesitate to contact our support
through the [Customer Center](https://my.yworks.com/) or by email [yfileshtml@yworks.com](mailto:yfileshtml@yworks.com).
