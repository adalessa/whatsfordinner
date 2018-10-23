<template>
    <div id="app" class="container mx-auto flex flex-col items-center">
        <h1 class="my-4">What's for dinner?</h1>
        <button class="bg-blue rounded-full text-white py-2 px-4" @click="choose">Choose for me</button>
        <div class="my-4" v-if="eleccion" >The Dinner is {{eleccion}}</div>
    </div>
</template>
<script>
    export default{
        data() {
            return {
                eleccion: "",
                comidas: ["Pizza", "Milanesas", "Fideos", "Arroz"]
            }
        },
        methods: {
            choose() {
                this.eleccion = this.comidas[Math.floor(Math.random() * this.comidas.length)]
            }
        }
    }
</script>
<style>
    @tailwind preflight;
    @tailwind components;
    @tailwind utilities;
</style>
