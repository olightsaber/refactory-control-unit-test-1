<template>
    <div>
        <Jumbotron class="w-full" :item="activeItem" />
        <div class="flex flex-row " v-for="(item, index) in items" :key="index">
            <Thumbnail :item="item" @setActive="setActive" />     
        </div>
       
    </div>
</template>

<script>
export default {
    props: {
        items: {
            type: Array,
            default: () => []
        }
    },
    components: {
        Thumbnail: () => import('../Thumbnail'),
        Jumbotron: () => import('../Jumbotron')
    }, 
    data: () => ({
        activeItem: {}
    }),
    methods: {
        setActive(item) {
            // if (this.activeItem != null) {
            //     this.activeItem = item.length-1
            // }
            this.activeItem = item
        }
    }
}
</script>