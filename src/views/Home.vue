<template>
  <div class="home">
    <myMain/>
    <myFooter/>
  </div>
</template>

<script>
// @ is an alias to /src
import myMain from '@/components/myMain.vue'
import myFooter from '@/components/footer.vue'

export default {
  name: 'Home',
  components: {
    myMain,
    myFooter
  }
}
</script>
