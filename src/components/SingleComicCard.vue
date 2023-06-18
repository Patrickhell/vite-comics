<template>
    <div class="cards">
        <img :src="cardElement.thumb" alt="">
        <div>
        <h3 class="series">
            {{ cardElement.series}}
        </h3>
        <p class="type">
            {{ cardElement.type }}
        </p>
        <p class="price">
            {{ cardElement.price }}
        </p>
    </div>   
        
    </div>
   
</template>

<script>

export default {
    name: 'SingleComicCard',
    props : {
            cardElement:Object
    },

}
</script >

<style lang="scss" scoped>
div.cards{
    width: calc((100% / 6) - 1rem);
    margin: .5rem;
}

img{
    width: 100%;
    height: 130px;
    object-fit: cover; 
}
 .type, .price{
    font-size: 13px;
    color:white;
}
.series{
    font-size: 14px;
    color: white;
    
}
</style>