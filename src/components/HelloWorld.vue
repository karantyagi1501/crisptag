<template>
  <div class="container mt-5">

   <form @submit="capitalize">
     <div class="input-group">
       <input type="text" name="" id="" placeholder="enter something" class="form-control" v-model="capitalized"/>
     </div>
     <input type="submit" value="capitalize" class="btn btn-primary mt-2">
   </form>

   <div class="box text-center">
     <p>{{capitalized}}</p>
   </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    

  },
  data(){
    return{
      capitalized:"",
    }
  },
  methods:{
    capitalize(E){
      E.preventDefault();
      this.capitalized = this.capitalized.toString().toUpperCase()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.box{
  border:1px solid lightgrey;
  border-radius:10px;
  margin-top: 2rem;
  padding: 5%;
}
</style>
