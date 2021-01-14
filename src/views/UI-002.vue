<template>
  <div class="flex-center">
    <div>
      <img alt="" :src="getImgUrl(imageSource)" @click="changeImage()" /> 
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      imageSource: "lightOn"
    }
  },
  methods: {
    getImgUrl(pet) {
      var images = require.context('../assets/', false, /\.png$/)
      return images('./' + pet + ".png")
    },
    changeImage() {
     this.imageSource = "lightOff"
     if this.imageSource = "lightOn" {
       this.imageSource = "lightOff"
     }
        else {
          this.imageSource = "ligtsOn"
        }
    }
  }
}

</script>

<style scoped>
  img{
    width: 300px;
    height: auto;
  }
</style>
