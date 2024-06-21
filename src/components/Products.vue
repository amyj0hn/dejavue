<template>

  <div class="container">
    <div class="row">
        <h2>Products</h2>
    </div>
    <div class="row gap-2">
    <Card v-for="(product, id) in products" :key="id">

    <template #cardHeader>
      <img :src="product.picture" :alt="product.productName" loading="lazy" class="img-fluid">
      </template>
      
      <template #cardBody>
        <p>{{ product.productName }} </p>
        <p>{{ product.status }}</p>
        <p>{{ product.price }}</p>
        <p>{{ product.description }}</p>
        </template>
    </Card>
  </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'
export default {
 name: 'ProductsComp',
 components: {
    Card
 },
 data(){
    return { 

      products: [
        { 
          id:1,
          productName: 'Pink Purse',
          status: 'In stock',
          price: 'R' + 300,
          description: 'Pink Fashionable Collar PU Leather Plain Bucket Bag Embellished Women Bags',
          picture: 'https://amyj0hn.github.io/project-images/images/purse.jpeg'


        },
        { 
          id:2,
          productName: 'Pink Purse',
          status: 'In stock',
          price: 'R' + 300,
          description: 'Pink Fashionable Collar PU Leather Plain Bucket Bag Embellished Women Bags',
          picture: 'https://amyj0hn.github.io/project-images/images/purse.jpeg'


        },
        { 
          id:3,
          productName: 'Pink Purse',
          status: 'In stock',
          price: 'R' + 300,
          description: 'Pink Fashionable Collar PU Leather Plain Bucket Bag Embellished Women Bags',
          picture: 'https://amyj0hn.github.io/project-images/images/purse.jpeg'


        },
        { 
          id:4,
          productName: 'Pink Purse',
          status: 'In stock',
          price: 'R' + 300,
          description: 'Pink Fashionable Collar PU Leather Plain Bucket Bag Embellished Women Bags',
          picture: 'https://amyj0hn.github.io/project-images/images/purse.jpeg'


        },
    ]
    
    }
}}
 


</script>

<style>

</style>