<template lang="html">

  <section class="screen">
    <div class="myContainer">
      <div class="hero" v-bind:style="{movement}">
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
      function movement(e) {
        if (e.keyCode == 37) {
          this.xPos -= '5px';
          //left
        }else if (e.keyCode == 38){
          this.yPos -= 5;
          //up
        }else if (e.keyCode == 39){
          this.yPos += 5;
          //right
        }else if (e.keyCode == 40){
          this.xPos -= 5;
          //down
          console.log(this.xPos)
        }
      }

      document.onkeydown = movement;

    },
    data() {
      return {
        screen: document.querySelector('.screen'),
        character: document.querySelector('.hero'),
        yPos: 5,
        xPos:5,
                
        }
    },
    methods: {
      movement:function(e){
        

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
