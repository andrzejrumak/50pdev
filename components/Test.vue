<script setup>
const msg = ref("Taka wiadomość")
</script>

<template>
    <div>
        <h1>Component 1</h1>
        <h2>
           {{ msg }}
        </h2>
    </div>
</template>