<template>
    <div id="app">
        <Header/>
        <router-view/>
    </div>
</template>

<style>
    html,
    body {
        margin: 0;
        padding: 0;
        height: 100%;
    }
</style>
<script lang="ts">
    import Vue from "vue";
    import {Component} from "vue-property-decorator";
    import Header from "@/components/Header.vue";

    @Component({
        components: {Header}
    })
    export default class App extends Vue {
    }
</script>