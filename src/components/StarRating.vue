<script>

  export default {
    name: 'StarRating',

    data() {
      return {
        rate: 0,
        selection: 0,
        isClicked: false
      }
    },

    computed: {
      firstStar() {
        return (this.selection || this.rate) >= 1 ? '★' : '☆'
      },
      secondStar() {
        return (this.selection || this.rate) >= 2 ? '★' : '☆'
      },
      thirdStar() {
        return (this.selection || this.rate) >= 3 ? '★' : '☆'
      },
      fourthStar() {
        return (this.selection || this.rate) >= 4 ? '★' : '☆'
      },
      fifthStar() {
        return (this.selection || this.rate) >= 5 ? '★' : '☆'
      },
      message(){
        return this.rate == 0 ? 'Valórame!' 
          : this.rate == 1 ? 'Valoración: 1 estrella'
          : `Valoración: ${this.rate} estrellas`
      }
    },

    methods: {
      handleClick() {
        const clickedId = parseInt(event.target.id)
        this.isClicked = true
        
        if(clickedId == this.rate) {
          this.rate = 0
          this.selection = 0
        }
        else this.rate = clickedId
      },
      handleHover() {
        const clickedId = parseInt(event.target.id)
        this.selection = clickedId
      },
      handleMouseOut(){
        console.log(this.rate)
        if(!this.isClicked) this.selection = 0

        this.isClicked = false
      }
    }
  }
</script>


<template>
  <div>
    <span id="1" @click="handleClick" @mouseover="handleHover" @mouseout="handleMouseOut" >{{ firstStar }}</span>
    <span id="2" @click="handleClick" @mouseover="handleHover" @mouseout="handleMouseOut" >{{ secondStar }}</span>
    <span id="3" @click="handleClick" @mouseover="handleHover" @mouseout="handleMouseOut" >{{ thirdStar }}</span>
    <span id="4" @click="handleClick" @mouseover="handleHover" @mouseout="handleMouseOut" >{{ fourthStar }}</span>
    <span id="5" @click="handleClick" @mouseover="handleHover" @mouseout="handleMouseOut" >{{ fifthStar }}</span>
  </div>
  <div>
    <p>{{ message }}</p>
  </div>
</template>


<style scoped>
  div {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  span {
    color: gold;
    font-size: 50px;
  }
  p{
    font-size: 1.6rem;
    margin: 0;
  }
</style>
