<template>
   <main>
  
    <ComicsCards />
        <div id="mainDown">
            <ul>
                <li v-for="option in optionsList">

                  <img :src="getImagePath(option.image)" alt="image-DC">
                  <p>
                    {{option.text }}
                  </p>

                </li>
            </ul>

        </div>
    </main>
  </template>
  
  
  <script>

  import ComicsCards from './ComicsCards.vue';

  export default {
  name : 'AppMain',
  
  data(){
      return{
        optionsList: [
            {
                image:"buy-comics-digital-comics.png",
                text: "DIGITAL COMICS"
            },
            {
                image:"buy-comics-merchandise.png",
                text: "DC MERCHANDISE"
            },
            {
                image:"buy-comics-subscriptions.png",
                text: "SUBSCRIPTION"
            },
            {
                image:"buy-comics-shop-locator.png",
                text: "COMIC SHOP LOCATOR"
            },
            {
                image:"buy-dc-power-visa.svg",
                text: "DC POWER VISA"
            },
        ]
  
      };
      
    },

    components: {
      ComicsCards,
    },
   
  methods: {
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        
      }
  
  }
  
};
  </script>
  
  <style lang="scss" scoped>

  
  #mainDown{
    height: 100px;
    background-color:#0282f9;
   
  }

  h3{
    color: white;
    position: absolute;
    top:50%;
    left: 22%;
    transform: translate(-50%, -50%);
  }
  ul{
    justify-content: center;
    display: flex;
    flex-direction: row;
   
  }
  
  li{
    color: white;
   display: flex;
   flex-direction: row;
   font-size: 10px;
   align-items:center;
   margin-right:15px;
   padding:1.5rem;
  
   
  }

  img{
    width: 35px;
    margin-right: .5rem;
  }

  
  </style>