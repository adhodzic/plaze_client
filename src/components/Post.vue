<template>
        <div class="card" style="width: 19rem; height:370px">
        <img style="height:170px;" class="card-img-top" :src="info.url" alt="Card image cap">
        <div class="card-body">
        <p id="postedBy-text">{{info.postedBy}}</p>
        <p id="beach-location-text"><img id="post-location-icon" src="@/assets/maps-and-flags.png" alt="">{{info.title}}</p>
         <star-rating id="star-rating"  :star-size="30" :read-only="true" :show-rating="false" :rating="info.score"></star-rating>
        </div>
      </div>
</template>

<script>
import StarRating from 'vue-star-rating'
export default {
    props:["info"],
    components: {
      StarRating
  }
}
</script>

<style lang="scss" scoped>

#post-location-icon{
  height: 25px;
  widows: 25px;
  transform: translate(0px,-5px);
  margin-right: 5px;
}
.card-title{
  font-weight: bold;
}
#star-rating{
  transform: translate(0px,-110px);
}
#postedBy-text{
  font-size: 22px;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  transform: translate(-20px,0px);
  text-align: center;
  transform: translate(0px,-20px);
}
#beach-location-text{
  font-size: 20px;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  transform: translate(0px,-70px);
  text-align: left;
}
#details-button{
  transform: translate(95px,-140px);
}
.card-body{
  background-color: rgb(220, 234, 247);
  height: 100px;
}
@media (max-width: 768px) {
  #beach-location-text{
    text-align: left;
  }
  #details-button{
    margin-right: 20px;
  }
  .card{
    width: 25rem;
  }
}
</style>