<template>
    <div>
        <button id = "button1">Button</button>
        <section v-for="(secret, index) in secrets" :key="index"  :class="{pinkPink}" @click = "pinkPink = !pinkPink">
           
            <p >{{secret}}</p>
        
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
            pinkPink: false
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
          
        }
       
        }
        

    
        
    
   
 
    
</script>

<style scoped>
.pinkPink {
    
    background: pink;
}
</style>