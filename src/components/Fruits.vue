<template>
<section>
    <button @click="toggleGridView">Toggle Grid View</button>
    <ul :class="{'grid-view':this.gridView}">
        <li v-for="fruit in fruits.fruits" :key="fruit">
            {{fruit}}
        </li>
    </ul>
</section>
</template>

<script>
export default {
    name: 'Fruits',
    props: ['fruits'],
    data () {
        return {
        gridView: true
        }
    },
    methods: {
        toggleGridView() {
            this.gridView = !this.gridView;
        }
    }
}
</script>

<style scoped>
* {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
    box-sizing: border-box;
    padding: 0;
    margin: 0
}

.grid-view {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    list-style: none;
}
.grid-view li {
    text-align: center;
    display: block;
    width: calc(100%/3);
    height: 30vw;
    padding: 10vw 0;
}
</style>