<template>
   
        <div class="top-0 right-0">
            <img class="flex align-center" :src="item.url" alt/>
        
            <h1 class="font-serif text-3xl text-center">{{ item.title }}</h1>
            <h3>{{ item.caption }}</h3>
        </div>
        
        
    
</template>

<script>
export default {
    props: {
        item: Object
    },
    data: () => ({
        title: 'gambar1',
        url: 'inigambar.jpg',
        caption: 'lorem ipsum dolores it sums'
    })
}
</script>