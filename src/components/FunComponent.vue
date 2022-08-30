<template>
    <div>
        <button id = "button1">Button</button>
        <section v-for="(secret, index) in secrets" :key="index" >
         <div @click="changeColor" >
        
            <p >{{secret}}</p>
         </div>
        </section>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                secrets: [`aa`, `bb`, `cc`, `dd`],
                // alternative method of changing color by adding css component to data ( :style "myStyle" )add to element
                myStyle:{
                background: "pink"
            },
            pinkPink: false,
            isPink: false
            }
        },
        mounted () {
            document.getElementById(`button1`).addEventListener(`click`, this.turn_blue);
            
        },
        name: 'fun-component',

        methods: {
            turn_blue() {
                      document.body.insertAdjacentHTML(`beforeend`, '<h1>testing to see if works</h1>');
        document.body[`style`][`background`]= 'blue';
            },
            // using details and target allows for individual target of the element
          changeColor(aaaaa) {
            this.isPink = !this.isPink;
            if (this.isPink) {
                aaaaa.target.style.background = "pink";
            } else {
                aaaaa.target.style.background = "transparent";
            }
          
          }
        }
       
        }
        

    
        
    
   
 
    
</script>

<style scoped>

.pinkPink {
    
 
}
</style>