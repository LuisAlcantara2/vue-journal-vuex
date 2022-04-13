<template>
  <div class="entry-list-container">
    <div class="px-2 pt-2">
      <input type="text" class="form-control" placeholder="Buscar">
    </div>
    <div class="entry-scrollarea">
      <h2 v-for="item in 100" :key="item">
        <Entry></Entry>
      </h2>
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from '@vue/runtime-core'
export default {
  components: {
    Entry: defineAsyncComponent(() => import('../components/Entry.vue'))
  },
}
</script>

<style lang="scss" scoped>
.entry-list-container {
  height: calc(100vh - 56px);
  border-right: 1px solid #2c3e50;
}
.entry-scrollarea {
  height: calc(100vh - 110px);
  overflow-y: scroll;
}
</style>>
