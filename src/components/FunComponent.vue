<template>
    <div>
        <button id = "button1">Button</button>
    </div>
</template>

<script>
    export default {
        name: 'fun-component'
    }
        
    
    document.getElementById(`button1`).addEventListener(`click`, turn_blue)
    function turn_blue () {
        document.body.insertAdjacentHTML(`beforeend`, '<h1>testing to see if works</h1>');
        document.body[`style`][`background-color`]= 'blue';
    }
    
</script>

<style scoped>

</style>