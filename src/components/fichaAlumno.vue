<template>
    <div class="col-2 offset-1 px-4">
      <div class="card carta shadow" >
        <router-link :to="{name:'card', params:{id:persona.id}}"><img class="card-img-top imagencarta" :src='"/public/img/"+persona.photo' :alt='persona.nombre'></router-link>
        <p class="text-center pt-3 ">{{persona.nombre}}</p>
      </div>
    </div>
</template>

<script>
export default {
    name: 'TheCard',
    props: {
        persona: Object
    }
}
</script>

<style>

  
</style>