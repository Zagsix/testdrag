<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <drop-list :items="items">
      <template v-slot:item="{ item }">
        <drag>
          <div class="drag">
            {{ item.title }}
          </div>
        </drag>
      </template>
    </drop-list>
  </div>
</template>

<script>
import DropList from "./components/DropList";
import Drag from "./components/Drag";

export default {
  name: "App",
  components: { DropList, Drag },
  data: () => {
    return {
      items: [
        { id: 1, title: "Adasd" },
        { id: 2, title: "Adasd asd" },
        { id: 3, title: "Adasd asd" },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.drag {
  cursor: grab;
  padding: 5px;
  border: 1px solid;
  margin: 4px;
}
</style>
