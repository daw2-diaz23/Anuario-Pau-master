<template>
    <div class="col-2 offset-1 px-4">
      <div class="card carta shadow">
        <img class="cartaProfesor" :src='"/public/img/"+persona.photo' :alt='persona.nombre'>
        <p class="text-center pt-3">{{persona.nombre}}</p>
      </div>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        persona: Object
    }
}
</script>

<style>

</style>