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
            <div class="d-flex mt-5">
                <div v-for="(card, index) in cardsCompany" :key="`company-${index}`" class="card-company">
                    <h2>{{ card.number }}</h2>
                    <h4>{{ card.title }}</h4>
                    <span>{{ card.text }}</span>
                </div>
            </div>
        </div>
        
        <img src="../assets/about-5.jpg" alt="">
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

    }
    img{
        width: 50%;
        height: 500px;
        object-fit: cover;
    }
}

</style>