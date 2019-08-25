<template lang="html">

  <section class="stats">
    <h1 class="display-4 heroName">Adrian, a furious warrior</h1>
    <p class="statsBars"> Health: {{hp}} </p>
    <p class="statsBars"> Mana: {{mana}} </p>
    <p class="statsBars"> XP: {{xp}}/{{xpToLevelUp}} </p>
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
        xp: 0,
        xpToLevelUp: 100,

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
  background-color:black;
  color:white;
}

.heroName{
  font-weight: 400;
}

.statsBars{
  font-weight: 400;
  font-size:30px;
  margin: 2px 0px;
}
</style>
