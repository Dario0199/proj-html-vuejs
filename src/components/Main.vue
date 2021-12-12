<template>
  <main>
    <div class="card-info">
        <div class="container d-flex">
            <div v-for="(card, index) in cards" :key="`card-${index}`" class="card">
                <i :class="`${card.icon}`"></i>
                <h4>{{ card.title }}</h4>
                <span>{{ card.text }}</span>
            </div>
        </div>
    </div>
    <div class="company d-flex">
        <div class="company-txt ">
            <h5>about the network</h5>
            <h1 class="d-flex"> 
                <div class="h1-bg d-flex">The</div> 
                Company
            </h1>
            <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras iaculis diam varius diam ultricies lacinia.</span>
            <div class="d-flex mt-3">
                <div v-for="(card, index) in cardsCompany" :key="`company-${index}`" class="card-company">
                    <h2>{{ card.number }}</h2>
                    <h4>{{ card.title }}</h4>
                    <span>{{ card.text }}</span>
                </div>
            </div>
            <button class="b-left">get in touch</button>
            <button class="b-right">read more</button>
        </div>
        <img src="../assets/about-5.jpg" alt="">
    </div>
    <div class="projects">
        <div class="container d-flex flex-column align-items-center">
            <h5>we do more for everyone</h5>
            <h1 class="d-flex">
                Actions & 
                <div class="h1-bg">Projects</div> 
            </h1>
            <div class="menu-bar">
                <ul class="link">
                    <li v-for="(link, index) in menuLinks" :key="`link-${index}`">
                        <a :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
            </div>
            <div class="projercts-card">
                <div class="card">
                    <img src="../assets/project-1.jpg" alt="">
                    <h5>Academic professional program in social media</h5>
                </div>
                <div class="card">
                    <img src="../assets/project-2.jpg" alt="">
                    <h5>President's speech at the annual meeting</h5>
                </div>
                <div class="card">
                    <img src="../assets/project-3.jpg" alt="">
                    <h5>International business trip in Shanghai</h5>
                </div>
                <div class="card">
                    <img src="../assets/project-4.jpg" alt="">
                    <h5>Technology workshop with education theme</h5>
                </div>
                <div class="card">
                    <img src="../assets/project-5.jpg" alt="">
                    <h5>Donation of clothes and food to the partner NGO</h5>
                </div>
                <div class="card">
                    <img src="../assets/project-6.jpg" alt="">
                    <h5>Confraternization of the procurement team</h5>
                </div>
            </div>
        </div>
    </div>
    <div class="men">
    <div class="management d-flex align-items-center flex-column">
        <h5>how it works in practice</h5>
        <h1 class="d-flex">
            <div class="h1-bg">
                Process
            </div>
            Menagement
        </h1>
        <span>We work with innovative methodologies to ensure that the entire reformatting process is done from start to finish as planned.</span>
        <div class="point-bar">
            <div class="bar">
                <div class="content d-flex justify-content-around">
                    <div v-for="(card, index) in pointCards" :key="`point-${index}`" class="cards">
                        <div class="d-flex justify-content-center">
                            <h5>{{ card.number }}</h5>
                        </div>
                        <h4>{{ card.title }}</h4>
                        <span class="card-txt">{{ card.text }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    </div>
    <div class="feedback">
        <div class="container">
            <h5>customer testimonials</h5>
            <h1 class="d-flex justify-content-center">
                Trusted
                <div class="h1-bg">
                    Feedback
                </div>
            </h1>
            <span>We work intensively in search of ideals that can add up in the lives of our customers. This is what moves us and we are grateful for the recognition.</span>
            <div class="feed-card d-flex">
                <div class="card">
                    <img src="../assets/logo-1.png" alt="">
                    <span class="txt" c>Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.</span>
                    <span class="txt">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span>
                    <i class="fas fa-quote-right"></i>
                </div>
                <div class="card">
                    <img src="../assets/logo-2.png" alt="">
                    <span class="txt">Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.</span>
                    <span class="txt">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span>
                    <i class="fas fa-quote-right"></i>
                </div>
                <div class="card">
                    <img src="../assets/logo-3.png" alt="">
                    <span class="txt">Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.</span>
                    <span class="txt">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span>
                    <i class="fas fa-quote-right"></i>
                </div>
            </div>
        </div>
    </div>
  </main>
</template>

<script>
export default {
    name: 'Main',
    data(){
        return{
            cards: [
                {
                    icon: 'fas fa-user-friends',
                    title: 'Human Capital',
                    text: 'Humanizing business: Harness the power of technology to improve the way people work.'
                },
                {
                    icon: 'fas fa-chart-pie',
                    title: 'Core Business',
                    text: 'It takes innovative approaches to transform, modernize, and run existing platforms.'
                },
                {
                    icon: 'fab fa-cloudscale',
                    title: 'Performance',
                    text: 'Achieving maximum impact and value from investments in finance and supply chain.'
                }
            ],
            cardsCompany: [
                {
                    number: 0,
                    title: 'Employees',
                    text: 'Lorem ipsum dolor sit amet'
                },
                {
                    number: 0,
                    title: 'Partners',
                    text: 'Lorem ipsum dolor sit amet'
                },
                {
                    number: 0,
                    title: 'Customers',
                    text: 'Lorem ipsum dolor sit amet'
                },
            ],
            menuLinks:[
                {
                    text: 'all',
                    url: '/',
                },
                {
                    text: 'institutional',
                    url: '/',
                },
                {
                    text: 'social',
                    url: '/',
                },
                {
                    text: 'events',
                    url: '/',
                },
                {
                    text: 'innovation',
                    url: '/',
                },
                    {
                    text: 'environment',
                    url: '/',
                },
                    {
                    text: 'technology',
                    url: '/',
                },
            ],
            // projectCards:[
            //     {
            //         image: '1',
            //         text: 'Academic professional program in social media'
            //     },
            //     {
            //         image: '2',
            //         text: "President's speech at the annual meeting"
            //     },
            //     {
            //         image: '3',
            //         text: 'International business trip in Shanghai'
            //     },
            //     {
            //         image: '4',
            //         text: 'Technology workshop with education theme'
            //     },
            //     {
            //         image: '5',
            //         text: 'Donation of clothes and food to the partner NGO'
            //     },
            //     {
            //         image: '6',
            //         text: 'Confraternization of the procurement team'
            //     }
            // ]
            pointCards:[
                {
                    number: '01',
                    title: 'Collection of information',
                    text: 'Lorem ipsum dolor sit amet consectetur'
                },
                {
                    number: '02',
                    title: 'Strategic planning',
                    text: 'Lorem ipsum dolor sit amet consectetur'
                },
                {
                    number: '03',
                    title: 'assignment of resposibilities',
                    text: 'Lorem ipsum dolor sit amet consectetur'
                },
                {
                    number: '04',
                    title: 'Formatting process',
                    text: 'Lorem ipsum dolor sit amet consectetur'
                },
                {
                    number: '05',
                    title: 'Continuity formalization',
                    text: 'Lorem ipsum dolor sit amet consectetur'
                }
            ],
            feedbackCards:[
                {
                    image: '1',
                    text1: 'Praesent volutpat justo sit amet elementum malesuada. Praesent sagittis augue justo, in accumsan orci rhoncus at pellentesque.',
                    text2: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.card-info{
    background: #e4eae6;
    padding: 70px 0;
    .card{
        width: calc(100% / 3);
        background: white;
        margin: 40px 20px;
        padding: 60px 40px;
        border: none;
        border-radius: 10px;
        
        h4{
            margin-bottom: 30px;
            font-weight: 700;
        }
        i{
            color: #038483;
            background: #03848441;
            font-size: 30px;
            width: 60px;
            height: 60px;
            margin-bottom: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 50%;
        }
    }
}
.company{

    .company-txt{
        width: 50%;
        padding-left: 110px;
        padding-right: 80px;
        padding-top: 80px;

        h5{
            color: #1a948f;
            text-transform: uppercase;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 20px;
        }
        h1{
            color: black;
            font-weight: 800;
            font-size: 50px;
            margin-bottom: 10px;

            .h1-bg{
                padding-left: 10px;
                color: #038483;
                background: #03848441;
                width: 110px;
                margin-right: 10px;
            }
        }
        span{
            font-size: 16px;
            color: #85878b;
            margin-bottom: 30px;
        }
        .card-company{
            width: calc(100% / 3);

            h2{
                color: #038483;
                margin-left: 15px;
                font-weight: 600;
            }
            h4{
                font-weight: 600;
            }
        }
        button{
            text-transform: uppercase;
            margin-top: 30px;
            margin-right: 15px;
            color: white;
        }
            .b-left{
                border: none;
                background: #1a948f;
                border-radius: 3px;
                width: 130px;
                height: 35px;
            }
            .b-right{
                width: 130px;
                height: 35px;
                background: none;
                color: #1a948f;
                border-radius: 3px;
                border: 2px solid #1a948f;
            }
    }
    img{
        width: 50%;
        height: 550px;
        object-fit: cover;
    }
}
.projects{
    background: black;

    .container{
        padding-top: 80px;
        h5{
            color: #1a948f;
            text-transform: uppercase;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 30px;
        }
        h1{
            color: white;
            font-weight: 800;
            font-size: 50px;
            margin-bottom: 30px;
            
            .h1-bg{
                padding-left: 10px;
                background: #03848441;
                width: 220px;
                margin-left: 10px;
            }
        }
        .menu-bar{
            margin-bottom: 30px;
            ul{
                display: flex;
                align-items: center;
                list-style: none;
                margin-top: 20px;
                li{
                    margin-left: 40px;
                    a{
                        text-decoration: none;
                        text-transform: uppercase;
                        color: white;
                        font-size: 14px;
                        font-weight: 600;
                        &:hover{
                            background: #03848441;
                            height: 25px;
                        }
                    }
                }
            }
        }
        .projercts-card{
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            .card{
                width: 400px;
                border: none;
                margin-bottom: 45px;
                background: none;
                &::after{
                    position: absolute;
                    content: '';
                    width: 100%;
                    height: 100%;
                    background-color: black;
                    opacity: 0.4;
                    z-index: 0;
                }

                img{
                    position: relative;
                    border-radius: 20px;
                }
                h5{
                    position: absolute;
                    text-align: center;
                    color: white;
                    z-index: 5;
                    left: 50%;
                    transform: translateX(-50%);
                    bottom: 15px;
                }
            }
        }
    }
}
.management{
    margin-bottom: 250px;
    h5{
        color: #038483;
        text-transform: uppercase;
        font-size: 14px;
        font-weight: 600;
        margin-top: 70px;
        margin-bottom: 30px;
    }
    h1{
        color: black;
        font-weight: 800;
        font-size: 50px;
        margin-bottom: 30px;
        
        .h1-bg{
            color: #038483;
            padding-left: 15px;
            background: #03848441;
            width: 220px;
            margin-right: 10px;
        }
    }
    span{
        text-align: center;
        font-size: 16px;
        color: #85878b;
        margin-bottom: 50px;
        width: 700px;
    }
    .point-bar{
        width: 100%;
        .bar{
            width: 100%;
            height: 4px;
            background-color: #03848441;
            position: relative;
        }
        .content{
            position: absolute;
            top: -85px;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            .cards{
            width: 15%;
            text-align: center;
            
                h5{
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    background: #bee0e0;
                    color: #038483;
                    font-weight: 700;
                    border-radius: 50%;
                    width: 35px;
                    height: 35px;
                    margin-left: 10px;
                    margin-bottom: 20px;
                    text-align: center;
                }
                h4{
                    text-align: center;
                    margin-bottom: 20px;
                    font-weight: 600;
                }
            }
        }
    }
}
.feedback{
    background: #e4eae6;
    padding: 70px 0;
    text-align: center;

    h5{
        color: #038483;
        text-transform: uppercase;
        font-size: 14px;
        font-weight: 600;
        margin-top: 70px;
        margin-bottom: 30px;
    }
    h1{
        color: black;
        font-weight: 800;
        font-size: 50px;
        margin-bottom: 30px;
        
        .h1-bg{
            color: #038483;
            background: #03848441;
            width: 250px;
            margin-left: 10px;
            text-align: center;
        }
    }
    span{
        
        font-size: 16px;
        color: #85878b;
        width: 700px;
    }
    .card{
        width: calc(100% / 3);
        background: white;
        margin: 40px 20px;
        padding: 60px 40px;
        border: none;
        border-radius: 10px;
        position: relative;
        
        img{
            width: 150px;
            margin-bottom: 20px;
        }
        .txt{
            width: 100%;
            margin-bottom: 15px;
            text-align: start;   
        }
        i{
            position: absolute;
            bottom: 70px;
            right: 20px;
            font-size: 40px;
            color: #85878b;
        }
    }
}

</style>