<template>
  <header>
    <div class="navBar">
        <div class="imgLogo" >
            <img class="image" src="../assets/img/dc-logo.png" alt="logo-DC">
        </div>
        <ul>
            <li v-for="link in linkList" :class ="link.active ?'active' : '' ">
                <a href="link.linkList">
                   {{ link.text }}
                </a>
                <hr>
            </li>
        </ul>
    </div>
    <div class="jumbotron">
        <div class="currentSeriesButton">
          <button>
            CURRENT SERIES
          </button>
        </div>
    </div>
    
    

  </header>
</template>

<script>
export default {
name : 'AppHeader',
data(){
    return{

      linkList :[
        {
            link : '#',
            text : 'CHARACTERS',
            active : false
        },
        {
            link : '#',
            text : 'COMICS',
            active : true
        },
        {
            link : '#',
            text : 'MOVIES',
            active : false
        },
        {
            link : '#',
            text : 'TV',
            active : false
        },
        {
            link : '#',
            text : 'GAMES',
            active : false
        },
        {
            link : '#',
            text : 'COLLECTIBLES',
            active : false
        },
        {
            link : '#',
            text : 'VIDEOS',
            active : false
        },
        {
            link : '#',
            text : 'FANS',
            active : false
        },
        {
            link : '#',
            text : 'NEWS',
            active : false
        },

        {
            link : '#',
            text : 'SHOP',
            active : false
        },
    ]

    }
}

}
</script >

<style lang="scss" scoped>
header div.narbar{
    height: 90px;
    position: relative;
    
}
header div.jumbotron{
    height: 330px;
    background-image: url('../assets/img/jumbotron.jpg');
    background-repeat: no-repeat;
    object-fit: contain;
    position:relative;
}
div.navBar{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
   
    
}
img.image{
    width: 90px;
    padding: 1rem;
}
ul {
    list-style-type: none;
    display: flex;
    align-items: center;
    flex-direction: row;


}
li a {
    text-decoration: none;
    color: black;
    font-size: 10px;
    margin-right: 12px;

    &.active,
    &:hover {
        color: #0282f9;
    }
}

hr {
    display: none;
}

.active:hover hr {
    display: block;
    width: 30px;
    height: 5px;
    background-color: #0282f9;
    margin-left: 25px;
    position: absolute;
    bottom: 0;
    right: 557px;
}
div.currentSerieButton{

}
button{
    height: 45px;
    width: 200px;
    background-color: #0282f9;
    color: white;
    font-size: 18px;
    border: none;
    position:absolute;
    left: 150px;
    bottom: -20px;
    
}
</style>