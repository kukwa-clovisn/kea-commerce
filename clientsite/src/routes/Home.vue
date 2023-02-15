<template>
    <main>
       <header>
        <div class="top-header">
            <div class="logo">
                KEA-COMMERCE
            </div>
            <div class="info-links">
               <div class="info-links-wrapper">
                <div class="content flex-row">
                    <div class="left-content"><i class="fa-solid fa-phone"></i></div>
                    <div class="right-content">
                        <a href="/">+237682449347</a>
                        
                    </div>
                </div>
                <div class="content flex-column">
                    <div class="content-flex"><i class="fa-solid fa-envelope"></i><a href="/">codingherald@gmail.com</a></div>
                    <div class="content-flex"><i class="fa-brands fa-whatsapp"></i><a href="/">codingherald</a></div></div>
               </div>
            </div>
        </div>
        <div class="bottom-header">
            <div class="left-bottom-header">My account<i class="fa-solid fa-caret-down"></i></div>
            <div class="bottom-header-routes">
                <div class="routes-wrapper">
                    <router-link to="/">Home</router-link>
                    <router-link to="/">shop</router-link>
                    <router-link to="/">pages</router-link>
                    <router-link to="/">cart</router-link>
                    <router-link to="/">about</router-link>
                </div>
            </div>
            <div class="right-bottom-header">
                <div class="content-wrapper">
                    <div class="search-box-wrapper">
                        <input type="search" name="search" id="search" placeholder="search item">
                        <button><i class="fa-solid fa-magnifying-glass"></i></button>
                    </div>
                </div>
            </div>
            <div class="cart">
                <div class="cart-wrapper">
                    <button>
                        <i class="fa-solid fa-cart-shopping"></i> 10 items ~ $210
                    </button>
                    
                </div>
            </div>
        </div>
       </header>
       <div class="landing-page">
<div class="main-wrapper">
    <div class="main-wrapper-content">
        <h3>kea-commerce at your sercice daily daily</h3>
        <h1>Get new arrivals from all around the world at one click. </h1>
        <router-link to="/">start shopping</router-link>
    </div>
    <div class="carousel-wrapper">
        <carousel :images="images" />
    </div>
</div>
       </div>
    </main>
</template>

<script > 
import carousel from '../components/carousel.vue'
import { ref } from 'vue'

export default{ 
    name:'carousel',
   
components: { 
    carousel
},setup(){ 
    const images = ref([
        "https://s3.envato.com/files/379243010/Retail%20Shopping%20(8).JPG","https://c8.alamy.com/comp/2J5A49J/e-commerce-ecommerce-web-banner-on-violet-background-various-shopping-icons-online-shopping-concept-2J5A49J.jpg","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSBFNc5TzSEqnmcPGsXg13507uO5VX4OGXUqw&usqp=CAU","https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSiqYLK3MWQ6OFSTi1cyi2vC0rXw_9NF0nGnw&usqp=CAU"
    ])
    return{images}
}
}

</script>

<style lang="scss" scoped>
$prime-color:rgb(209, 59, 0);
main{ 
    width:100vw;
    height:fit-content;

    header{ 
        max-width:100%;
        height:23vh;
        padding:0;
        margin:0;

        .top-header{ 
            width:100%;
            height:35%;
            display:flex;
            justify-content: space-between;
            align-items: center;
            background:rgb(30,30,38);
           

            .logo{ 
                width:20%;
                height:90%;
                display:flex;
                justify-content:center;
                align-items:center;
                font-size:20px;
                font-weight:600;
                color:white;
                font-family: "Poppins",sans-serif;
             
            }
            .info-links{ 
                width:35%;
                height:100%;
                display:flex;
                justify-content:center;
                align-items:center;

              .info-links-wrapper{ 
                height:60%;
                width:100%;
                  display: flex;
                  justify-content:space-evenly;
                  align-items: center;
                  .content{ 
                    width:30%;
                    height:100%;
                    display:flex;
                    align-items: center;
                    justify-content: center;
                    

                    i{ 
                        color:rgb(236, 235, 235);
                        font-size:12px;
                    }
                    a{ 
                        color:rgb(224, 224, 224);
                        font-size:11px;
                        font-family:"Nunito Sans",sans-serif;
                        letter-spacing: 1px;
                    }

                    .left-content{ 
                        width:fit-content;
                        height:100%;
                        display:flex;
                        justify-content:flex-end;
                        align-items:center;

                        i{ 
                            font-size:19px;
                        }
                    }
                    .right-content{ 
                        min-width:80%;
                      
                        display:flex;
                        justify-content:flex-start;
                        align-items:center;
                        flex-direction: column;
                    }
                    .content-flex{ 
                        width:100%;
                        display:flex;
                        justify-content:space-between;
                        align-items:center;
                      

                        i {
                            font-size:15px;
                            width:25%;
                            display:flex;
                            justify-content:center;
                            align-items:center;
                           
                        }
                        a{ 
                            width:75%;
                            display:flex;
                            font-size:11px;
                            justify-content:flex-start;
                            align-items:center;
                        }
                    }
                  }

                  .flex-row{ 
                    width:30%;
                    flex-direction: row;
                  }
                  .flex-column{ 
                    width:50%;
                    flex-direction:column;
                  }
              }
            }
        }

        .bottom-header{ 
            width:100%;
            height:65%;
            display:flex;
            justify-content:space-around;
            align-items:center;
            box-shadow: 0 5px 5px 7px rgb(30,30,38);
          

            .left-bottom-header{ 
                width:10%;
                height:100%;
              cursor:pointer;
                display:flex;
                justify-content: center;
                align-items:center;
                // border-right:1px solid rgb(30,30,38);
                font-size:20px;
                font-weight: 600;
                box-shadow: -5px 0 5px 3px rgb(30,30,38);

               i{ 
                    font-size:20px;
                }
            }
            .bottom-header-routes{ 
                width:55%;
                height:100%;
                display: flex;
                justify-content:center;
                align-items:center;

                .routes-wrapper{ 
                    width:100%;
                    height:100%;
                    display:flex;
                    justify-content:space-evenly;
                    align-items:center;

                    a{ 
                        color:rgb(32, 32, 32);
                        text-transform: capitalize;
                        font-size:18px;
                        font-weight:600;
                    }
                }
            }
            .right-bottom-header{ 
                width:22%;
                height:100%;
                display:flex;
                justify-content:space-evenly;
                align-items:center;

                .content-wrapper{ 
                    width:100%;
                    height:100%;
                    display:flex;
                    justify-content:space-evenly;
                    align-items: center;

                    .search-box-wrapper{ 
                        width:100%;
                        display:flex;
                        justify-content:center;
                        align-items:center;
                        border:1px solid $prime-color;

                        input{ 
                            width:75%;
                            height:40px;
                            padding:2px 5px;
                            padding-left:15px;
                            outline:none;
                            border:none;
                        }
                        button{ 
                            width:25%;
                            height:40px;
                            padding:2px 5px;
                            outline:none;
                            border:none;
                            display:flex;
                            justify-content:center;
                            align-items:center;
                            background:rgb(209, 59, 0);
                            border-radius: 0;

                            i{ 
                                font-size:22px;
                                color:rgb(235, 235, 235);
                            }

                            &:hover{ 
                                background:rgb(219, 219, 219);
                            }
                        }
                    }
                }
            }
            .cart{ 
                width:10%;
                height:100%;
                display:flex;
                justify-content:center;
                align-items: center;

                .cart-wrapper{ 
                    width:100%;
                    height:40px;
                    display:flex;
                    justify-content:center;
                    align-items:center;
                    border:1px solid $prime-color;
                    background:$prime-color;

                    button{ 
                        width:100%;
                        height:100%;
                        display:flex;
                        justify-content:center;
                        align-items:center;
                        outline:none;
                        border:none;
                        background:none;
                        color:white;
                        font-size:12px;

                        i{ 
                        color:white;
                            font-size:19px;
                        }
                    }
                }
            }
        }
    }
    .landing-page{ 
        width:100vw;
        height:70vh;
        background:rgb(240, 240, 240);

        .main-wrapper{ 
            width:100%;
            height:100%;
            display:flex;
            justify-content: flex-start;
            align-items: center;
            position:relative;

            .main-wrapper-content{ 
                width:55%;
                height:fit-content;
                position:relative;
                z-index: 1;
              
margin-left:10%;
              padding:10px;

                h3{ 
                    font-size:13px;
                    font-weight:500;
                    padding:0;
                    margin:0;
                    color:rgb(235, 234, 234);
                    font-family:"Nunito Sans",sans-serif;
                    word-spacing: 10px;
                }
                h1{ 
                    font-size:55px;
                    font-weight:600;
                    text-transform:capitalize;
                    font-family: "Nunito Sans",sans-serif;
                    margin:0;
                    margin: 35px 0;
                    margin-top:10px;
                    padding:0;
                    color:rgb(219, 219, 219);
                    word-spacing:7px;
                    line-height:70px;
                }

                a{ 
                    width:200px;
                    height:50px;
                    font-size:15px;
                    display:flex;
                    justify-content:center;
                    align-items:center;
                    border-radius:3px;
                    background:$prime-color;
                    color:white;
                    text-transform:uppercase;
                    margin:0;
                }
            }

            .carousel-wrapper{ 
                width:100%;
                height:100%;
position:absolute;
top:0;
left:0;
            }
        }
    }
}
</style>
