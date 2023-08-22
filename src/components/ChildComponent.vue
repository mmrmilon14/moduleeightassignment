<script setup>
   const props  = defineProps(['message']);
   const emit   = defineEmits(['update:modelValu']);

   function messageEmitted (){
     props.name = emit('update:message','Hi I\'m a Web Developer with Vue Learner!')
   }

</script>

<template>
    <div class="mt-10">
        <h1 class="text-black-900 text-xl my-5">Chiled Component:</h1>
        <h2 class="text-black text-xl my-5">Message : <span class="text-yellow-600 hover:text-yellow-900">{{ message }}</span></h2>

        <button @click="messageEmitted ()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold my-8 py-2 px-4 rounded">
            Button
        </button>
    </div>
</template>

<style scoped>

</style>