<template>
    <div class="footerUpper">
      <div class="footer">
          <div>
            <ul>
              <p class="title">
                DC COMICS
              </p>
              <li v-for=" element in dcComicsList">
                <p>
                 {{ element }}
                </p>
              </li>
       
              <p class="title-text title">
                   SHOP
              </p>
              <li v-for="shopElement in shopList">
                <p>
                 {{shopElement }}
                </p>
              </li>
            </ul>
          </div>
      
            <ul>
              <p class="title">
                DC
              </p>
              <li v-for=" dcElement in dcList">
              <p>
               {{ dcElement }}
              </p>
              </li>
            </ul>
      
            <ul>
              <p class="title">
                SITES
              </p>
              <li v-for=" siteElement in siteList">
              <p>
               {{ siteElement }}
              </p>
              </li>
            </ul>
      </div>
      

      <img src="../assets/img/dc-logo-bg.png" alt="">
    </div>
    <div class="flex-column">
      <div class="middleFooter">
        <div>
          <button >
            SIGN-UP NOW!
          </button>
        </div>
        <div class="flex">
          <p class="text">
            FOLLOW US
          </p>
          <ul class="flex">
            <li v-for="icon in iconsList"  class="iconsSize">

              <img :src="getImagePath(icon)" alt="icon's social" style="width: 90px; height: 90px;">

            </li>
          
          </ul>

        </div>
      
      </div>
      <div class="downFooter">

      </div>

   
    
    </div>
    
    
  
</template>
  
<script>
  export default {
  name : 'AppFooter',
  data(){
      return{
        dcComicsList : ['Characters', 'Comics', 'Movies', 'Tv', 'Games', 'Videos', 'News' ],

        dcList : ['Terms Of Use', ' Privacy', 'Ad Choises', 'Advertsing', 'Jobs', 'Subscriptions',
                   'Talent Workshop','CPSC Certificates', 'Ratings','Shop help','Contact Us'],

        shopList:[ 'Shop DC', 'Shop DC Collectibles'],
        
        siteList: [ 'DC', 'MAD Magazine', 'DC Kids', ' DC Univers', 'DC Power Visa'],

        iconsList : [ 'footer-facebook.png', 'footer-twitter.png', 'footer-youtube.png', 'footer-pinterest.png', 'footer-periscope.png']
  
      }
  },

  methods: {
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        
      }
  
  }
  
  };
</script>
  
<style lang="scss" scoped>
  

  div.footerUpper{
   height: 250px;
    background-image: url('../assets/img/footer-bg.jpg');
    object-fit: cover;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
   
  }

  .footer{
    display: flex;
    flex-direction: row;
    margin-left:30px;
    
    

  }
  div.middleFooter{
    height: 80px;
    background-color: #303030;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    
  }

  .flex-column{
    display: flex;
    flex-direction: column;
  }
  div.downFooter{
    height: 100px;
    background-color: black;
  
  }

  img{
    width: 410px;
    height: 410px;
    margin-left:20px;
    padding: 2rem;

  }
  
  ul{
    color:  #7f7f7f;
    display: flex;
    flex-direction: column;
    margin-right: 35px;
    margin-bottom: .8rem;
    padding-top: .5rem
    
  }
  li{
    display: flex;
    flex-direction: column;
    font-size: 11px;
    text-align: left;
    line-height: .8rem;
    
  }
  ul p.title{
    color:white;
    margin-bottom: .5rem;
   
  }
  li p{
    color: #818582;
  }

  button{
    height: 35px;
    border-color: #0a73d4;
    background-color:#303030;
    color: white;
    padding: .5rem;
    margin-right: 4rem;
  }

  .iconsSize{
   width: 45px;
    
  }

  .flex{
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  .title-text{
    margin-top: .3rem;
  }
  .text{
    color:#0b70df
  }


   
</style>