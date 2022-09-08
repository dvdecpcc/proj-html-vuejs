<template>
  <section class="footerTop">
    <div class="leftSide">
      <img src="../assets/images/avada-bakery-logo-retina.png" alt="bakery logo">
      <div class="navLinks">
                <ul>
                    <li v-for="(link, index) in myNavLinks" :key="index"><a :href="link.url">{{link.text}}</a></li>
                    <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
                </ul>
            </div>
    </div>
    <div class="rightSide">
      <h4>Subscribe to our newsletter</h4>
      <div class="input">
        <input type="text" placeholder="Enter email address">
        <button class="purpleBtn">Subscribe</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
name: "MyFooter",
data: function(){
        return {
            myNavLinks: [
                {
                    text:"HOME",
                    ulr:"#"
                },
                {
                    text:"SHOP",
                    ulr:"#"
                },
                {
                    text:"ABOUT",
                    ulr:"#"
                },
                {
                    text:"GALLERY",
                    ulr:"#"
                },
                {
                    text:"LOCATIONS",
                    ulr:"#"
                },
                {
                    text:"JOURNAL",
                    ulr:"#"
                },
                {
                    text:"CONTACTS",
                    ulr:"#"
                },
                {
                    text:"MY ACCOUNT",
                    ulr:"#"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "../styles/commonRules.scss";

  .footerTop{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin: 60px 60px;
    img{
      width: 150px;
      }
     .navLinks{
            display: flex;
            align-items: center;
            justify-content: space-around;
            flex-direction: row;
            cursor: pointer;


            ul li{
                font-size: .5rem;
                display: inline;
                margin: 5px 20px;
                color: $daisyBush;
                list-style: none;
                &:hover{
                    border-bottom: 1px solid $daisyBush;
                }
            }
        }
  }
  h4{
    margin-bottom: 20px;
    color: $daisyBush;
  }
  input{
    padding:5px 10px;
    margin-right: 10px;
    }
  .purpleBtn{
        background-color: $daisyBush;
        color: $white;
        border-radius: 8px;
        padding: 10px 15px;
        border: none;
        cursor: pointer;
        font-size: .5rem;
        &:hover{    
        color: $daisyBush;
        background-color: rgb(236, 232, 243);
        }
    }   
</style>