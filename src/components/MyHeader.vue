<template>
  <header>
    
        <nav class="navbar">
            <div class="navLogo">
                <a href="#"><img src="../assets/images/avada-bakery-logo-retina.png" alt=""></a>
            </div>
            <div class="navLinks">
                <ul>
                    <li v-for="(link, index) in myNavLinks" :key="index"><a :href="link.url">{{link.text}}</a></li>
                    <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
                </ul>
            </div>
        </nav>
        <section class="imgWrapper">
            <div class="offers">
                <div class="demos">
                    <a href="#">
                        <i class="fa-solid fa-folder"></i>
                        <p>Demos</p>
                    </a>
                    
                </div>
                <div class="sale">
                    <a href="#">
                     <span class="dollar">$ </span>
                     <span class="price">39</span>
                     <p class="onSale">On Sale</p>
                    </a>
                    
                </div>
            </div>
            <div class="title">
                <p>FRESH & TASTY BAKERY EVERYDAY</p>
                <h1>The Perfect Fresh Bread</h1>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis numquam vero quia? Quo nam voluptatum ipsa eveniet dolorum quibusdam ipsam deserunt corporis rerum autem. </p>
                <button class="whiteBtn">Explore our products</button>
            </div>
        </section>
  </header>
</template>

<script>
export default {
    name: "MyHeader",
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
header{
    height: 80vh;
    background-image: url("../assets/images/hero-header-bakery.jpg");
    background-size: cover;

    .navbar{
        display: flex;
        align-items: center;
        justify-content: space-between;
        .navLogo img{
            width: 120px;
            margin-left: 10px;
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
    .title{
        text-align: left;
        margin-top: 30px;
        margin-left: 100px;
        max-width: 400px;
        line-height: 30px;

        h1{
            font-size: 2.5rem;
            color: $daisyBush;
        }
        p{
            color: $mamba;
            font-size: .8rem;
            margin: 20px 0;
        }
        .whiteBtn{
            color: $daisyBush;
            background-color: $white;
            border-radius: 8px;
            padding: 10px 15px;
            border: none;
            cursor: pointer;
            font-size: .5rem;
            &:hover{
                background-color: $daisyBush;
                color: $white;
            }
        }
    }
    .offers{
        display: flex;
        justify-content: flex-end;
        font-size: .5rem;
        flex-direction: column;
        align-items: flex-end;
        margin-top: 20px;
        margin-right: 20px;
            
        a{
            text-decoration: none;
            color: $mamba;
        }

        .demos, .sale{
            background-color: $white;
            border-radius: 8px;
            box-shadow: 20px 20px 50px grey;
            padding: 10px;
            margin: 5px 10px;
            
            i{
                color: $outerSpace;
            }
            .dollar, .price{
                color: $japaneseLaurel;
                font-weight: bolder;
            }
            .price{
                font-size: .7rem;
            }
        }
    }
}
</style>