<template>
    <div class="section section-plain-cards">
        
            <!--     *********    PLAIN BLOG CARDS      *********      -->
            <client-only>
              <div class="card-grid row">
                    <slider-card v-for="post in posts" v-bind:key="post.slug" :prefix="prefix" :post="post" :ct="post.attributes.category"/>
                   
                </div>
            </client-only>
                
            </div>
        </div>
        <!--     *********    END PLAIN BLOG CARDS      *********      -->
       
   
</template>
<script>
    import SliderCard from './SliderCard'; 
  export default {
    components: {
      SliderCard
    },
     props: {
    prefix: String,
    slug: String,
    posts: Array, 
  }
  }
</script>
<style>

.card-grid{

}
</style>
