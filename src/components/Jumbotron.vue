<template>
        <div class="w-full">
            <img class="mx-auto flex justify-center" :src="item.url" alt/>
            <h1 class="font-serif text-4xl text-center">{{ item.title }}</h1>
            <h3 class="font-serif text-xl text-center">{{ item.caption }}</h3>
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