<template lang="html">

  <section class="stats">
    <h1>Adrian, a furious warrior</h1>
    <p> Health:{{hp}} </p>
    <p> Mana:{{mana}} </p>
  </section>

</template>

<script lang="js">
  export default  {
    name: 'stats',
    props: [],
    mounted() {

    },
    data() {
      return {
        hp: 100,
        mana: 80,

      }
    },
    methods: {

    },
    computed: {

    }
}
</script>

<style scoped lang="css">
.stats {
  border: 5px solid gray;
  height: 25%;
}
</style>
