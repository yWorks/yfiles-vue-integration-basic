<template>
  <!-- a container that is used by yFiles -->
  <div id="graph-component"></div>
</template>

<script>
  import { GraphComponent, GraphEditorInputMode, License, Point, Rect } from 'yfiles'
  import licenseData from '../license.json'

  License.value = licenseData

  export default {
    name: 'GraphComponent',
    mounted() {
      // instantiate a new GraphComponent
      this.graphComponent = new GraphComponent('#graph-component')

      // configure an input mode for out of the box editing
      this.graphComponent.inputMode = new GraphEditorInputMode()

      // create some graph elements
      this.createSampleGraph(this.graphComponent.graph)

      // center the newly created graph
      this.graphComponent.fitGraphBounds()
    },
    methods: {
      createSampleGraph(graph) {
        // create some nodes
        const node1 = graph.createNodeAt(new Point(30, 30))
        const node2 = graph.createNodeAt(new Point(150, 30))
        const node3 = graph.createNode(new Rect(230, 200, 60, 30))

        // create some edges between the nodes
        graph.createEdge(node1, node2)
        graph.createEdge(node1, node3)
        const edge = graph.createEdge(node2, node3)
        // Creates the first bend for edge at (260, 30)
        graph.addBend(edge, new Point(260, 30))

        // add labels to some graph elements
        graph.addLabel(node1, 'n1')
        graph.addLabel(node2, 'n2')
        graph.addLabel(node3, 'n3')
      }
    }
  }
</script>

<style scoped>
/* yfiles.css is an integral part of the library and must be loaded wherever a yFiles GraphComponent is created */
@import '~yfiles/yfiles.css';

#graph-component {
  width: 500px;
  height: 500px;
  border: 2px solid #2c3e50;
  border-radius: 5px;
}
</style>
