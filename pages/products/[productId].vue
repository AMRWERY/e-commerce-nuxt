<template>
    <section class="text-gray-600 body-font overflow-hidden">
        <div class="container px-5 py-24 mx-auto">
            <div class="lg:w-4/5 mx-auto flex flex-wrap">
                <ProductDetails :product="product" />
            </div>
        </div>
    </section>
</template>

<script setup>
const { productId } = useRoute().params

const uri = 'https://fakestoreapi.com/products/' + productId

const { data: product } = await useFetch(uri, { key: productId })
</script>