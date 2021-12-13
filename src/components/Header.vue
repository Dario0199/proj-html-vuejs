<template>
    <header>
        <section class="top-bar">
            <div class="container d-flex justify-content-between">
                <div class="left">
                    <i class="fas fa-clock"></i>
                    <span>Open Hours: Mon - Sat - 9:00 - 18:00 </span>
                </div>
                <div class="right">
                    <ul class="d-flex">
                        <li>
                            <i class="fas fa-phone"></i>
                            <span>+1 (305) 1234 - 5678</span>
                        </li>
                        <li>
                            <i class="fas fa-envelope"></i>
                            <span>hello@example.com</span>
                        </li>
                        <li>
                            <i class="fab fa-facebook-f"></i>
                        </li>
                        <li>
                            <i class="fab fa-twitter"></i>
                        </li>
                        <li>
                            <i class="fab fa-linkedin-in"></i>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
        <section class="hero">
            <div class="container">
                <div class="nav-bar">
                    <img src="https://nexgen.codings.dev/wp-content/uploads/2021/03/logo.svg" alt="">
                    <div class="menu d-flex align-items-center">
                        <ul class="link">
                            <li v-for="(link, index) in navLinks" :key="`link-${index}`">
                                <!-- <a :class="{ active: link.current }" :href="link.url">{{ link.text }}</a> -->
                                <Menu 
                                :option="link.text"
                                :thumb="link.url"
                                :value="link.current"
                                />
                            </li>
                        </ul>
                        <a class="d-flex align-items-center" href="#">
                            <i class="far fa-user"></i>
                        </a>
                        <button>get in touch</button>
                    </div>
                </div>
                <div class="content">
                    <div class="text">
                        <h5>human resources</h5>
                        <h1>Get More</h1>
                        <h1>Productivity</h1>
                        <span>Planning, recruitment and selection process and performance evaluation of employees</span>
                    </div>
                    <div class="buttons">
                        <button class="b-left">get in touch</button>
                        <button class="b-right">read more</button>
                    </div>
                </div>
            </div>
            

        </section>
    </header>
</template>

<script>
import Menu from '@/components/Menu.vue';

export default {
    name: 'Header',
    components:{
        Menu,
    },
    data(){
        return{
            navLinks:[
                {
                    text: 'home',
                    url: '/',
                    current: false
                },
                {
                    text: 'about',
                    url: '/',
                    current: false
                },
                {
                    text: 'projects',
                    url: '/',
                    current: false
                },
                {
                    text: 'process',
                    url: '/',
                    current: true
                },
                {
                    text: 'testimonials',
                    url: '/',
                    current: false
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    .top-bar{
        background: #24343c;
        .container{
                align-items: center;
        }

        div{
            color: white;
            

            .right{
                li{
                    list-style: none;
                    margin-left: 30px;

                    i{
                        margin-right: 5px;   
                    }
                }
            }
        }
    }
    .hero{
        background-image: url('../assets/bg-4.jpg');
        width: 100%;
        height: 680px;
        background-size: cover;
        position: relative;
        display: flex;
        justify-content: space-around;
        &::after{
            position: absolute;
            content: '';
            width: 100%;
            height: 100%;
            background-color: black;
            opacity: 0.4;
            z-index: 0;
        }  
        .container{
            position: absolute;
            z-index: 10;
            
            .nav-bar{
                display: flex;
                width: 100%;
                display: flex;
                justify-content: space-between;
                img{
                    width: 120px;
                    margin-top: 15px;
                }
                .menu{
                    ul{
                        display: flex;
                        align-items: center;
                        list-style: none;
                        margin-top: 20px;
                        
                            // a{
                            //     text-decoration: none;
                            //     text-transform: uppercase;
                            //     color: white;
                            //     font-size: 14px;
                            //     font-weight: 600;
                            //     &.active,
                            //     &:hover{
                            //         color: #1a948f;
                            //     }
                            // }
                        
                    }
                    a{
                        margin-top: 4px;
                        color: white;
                        font-size: 14px;
                        font-weight: 600;
                        margin-left: 20px;
                        &:hover{
                            color: #1a948f;
                        }
                    }
                    button{
                        text-transform: uppercase;
                        background: #1a948f;
                        color: white;
                        border: none;
                        border-radius: 3px;
                        width: 130px;
                        height: 35px;
                        margin-left: 20px;
                        &:active{
                            background: white;
                            color: #1a948f;
                        }
                    }
                }
            }
            .content{
                margin-top: 150px;
                width: 30%;
                
                .text{

                    h5{
                        color: #1a948f;
                        text-transform: uppercase;
                        font-size: 14px;
                        font-weight: 600;
                    }
                    h1{
                        color: white;
                        font-weight: 800;
                        font-size: 50px;
                    }
                    span{
                        font-size: 16px;
                        color: #babdbe;
                    }
                }
                .buttons{
                    margin-top: 25px;
                    button{
                        text-transform: uppercase;
                        margin-right: 15px;
                        color: white;
                    }
                    .b-left{
                        border: none;
                        background: #1a948f;
                        border-radius: 3px;
                        width: 130px;
                        height: 35px;
                        &:active{
                            background: white;
                            color: #1a948f;
                        }
                    }
                    .b-right{
                        width: 130px;
                        height: 35px;
                        background: none;
                        border-radius: 3px;
                        border: 2px solid #1a948f;
                        &:active{
                            background: white;
                            color: #1a948f;
                            border: 2px solid #1a948f;

                        }
                    }
                }

            } 
        }
    }
</style>