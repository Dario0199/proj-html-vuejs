<template>
  <main>
    <div class="card-info">
        <div class="container d-flex">
            <div v-for="(card, index) in cards" :key="`card-${index}`" class="card">
                <i :class="`${card.icon}`"></i>
                <h4>{{ card.title }}</h4>
                <span>{{ card.text }}</span>
            </div>
            <!-- <div class="card">
                <i class="fas fa-chart-pie"></i>
                <h4>Core Business</h4>
                <span>It takes innovative approaches to transform, modernize, and run existing platforms.</span>
            </div>
            <div class="card">
                <i class="fab fa-cloudscale"></i>
                <h4>Performance</h4>
                <span>Achieving maximum impact and value from investments in finance and supply chain.</span>
            </div> -->
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

</style>