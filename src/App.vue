<template>
  <div id="app">
    <div class="row screen d-flex">
      <div class="col-10">
        <screen></screen>
        <stats></stats>
      </div>
      <div class="col flex-row justify-content-between">
        <character class="row"></character>
        <items class="row"></items>
        <superSayan class="row"></superSayan>
      </div>
    </div>
  </div>
</template>

<script>
import screen from "./components/screen.vue";
import equips from "./components/equips.vue";
import items from "./components/items.vue";
import stats from "./components/stats.vue";
import character from "./components/character.vue";
import superSayan from "./components/superSayan.vue";

export default {
  name: "app",
  components: {
    screen,
    equips,
    items,
    stats,
    character,
    superSayan,
  }
};
</script>

<style>
#app {
  height: 900px;
}

.screen{
  height: 100%;
  width: 100%;
}

</style>
