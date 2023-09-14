<template>
    <!-- <div
        class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80">
        <img :src="product.image" class="h-full w-full object-cover object-center lg:h-full lg:w-full" />
    </div>
    <div class="mt-4 flex justify-between">
        <div>
            <h3 class="text-sm text-gray-700">
                <nuxt-link :to="`/products/${product.id}`">
                    <span aria-hidden="true" class="absolute inset-0" />
                    {{ product.title }}
                </nuxt-link>
            </h3>
        </div>
        <p class="text-sm font-medium text-gray-900">${{ product.price }}</p>
    </div> -->
    <div
        class="relative h-80 w-full overflow-hidden rounded-lg bg-white sm:aspect-h-1 sm:aspect-w-2 lg:aspect-h-1 lg:aspect-w-1 group-hover:opacity-75 sm:h-64">
        <img :src="product.image" class="h-full w-full object-cover object-center" />
    </div>
    <h3 class="mt-6 text-sm text-gray-500">
        <nuxt-link :to="`/products/${product.id}`">
            <span class="absolute inset-0" />
            {{ product.title }}
        </nuxt-link>
    </h3>
    <p class="text-base font-semibold text-gray-900">${{ product.price }}</p>
</template>

<script setup>
const { product } = defineProps(['product'])
</script>
