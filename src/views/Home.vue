<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <div @click="loadChild()">加载子组件1</div>
    <div @click="loadChild2()">加载子组件2</div>
    <router-view />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  },
  methods: {
    loadChild() {
      this.$router.push({path:'/test'})
    },
    loadChild2() {
      this.$router.push({path:'/test1'})
    },
  },
};
</script>
