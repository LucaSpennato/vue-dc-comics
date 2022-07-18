<template>
    <ul>
        <li><h5>{{ listName }}</h5></li>
        <li v-for="(link, index) in links"
            :key="index">
            <a :href="link.url"
            @click.prevent>{{ link.text }}</a>
        </li>
    </ul>
</template>

<script>
export default {
    name: 'link',
    props:{
        listName: String,
        links: Object,
    },
}
</script>

<style lang="scss">

    h5 {
        color: white;
        text-transform: uppercase;
    }
    ul {
        padding: 0;
        margin: 0;
        list-style: none;
    }
    li {
        line-height: 100%;
    }

</style>