<template>
    <div class="bg-white">
        <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-full lg:px-8">
            <h2 class="text-2xl font-bold tracking-tight text-gray-900">Customers also purchased</h2>

            <div class="mt-6 space-y-12 h-32 lg:grid lg:grid-cols-3 lg:gap-x-6 lg:space-y-0">
                <div v-for="product in products" class="group relative">
                    <ProductCard :product="product" />
                </div>
            </div>
        </div>
    </div>
</template>
  
<script setup>
const { data: products } = await useFetch('https://fakestoreapi.com/products')
</script>