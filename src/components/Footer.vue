<template>
  <footer>
    <div class="container d-flex">
        <div class="left">
            <h5>send a message</h5>
            <h1 class="d-flex">
                Get in  
                <div class="h1-bg">Touch</div> 
            </h1>
            <span>We will respond to your message as soon as possible</span>
            <div class="data-entry d-flex flex-wrap">
                <input type="text" placeholder="Name">
                <input type="text" placeholder="Email">
                <input type="text" placeholder="Phone">
                <select>
                    <option value="more-info">More Info</option>
                </select>
                <input class="text-msg" type="text" placeholder="Message">
                <button>send</button>
            </div>
            
        </div>
        <div class="right">
            <h4>Example Inc.</h4>
            <div class="txt">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</div>
            <div class="txt">Praesent diam lacus, dapibus sed imperdiet consectetur.</div>
            <div class="info d-flex">
                <i class="fas fa-phone d-flex"></i>
                +1.(305) 1234-5678
            </div>
            <div class="info d-flex d-flex">
                <i class="fas fa-envelope"></i>
                hello@example.com
            </div>
            <div class="info d-flex">
                <i class="fas fa-map-marker-alt"></i>
                Main Avenue, 987
            </div>
            <button>view map</button>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped lang="scss">
footer{
    background: black;

    .container{
        padding: 90px 0;
        .left{
            width: 60%;
            padding-right: 15px;
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
                text-align: center;
                
                .h1-bg{
                    background: #03848459;
                    width: 180px;
                    margin-left: 10px;
                }
            }
            span{
            font-size: 16px;
            color: #85878b;
            }
            .data-entry{
                justify-content: space-between;
                margin-top: 30px;
                
                input{
                    width: 49%;
                    padding: 5px;
                    margin-bottom: 15px;
                    background: #2c2c2c;
                    border: none;
                    border-radius: 3px;
                    color: #85878b;
                }
                select{
                    width: 49%;
                    margin-bottom: 15px;
                    background: #2c2c2c;
                    border: none;
                    border-radius: 3px;
                    color: #85878b;
                }
                .text-msg{
                    width: 100%;
                    height: 100px;
                }
                button{
                    border: none;
                    background: #1a948f;
                    border-radius: 3px;
                    width: 80px;
                    height: 35px;
                    color: white;
                    text-transform: uppercase;
                }
            }
            
        }
        .right{
            width: 40%;
            padding-left: 15px;

            h4{
                color: white;
                font-weight: 700;
                margin-bottom: 30px;
            }
            div{
                margin-bottom: 25px;
            }
            .txt{
                color: #85878b;   
            }
            .info{
                padding-top: 20px;
                color: #1a948f;
                align-items: center;
                i{
                    background: #03848459;
                    color: #1a948f;
                    border-radius: 50%;
                    width: 35px;
                    height: 35px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                }
            }
            button{
                border: 2px solid #1a948f;
                background:none;
                border-radius: 3px;
                width: 120px;
                height: 35px;
                color: white;
                text-transform: uppercase;
                margin-top: 20px;
            }
        }
    }
}
</style>