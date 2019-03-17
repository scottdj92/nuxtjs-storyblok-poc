<template>
    <h1>{{ salutation }} {{ name }}, {{ message }}</h1>
</template>

<script lang="ts">
import Vue from 'vue'
type Data = {
    message: string;
}

type Props = "name" | "salutation";
export default Vue.component<Data, {}, {}, Props>("Message", {
    data() {
        return {
            message: "Nuxt.js"
        }
    },
    props: ["name", "salutation"]
})
</script>

<style>
    h1 {
        color: coral;
    }
</style>

