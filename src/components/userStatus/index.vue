<!--
 * @path        : \RuoYi-terminal\src\components\userStatus\index.vue
 * @message     : 
 * @Author      : yvangod
-->
<template>
  <div>
    <div class="user-wrapper">
      <img :src="avatar" class="user-avatar" />
      <div class="name">
        {{ nickName }}
      </div>
      <div class="exit" @click="logout">
        退出
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  computed: {
    
    ...mapGetters([
      'nickName',
      'avatar',
      'device'
    ]),
  },
  methods: {
    
    async logout() {
      this.$confirm('确定注销并退出系统吗？', '提示', {
        confirmButtonText: '确定',
        cancelButtonText: '取消',
        type: 'warning'
      }).then(() => {
        this.$store.dispatch('LogOut').then(() => {
          location.href = '/index';
        })
      }).catch(() => {});
    }
  }
};
</script>

<style lang="scss" scoped>
.user-wrapper{
  display: flex;
  align-items: center;
  .name{
    margin-left: 5px;
  }
  .exit{
    margin-left: 10px;
  }
}
</style>
