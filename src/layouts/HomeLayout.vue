<template>
  <router-view/>
</template>
  

<script>
// Import thành phần (components) NavBar, SideBar, FooterBar để sử dụng
import HeaDer from '@/components/HeaDer.vue'
import FooTer from '@/components/FooTer.vue'
import TopTer from '@/components/TopTer.vue'

import { useCounterStore } from '@/stores/counter';


// Để sử dụng được các thẻ (tag) của các component tương ứng
// <nav-bar />     -> component NavBar
// <side-bar />    -> component SideBar
// <footer-bar />  -> component FooterBar
// Chúng ta phải khai báo trong thuộc tính `components` của phần export default {}
export default {
  setup() {
    const counter = useCounterStore();
    return { counter }
  },
  mounted: function () {
    this.F_all_user();
  },
  methods: {
    async F_all_user(){
      // await this.counter.keep_login();
    }
  },
  components: {
    HeaDer,
    FooTer,
    TopTer,
  }
}
</script>
  
<style>
</style>
