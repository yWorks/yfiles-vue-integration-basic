<script setup lang="ts">
import { ref, onUnmounted, onMounted } from 'vue'
import { GraphComponent, GraphEditorInputMode, IGraph, License, Point, Rect } from 'yfiles'
import licenseData from '../license.json'

License.value = licenseData

const gcContainer = ref(null)

const graphComponent = initializeGraphComponent()
graphComponent.inputMode = new GraphEditorInputMode()

onMounted(() => {
  ;(gcContainer.value as HTMLDivElement).appendChild(graphComponent.div)
  graphComponent.fitGraphBounds()
})

onUnmounted(() => {
  ;(graphComponent.div.parentElement as HTMLDivElement).removeChild(graphComponent.div)
})

function initializeGraphComponent(): GraphComponent {
  const graphComponent = new GraphComponent()
  // configure an input mode for out of the box editing
  graphComponent.inputMode = new GraphEditorInputMode()
  // create some graph elements
  createSampleGraph(graphComponent.graph)
  return graphComponent
}

function createSampleGraph(graph: IGraph): void {
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
</script>

<template>
  <!-- a container that is used by yFiles -->
  <div class="graph-component" ref="gcContainer"></div>
</template>

<style scoped>
.graph-component {
  width: 500px;
  height: 500px;
  border: 2px solid #2c3e50;
  border-radius: 5px;
}
.graph-component :deep(.yfiles-canvascomponent) {
  width: 100%;
  height: 100%;
}
</style>
