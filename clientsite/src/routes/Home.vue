<template>
    <main>
       <header>
        <div class="top-header">
            <div class="logo">
                logo here
            </div>
            <div class="info-links">
               <div class="info-links-wrapper">
                <div class="content flex-row">
                    <div class="left-content"><i class="fa-solid fa-phone"></i></div>
                    <div class="right-content">
                        <a href="/">+237682449347</a>
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
            <div class="left-bottom-header"><i class="fa-solid fa-bars"></i></div>
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
                        <i class="fa-solid fa-cart-shopping"></i>
                    </button>
                    
                </div>
            </div>
        </div>
       </header>
       <div class="landing-page">

       </div>
    </main>
</template>

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
        border-bottom: 1px solid rgb(185, 184, 184);

        .top-header{ 
            width:100%;
            height:60%;
            display:flex;
            justify-content: space-between;
            align-items: center;
           

            .logo{ 
                width:20%;
                height:100%;
                display:flex;
                justify-content:center;
                align-items:center;
             
            }
            .info-links{ 
                width:35%;
                height:100%;
                display:flex;
                justify-content:center;
                align-items:center;

              .info-links-wrapper{ 
width:100%;
                  display: flex;
                  justify-content:space-evenly;
                  align-items: center;
                  .content{ 
                    width:43%;
                    height:80%;
                    display:flex;
                    align-items: center;
                    justify-content: center;
                    border:1px solid rgb(240, 238, 238);
                    background:rgb(253, 253, 253);

                    i{ 
                        color:$prime-color;
                    }
                    a{ 
                        color:rgb(116, 89, 89);
                    }

                    .left-content{ 
                        width:25%;
                        height:100%;
                        display:flex;
                        justify-content:flex-end;
                        align-items:center;

                        i{ 
                            font-size:23px;
                        }
                    }
                    .right-content{ 
                        width:75%;
                      
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
                            font-size:25px;
                            width:25%;
                            display:flex;
                            justify-content:center;
                            align-items:center;
                           
                        }
                        a{ 
                            width:75%;
                            display:flex;
                            font-size:14px;
                            justify-content:flex-start;
                            align-items:center;
                        }
                    }
                  }

                  .flex-row{ 
                    flex-direction: row;
                  }
                  .flex-column{ 
                    flex-direction:column;
                  }
              }
            }
        }

        .bottom-header{ 
            width:100%;
            height:40%;
            display:flex;
            justify-content:space-around;
            align-items:center;
          

            .left-bottom-header{ 
                width:10%;
                height:100%;
              cursor:pointer;
                display:flex;
                justify-content: center;
                align-items:center;

               i{ 
                    font-size:26px;
                }
            }
            .bottom-header-routes{ 
                width:60%;
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
                width:20%;
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
                                color:rgb(151, 149, 149);
                            }

                            &:hover{ 
                                background:rgb(219, 219, 219);
                            }
                        }
                    }
                }
            }
            .cart{ 
                width:8%;
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

                    button{ 
                        outline:none;
                        border:none;
                        background:none;

                        i{ 
                            font-size:28px;
                        }
                    }
                }
            }
        }
    }
}
</style>
