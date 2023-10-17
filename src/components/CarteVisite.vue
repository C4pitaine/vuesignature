<template>
    <div class="rectangle">       
        <div class="carte">
            <div class="name">
                <h5>{{  name }}</h5>
                <h6>{{ firstname }}</h6>
            </div>
            <div>{{ email }}</div>
            <div v-if="tel!==''">+32 {{ tel }}</div>
            <hr>
            <div v-if="citation!==''">" {{ citation.text }} " écrit par {{ citation.author }}</div>
        </div>
    </div>
</template>
    
    <script>
    export default {
      name: 'CarteVisite',
      props: {
        name: String,
        firstname: String,
        email: String,
        tel: String,
        citation: Object
      }
    }
    </script>
    
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style>
      .rectangle{
        width:100%;
        height:1000px;
        display: flex;
        justify-content: center;
        align-items: center;
        .carte{
            width:600px;
            height:400px;
            background-color: grey;
            text-align: start;

            .name{
                display: flex;
                margin: 20px;
                font-size: 30px;

                h6{
                    margin-left:20px;
                }
            }
            div{
                margin: 20px 20px;
                font-size: 22px;
            }
        }
      }
    </style>