<template>
    <div class="flex flex-row">
        <span @click="$emit('setActive', item)">
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