<template lang="html">
  <div id="app" class="">
    <h3>{{title}}</h3>
    <button type="button" class="btn btn-primary" name="button" @click="fetchCharacter">getCharacter</button>
  </div>
</template>

<script>
export default {
  name:'app',
  data(){
    return {
      title:'Genarate team'
    }
  },
  methods:{
    fetchCharacter(){
      fetch('https://swapi.co/api/people/1',{
        method:'GET',

      }).then(response=> response.json())
      .then(json=>console.log(json))
    }
  }
}
</script>

<style lang="css">
</style>
