<template>
<div>

 <div id="q-app">
    <toolbar />
    <router-view />
  </div></div>
 
</template>
<script>
import toolbar from 'components/header.vue' 
// 
export default {
  name: 'App',
  
  components: { toolbar },
}
</script>
