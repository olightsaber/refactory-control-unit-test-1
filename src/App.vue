<template>
  <div id="app">
    <div class="flex flex-row mx-2">
      <div class="w-1/3 flex flex-col">
        <input type="text" class="mb-4 mx-1 bg-gray-200 border-orange-300 border" v-model="url" placeholder="Url">
        <input type="text" class="mb-4 mx-1 bg-gray-200 border-orange-300 border" v-model="title" placeholder="title image">
        <input type="text" class="mb-4 mx-1 bg-gray-200 border-orange-300 border" v-model="caption" placeholder="caption image">
        <button @click="submitImg" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-1 px-1  mx-2 rounded">Submit</button>
      </div>

      <MiniGallery class="w-2/3" :items="galleries"/>
    </div>
    
    
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      url: '',
      title: '',
      caption: '',
      galleries: [],
    }
  },
  components: {
    MiniGallery: () => import('./components/MiniGallery/index')
  },
  methods: {
    submitImg() {
      let _ = this;
      var ups = {
          "title" : this.title,
          "url" : this.url,
          "caption" : this.caption
          }
      if (_.url && _.title && _.url != null ) {
        _.galleries.push(ups);
        console.log(ups)
        _.url = '',
        _.title = '',
        _.caption = ''
      }
    console.log(_.galleries)
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
input[type="text"]{
  text-align:center;
}
input[type="text"]::placeholder {  
    /* Firefox, Chrome, Opera */ 
    text-align: center; 
} 

</style>
