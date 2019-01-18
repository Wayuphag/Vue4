<template>
  <div class="photo">
  <br>
  <button @click="NextImg()">Next</button>
  <button @click="PrevImg()">Prev</button>
  <br>
    <img alt="Vue logo" :src="ImgLink[ImgIndex]" width="500">
  </div>
</template>

<script>


export default {
  name: 'photo',
  data (){
      return{
          ImgLink :[
              'https://scontent.fbkk10-1.fna.fbcdn.net/v/t1.0-9/38817202_10205018439496482_884330012444983296_n.jpg?_nc_cat=108&_nc_ht=scontent.fbkk10-1.fna&oh=157ed8653fbe3a6570a229024d8a79ce&oe=5CC909E3'
              ,'https://scontent.fbkk10-1.fna.fbcdn.net/v/t1.0-9/35644891_10204835794050460_3909774120425881600_n.jpg?_nc_cat=111&_nc_ht=scontent.fbkk10-1.fna&oh=cd59f04d3266ce6b04122405631230e8&oe=5CFD2771'  
          ],
          ImgIndex: 0
      }
  },
  methods:{
     NextImg(){
            this.ImgIndex++
            if(this.ImgIndex == this.ImgLink.length){
                this.ImgIndex = 0
            }
        },
     PrevImg(){
            this.ImgIndex--
            if(this.ImgIndex == this.ImgLink.length + 1){
                this.ImgIndex 
            }
        }
    }
}
</script>
