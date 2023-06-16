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
header{
    height: 90px;
    position: relative;
    
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

</style>