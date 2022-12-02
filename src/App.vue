<template>
    <div id="app">
        <img alt="Vue logo" src="./assets/logo.png">
        <HelloWorld msg="Vuenardo"/>
        <div class="container_flex">
            <card-comp :class="estilo1" v-for="(pizza,index) of pizzas" :key="index" :plato="pizza.plato" :imagen="pizza.imagen" :costo="pizza.costo" :stock="pizza.stock" :prod="pizza"></card-comp>
        </div>
        <div class="container_flex">
            <card-comp :class="estilo2" v-for="(pasta,index) of pastas" :key="index" :plato="pasta.plato" :imagen="pasta.imagen" :costo="pasta.costo" :stock="pasta.stock" :prod="pasta"></card-comp>
        </div>
        <div class="container_flex">
            <card-comp :class="estilo3" v-for="(postre,index) of postres" :key="index" :plato="postre.plato" :imagen="postre.imagen" :costo="postre.costo" :stock="postre.stock" :prod="postre"></card-comp>
        </div>
    </div>
</template>
<script>
  import CardComp from './components/card-comp.vue'
  import HelloWorld from './components/HelloWorld.vue'
  /* import card-comp from './components/HelloWorld.vue' */
  export default {
    name: 'App',
    components: {
        HelloWorld,
        CardComp
    },
    data () {
      return {
        pizzas:[
            {
                plato:"Pizza Margarita",
                imagen:"https://www.lanacion.com.ar/resizer/_F-gR7gXhZpGQF9u6I7aarAa53Q=/309x206/filters:format(webp):quality(80)/cloudfront-us-east-1.images.arcpublishing.com/lanacionar/M7NX62ONAJGRHMGZQKL3UMOIG4.jpeg",
                costo:7990,
                stock:true
            },
            {
                plato:"Pizza Napoletana",
                imagen:"https://res.cloudinary.com/tf-lab/image/upload/restaurant/9b544d66-5c1f-42c3-9d7e-902802c437b2/797ff405-94f7-4698-a45d-d7eafd67b6a6.jpg",
                costo:10990,
                stock:true
            },
            {
                plato:"Pizza del Huerto",
                imagen:"https://tofuu.getjusto.com/orioneat-prod/tCv7jXW5AzJhBweoR-Del%20Huerto.jpg",
                costo:16990,
                stock:false
            },
            {
                plato:"Pizza Gorgonzola",
                imagen:"https://www.silviocicchi.com/pizzachef/wp-content/uploads/2015/03/g3.jpg",
                costo:17990,
                stock:true
            },
        ],
        pastas:[{
                plato:"Sorrentinos",
                imagen:"https://canalcocina.es/medias/publicuploads/2012/11/11/92889/1gm5mvqgcfygjesl396w.jpg",
                costo:8990,
                stock:true
            },
            {
                plato:"Spaghetti",
                imagen:"https://m.ftscrt.com/static/recipe/c03fbea5-6fd4-458e-b726-f59bd9a3e86b.jpg",
                costo:5990,
                stock:false
            },
            {
                plato:"Canelloni",
                imagen:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRpNirJExILXg4C4-PrCliRkgD6ewge3qld8w&usqp=CAU",
                costo:11990,
                stock:true
            },
            {
                plato:"Lasagna",
                imagen:"https://www.eatthis.com/wp-content/uploads/sites/4/2020/03/gluten-free-dairy-free-lasagna.jpg?quality=82&strip=1",
                costo:12990,
                stock:true
            },
        ],
        postres:[{
                plato:"Pannacotta",
                imagen:"https://cdn5.recetasdeescandalo.com/wp-content/uploads/2018/10/Panacota-o-panna-cotta-receta-del-clasico-postre-italiano-de-nata.jpg",
                costo:2590,
                stock:true
            },
            {
                plato:"Helado",
                imagen:"https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Ice_Cream_dessert_02.jpg/245px-Ice_Cream_dessert_02.jpg",
                costo:3990,
                stock:true
            },
            {
                plato:"Panqueques con manjar",
                imagen:"https://img-global.cpcdn.com/recipes/6f911cff980811c2/400x400cq70/photo.jpg",
                costo:2990,
                stock:true
            },
            {
                plato:"Torta de chocolate",
                imagen:"https://t2.rg.ltmcdn.com/es/posts/2/5/2/torta_de_chocolate_casera_45252_orig.jpg",
                costo:3990,
                stock:true
            },
        ],
        estilo1:{
        },
        estilo2:{
        },
        estilo3:{
        }
      }
    },
  }
</script>
<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2C3E50;
    margin-top: 60px;
}
.container_flex{
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin: 1rem 0;
}
</style>