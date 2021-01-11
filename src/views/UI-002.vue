<template>
  <div class="flex-center">
    <div class="lightOn">
     <img class="src[currentSrc]"> 
    </div>
  </div>
</template>

<script>
data () {
  return {
    src: ['../assets/lightOff.png', '../assets/lightOn.png'],
    currentSrc: 0
  }
}

methods:{
   changeImage(){
        if(currentSrc < src.length-1){
            currentSrc ++
    }else{
           currentSrc = 0
    }
}

</script>

<style scoped>
  img{
    width: 300px;
    height: auto;
  }
</style>