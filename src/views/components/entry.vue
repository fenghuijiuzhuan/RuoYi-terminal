<!--
 * @path        : \RuoYi-terminal\src\views\components\entry.vue
 * @message     : 
 * @Author      : yvangod
-->
<template>
  <div class="entry-container">
    <div class="entrys-wrap">
      <template v-for="(item, index) in pageList">
        <div
          class="entry"
          :key="item.path + index"
          v-if="item.path !== $route.path"
          @click="handleEntry(item)"
        >
          <p class="title">{{ item.meta.title }}</p>
          <p class="tip" v-html="item.tipText"></p>
        </div>
      </template>
    </div>
  </div>
</template>

<script>
export default {
  name: "entry-container",
  props: {
    pageList: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    handleEntry(item) {
      this.$router.push({ path: item.path });
    },
  },
};
</script>

<style scoped lang="scss">
.entry-container {
  width: 100%;
  height: 100%;
  .entrys-wrap {
    padding: 100px;
    width: 100%;
    height: 100%;
    overflow: auto;
    display: flex;
    justify-content: space-around;
    flex-flow: wrap;
  }
  .entry {
    width: 16%;
    min-width: 180px;
    height: 250px;
    margin: 0 30px 40px;
    background-color: #0080ff;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    color: #fff;
    font-weight: 500;
    border-radius: 10px;
  }
  .title {
    font-size: 22px;
  }
  .tip {
    font-size: 14px;
  }
}
</style>
