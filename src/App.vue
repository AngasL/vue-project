<template>
  <div id="app">
    <ul>
      <tree :model="data"></tree>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    tree
  },
  data(){
    return{
      data:data
    }
  }
}

var data = {
  name:"My Tree",
  children:[
    {name:'hello'},
    { name: 'wat' },
    {
      name: 'child folder',
       children: [
        {
          name: 'child folder',
          children: [
            { name: 'hello' },
            { name: 'wat' }
          ]
        },
        { name: 'hello' },
        { name: 'wat' },
        {
          name: 'child folder',
          children: [
            { name: 'hello' },
            { name: 'wat' }
          ]
        }
      ]
    }
  ]
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
