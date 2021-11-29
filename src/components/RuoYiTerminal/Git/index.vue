<!--
 * @path        : \RuoYi-terminal\src\components\RuoYiTerminal\Git\index.vue
 * @message     : 
 * @Author      : yvangod
-->
<template>
  <div>
    <svg-icon icon-class="github" @click="goto" />
  </div>
</template>

<script>
export default {
  name: 'RuoYiTerminalGit',
  data() {
    return {
      // url: 'https://github.com/fenghuijiuzhuan/RuoYi-terminal.git'
      url: 'https://gitee.com/yvan_gordon/RuoYi-terminal.git'
    }
  },
  methods: {
    goto() {
      window.open(this.url)
    }
  }
}
</script>