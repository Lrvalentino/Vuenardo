<template>

  <section class="card-comp">
    <div class="card text-center">
        <img width="300" height="300" :src="imagen" :alt="plato">
        <div class="card-body">
            <h5 class="card-title">{{plato}}</h5>
            <p class="card-text">$<strong>{{costo}}</strong></p>
            <button v-if="stock" class="btn btn-primary">Comprar</button>
            <p v-else>Sin stock</p>
        </div>
    </div>
  </section>

</template>

<script>
  export default  {
    name: 'card-comp',
    props:         {
        plato:String,
        imagen:String,
        costo:Number,
        stock:Boolean
    },
    data () {
      return {

      }
    },
    methods: {

    },
}


</script>

<style scoped>
</style>
