<script setup>
const msg = ref("The news from the first component")
</script>

<template>
    <div>
        <h1 class="m-3 text-emerald-900 text-2xl text-center ">The First component</h1>
        <h2 class="text-1xl text-center  text-lime-900 border-green-900 border-2">
           {{ msg }}
        </h2>
    </div>
</template>