<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div id="pikachu"></div>
  </div>
</template>


<script>
// @ is an alias to /src
import depth from '@/depthmap.js'

export default {
  name: 'HomeView',
  // components: {
  //   depth
  // },
  data() {
    return {};
  },
  created() {
  },
  mounted() {
    this.depthmapTest();
  },
  methods: {
    depthmapTest() {
      depth.generate3dPhoto({
        el: '#pikachu', // Required!
        src: 'pikachu.jpg', // Required!
        map: 'pikachu.map.jpg', // Required!
        scale: 0.7 // Optional, default: 1 
      });
    }
  }
}
</script>