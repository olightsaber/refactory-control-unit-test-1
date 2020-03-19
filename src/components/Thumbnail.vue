<template>
    <div class="w-full flex">
        <span @click="$emit('setActive', item)" class="w-full">
            <img :src="item.url" />
            <h2>{{ item.title }}</h2>
            <h4>{{ item.caption }}</h4>
        </span>       
    </div>
</template>

<script>
export default {
    props: {
        item: Object
    }
}
</script>