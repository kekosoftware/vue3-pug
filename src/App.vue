<template lang="pug">
div 
    h1 Hijo de div
    h2 Hermano de H1
    ol 
        li.element1 manzana
        li.element2 pera
        li#element3 melón

    a(
        href="https://google.com" 
        target="_blank"
    ) Google con Pug

    h2 Frutas
    ol 
        li(v-for="fruta in frutas") {{ fruta }}

lista(:elmentos="juegos")

</template>

<script>
import Lista from "./components/Lista.vue"

export default {
    data: () => ({
        frutas: ['manzana', 'pera', 'melón'],
        juegos: ['CSGO', 'Minecraft', 'PUBG',],
    }),
    components: { Lista },
}
</script>

<style scoped>

h1 {
    color: red;
}

.element1 {
    color:blue;
}
.element2 {
    color: purple;
}
#element3 {
    color: green;
}

</style>