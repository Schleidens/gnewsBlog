<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <myFooter/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import myFooter from '@/components/footer.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    myFooter
  }
}
</script>
