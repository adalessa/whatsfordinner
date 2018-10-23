<template>
    <div id="app" class="container mx-auto flex flex-col items-center h-full mt-10">
        <h2 class="my-10">What's for dinner?</h2>
        <button class="bg-blue rounded-full text-white py-2 px-4" @click="choose">Choose for me</button>
        <div class="my-10 text-green-dark" v-if="eleccion" >The Dinner is {{eleccion}}</div>
        <div class="my-10" v-else>Food not choosed</div>
        <div>
            <div class="mb-4 font-bold">Plates: </div>
            <ul class="list-reset">
                <li v-for="comida in comidas">{{comida}}</li>
            </ul>
        </div>
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
