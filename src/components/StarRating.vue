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
      }
    },
    methods: {
      handleClick(id) {
        // const clickedId = parseInt(event.target.id)
        this.isClicked = true
        
        if(id == this.rate) this.rate = 0
        else this.rate = id

        console.log(id == this.rate, id, this.rate)
      },
      handleHover(id) {
        this.selection = id
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
    <p id="1" @click="handleClick(1)" @mouseover="handleHover(1)" @mouseout="handleMouseOut" >{{ firstStar }}</p>
    <p id="2" @click="handleClick(2)" @mouseover="handleHover(2)" @mouseout="handleMouseOut" >{{ secondStar }}</p>
    <p id="3" @click="handleClick(3)" @mouseover="handleHover(3)" @mouseout="handleMouseOut" >{{ thirdStar }}</p>
    <p id="4" @click="handleClick(4)" @mouseover="handleHover(4)" @mouseout="handleMouseOut" >{{ fourthStar }}</p>
    <p id="5" @click="handleClick(5)" @mouseover="handleHover(5)" @mouseout="handleMouseOut" >{{ fifthStar }}</p>
  </div>
</template>


<style scoped>
  p {
    color: gold;
    font-size: 50px;
  }
  div {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
</style>
