<template>
  <div id="app">
    <Sintaxe/>
  </div>
</template>

<script>
import Sintaxe from '@/documentacao/Sintaxe.vue'

export default {
  name: 'App',
  components: {
    Sintaxe
  }
}
</script>

<style lang="scss">
body{


}

#app {

}
.card{
  border:5px solid #1f83ed!important;
  border-radius: 12px!important;
  h3{
    color:#1f83ed ;
    font-weight: 600;
  }

  h5{
    color:#000 ;
    font-weight: 600;
  }
}


</style>
