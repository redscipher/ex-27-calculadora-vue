<script setup lang="ts">
//
const numerosCalculadora = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
// 
</script>

<template>
    <!--  -->
    <div class="container py-5 text-center text-white">
        <ul class="row">
            <li class="col-4" v-for="num in numerosCalculadora">
                <button>{{ num }}</button>
            </li>
        </ul>
    </div>
    <!--  -->
</template>

<style scoped lang="scss">
    //
    ul{
        list-style: none;
    }
    //
</style>