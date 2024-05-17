<script setup>
    import { ref } from 'vue';

    const showTheme1 = ref(true)
    const showTheme2 = ref(false)
    const showTheme3 = ref(false)
    const showTheme4 = ref(false)

    function showInfo(index) {
        if(index == 1) {
            showTheme1.value = true
            showTheme2.value = false
            showTheme3.value = false
            showTheme4.value = false
        }

        if(index == 2) {
            showTheme1.value = false
            showTheme2.value = true
            showTheme3.value = false
            showTheme4.value = false
        }

        if(index == 3) {
            showTheme1.value = false
            showTheme2.value = false
            showTheme3.value = true
            showTheme4.value = false
        }

        if(index == 4) {
            showTheme1.value = false
            showTheme2.value = false
            showTheme3.value = false
            showTheme4.value = true
        }
    }

</script>

<template>

<div  class="bg-blue-500 p-2 max-w-60 mx-auto mt-12 ">
    <div class="">
        <h1 @click="showInfo(1)" class="bg-blue-300 text-white px-1 flex justify-between cursor-default hover:cursor-pointer select-none">
            Tema 1 
            <span class="font-bold cursor-pointer"> {{ showTheme1 ? '-' : '+' }} </span>
        </h1> 
        <div v-show="showTheme1" class="bg-blue-50/50 text-black p-1 mt-1 cursor-default">
            Lorem ipsum
        </div>
    </div>

    <div class="">
        <h1 @click="showInfo(2)" class="bg-blue-300 text-white px-1 flex justify-between cursor-default hover:cursor-pointer select-none">
            Tema 2 
            <span  class="font-bold cursor-pointer"> {{ showTheme2 ? '-' : '+' }} </span>
        </h1> 
        <div v-show="showTheme2" class="bg-blue-50/50 text-black p-1 mt-1 cursor-default">
            Lorem ipsum
        </div>
    </div>

    <div class="">
        <h1 @click="showInfo(3)" class="bg-blue-300 text-white px-1 flex justify-between cursor-default hover:cursor-pointer select-none">
            Tema 3 
            <span class="font-bold cursor-pointer"> {{ showTheme3 ? '-' : '+' }} </span>
        </h1> 
        <div v-show="showTheme3" class="bg-blue-50/50 text-black p-1 mt-1 cursor-default">
            Lorem ipsum
        </div>
    </div>

    <div class="">
        <h1 @click="showInfo(4)" class="bg-blue-300 text-white px-1 flex justify-between cursor-default hover:cursor-pointer select-none">
            Tema 4 
            <span class="font-bold cursor-pointer"> {{ showTheme4 ? '-' : '+' }} </span>
        </h1> 
        <div v-show="showTheme4" class="bg-blue-50/50 text-black p-1 mt-1 cursor-default">
            Lorem ipsum
        </div>
    </div>
</div>    



</template>