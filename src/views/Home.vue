<template>
  <div class="home">
    <mt-header fixed title="Wechat"></mt-header>
  </div>
</template>

<script>
// @ is an alias to /src
import { Header } from 'mint-ui';

export default {
  name: 'home',
  components: {
    Header
  },
  data() {
      return {
          
      }
  },
  methods: {
      goDetails() {
          console.log('jump to user details')
          this.$router.push({
              path: '/user/details/12',
              params: {
                  userId: this.$route.params.id        
              }
          })
      }
  }
}
</script>
