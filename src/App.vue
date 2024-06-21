<template>
 <div>
  <Card>

  </Card>

  <Friends>
    
  </Friends>
 </div>
</template>

<script>
import Card from './components/Card.vue'
import Friends from './components/Friends.vue'

export default {
  name: 'App',
  components: {
    Card, Friends,
  },

  data(){
    return { 
      friends: [
        {
          firstName: 'Mapule',
          lastName: 'Mbuzwana',
          age: 89

        },
        {
          firstName: 'Mbalentle',
          lastName: 'Diko',
          age: 19

        },
        {
          firstName: 'Mbalentle',
          lastName: 'Diko',
          age: 19

        },
        {
          firstName: 'Mbalentle',
          lastName: 'Diko',
          age: 19

        },
        {
          firstName: 'Mbalentle',
          lastName: 'Diko',
          age: 19

        }
      ]
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
