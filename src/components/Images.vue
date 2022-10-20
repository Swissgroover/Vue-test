<script setup>
import { computed, reactive, ref } from 'vue';
const transform = ref(false);

</script>
<template>
    <div class="max-w-2xl m-auto">
        <div class="text-center p-4">
            <button class="p-4 rounded-md bg-blue-100 text-xs" @click="transform = !transform">Shuffle?</button>
        </div>
        <div v-if="!transform">
            <div class="grid grid-flow-col grid-rows-2 grid-cols-3 gap-8">
                <div class="col-start-1">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1665911291889-270afca0a2d9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2086&q=80" alt="" loading="lazy">
                </div>
                <div class="col-start-3">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666115883713-c5766e9d668e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2832&q=80" alt="" loading="lazy">
                </div>
                <div>
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666096968009-f8b7bdd51ba3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80" alt="" loading="lazy">
                </div>
                <div>
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666043073961-6112c7e1646c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80" alt="" loading="lazy">
                </div>
                <div class="row-start-1 col-start-2 col-span-2">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666126431272-8bffcafa6fb1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80" alt="" loading="lazy">
                </div>
            </div>
        </div>

        <div v-if="transform" class="m-auto p-20 transform">
            <div class="grid grid-flow-col grid-rows-2 grid-cols-3 gap-8">
                <div class="transform scale-110 -rotate-6 blur">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666096968009-f8b7bdd51ba3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80" alt="" loading="lazy">
                </div>
                <div class="col-start-3 transform scale-75 rotate-6 translate-x-2 translate-y-15">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1665911291889-270afca0a2d9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2086&q=80" alt="" loading="lazy">
                </div>
                <div class="transform scale-150 translate-y-11">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666043073961-6112c7e1646c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987&q=80" alt="" loading="lazy">
                </div>
                <div class="transform translate-y-24">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666115883713-c5766e9d668e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2832&q=80" alt="" loading="lazy">
                </div>
                <div class="row-start-1 col-start-2 col-span-2 transform translate-x-20 translate-y-4">
                    <img class="rounded-lg" src="https://images.unsplash.com/photo-1666126431272-8bffcafa6fb1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2340&q=80" alt="" loading="lazy">
                </div>
            </div>
        </div>
    </div>
</template>