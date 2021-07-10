<template>
 <div class="contaner">
   <input placeholder="متن را وارد کنید" type="text"  v-model="txt" >
   <br><br>
<button @click="addList">Add</button>
<br><br>

   <div v-for="item in mylist" :key="item">
    {{item}}
   </div>

 </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data(){
    return{
      txt:"",
    mylist:[]
    }
    },
    methods:{
addList(){
this.mylist.push(this.txt)
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
