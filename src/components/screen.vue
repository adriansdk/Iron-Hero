<template lang="html">

  <section class="screen" v-on:keydown.enter="movement(e)">
    <div class="myContainer">
      <div class="hero" v-bind:style="{ marginLeft: this.yPos + 'px', marginTop: this.xPos + 'px' }">
        <h1>hero</h1>
      </div>
    </div>
    
  </section>

</template>

<script lang="js">
  export default  {
    name: 'screen',
    props: [],
    mounted() {

    

    },
    data() {
      return {
        screen: document.querySelector('.screen'),
        character: document.querySelector('.hero'),
        yPos: 50,
        xPos: 50,
                
        }
    },
    methods: {
      movement:function(e) {
        console.log('whatever')
        if (e.keyCode == 37) {
          this.xPos -= 5
          console.log(this.xPos)

          //left
        }else if (e.keyCode == 38){
          this.yPos -= 5
          console.log(this.yPos)
          //up
        }else if (e.keyCode == 39){
          this.yPos += 5
          console.log(this.yPos)
          //right
        }else if (e.keyCode == 40){
          this.xPos -= 5
          //down
          console.log(this.xPos)
        }
        return {
        }

      }
      

    },
    computed: {

    }
}
</script>

<style scoped lang="css">

  section{
    height: 75%;
    border: 2px solid black;
  }

  .hero {
    height: 100px;
    width: 100px;
    background-color:red;
    border: black 2px solid;
  }
</style>
