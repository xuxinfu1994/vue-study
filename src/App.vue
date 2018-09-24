<template>
  <div id="app">
    
    <Dialog 
      :isShow="showDilog" 
      @closeDialogHandle="closeDia">
    </Dialog>
    
  </div>
</template>

<script>
import Dialog from './components/Dialog.vue';

export default {
  name: 'app',
  data() {
    return {
      showDilog: true,
    }
  },
  components: {
    Dialog
  },
  methods: {
    closeDia: function(bname){

      if( typeof bname == 'function' ) {
        bname();
      }

      this.showDilog = false;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
