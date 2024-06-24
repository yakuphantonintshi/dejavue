<template>
    <div class="container">
        <div class="row">
            <h2 class="display-2">Products</h2>
        </div>
        <div class="row gap-2 justify-content-center">
            <Card v-for="product in products" :key="product.id">
                <template #cardHeader>
                    <img :src="product.ImageUrl" :alt="product.flowerName" class="img-fluid" loading="lazy">
                </template>
                <template #cardBody>
                    <p>{{ product.Description }} </p>
                    <p>Amount: R{{ product.Price }}</p>
                </template>
            </Card>
        </div>
    </div>
</template>

<script>
import Card from './Card.vue'
export default {
    name: "ProductComp",
    components: {
        Card
    },
    data() {
        return {
            products: [
        {
            id: 2,
            flowerName: "Lavender flower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/lavender_flowers.jpg",
            Price: 55.00
        },
        {
            id: 3,
            flowerName: "Lily flower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/lily_flower.jpg",
            Price: 250.00
        },
        {
            id: 4,
            flowerName: "Rose flower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/rose_flowers.jpg",
            Price: 300.00
        },
        {
            id: 5,
            flowerName: "Sunflower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/sunflower.jpg",
            Price: 200.00
        },
        {
            id: 6,
            flowerName: "Aster flower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/aster_flowers.jpg",
            Price: 345.00
        },
        {
            id: 7,
            flowerName: "Carnation flower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/carnation_flowers.jpg",
            Price: 500.00
        },
        {
            id: 8,
            flowerName: "Popies flower",
            Description: "Price per bunch, Stems per bunch: 20",
            ImageUrl: "https://yakuphantonintshi.github.io/myimages/Images/popies_flowers.jpg",
            Price: 450.00
        }
            ]
        }
    }
}
</script>

<style lang="scss" scoped></style>