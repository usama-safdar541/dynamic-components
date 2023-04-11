<template>
  <div class="quotes">
    <div>
<button @click="selectedComponent='appquote'">Quote</button>
<button @click="selectedComponent='appAuthor'">Author</button>
<button @click="selectedComponent='appNew'">New</button>
<!-- <p>{{ selectedComponent }}</p> -->
     
<component :is="selectedComponent"></component>

<AppQuotes >
      <h2>The QUotes</h2>
      <p>The wonderful quote</p>
     </AppQuotes>
     </div>
  </div>    
  
  </template>
  <script> 
  import Quote from './components/appQuote.vue';
  import New from './components/New.vue';
  import Author from './components/Author.vue';
  
  export default{
    data(){
return{
  selectedComponent: 'appquote'
}
    } , 
    
    components:{
  appQuotes: Quote,
  appAuthor:Author,
  appNew:New

      }
  } 
  
  
  </script> 

  <style scoped>

.quotes{
  display: flex;
  justify-content: center;
  border: 2px solid;
  width: 80%;
  border-radius: 20px;
  margin: auto;
}

</style>