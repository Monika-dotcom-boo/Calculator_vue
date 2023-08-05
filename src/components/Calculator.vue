<template>
    <div class="Hello"></div>
    <h1 class='text-center'>{{msg}}</h1>

    <div class="col-md-4 m-3">
        <table class="table table-bordered text-center ">
        <tr class="output">
            <td colspan="4">
                {{output || 0 }}
            </td>
        </tr>
  <tbody>
    <tr>
      <td v-on:click="clearField">C</td>
      <td v-on:click="setNagativerOrPosiive">+/-</td>
      <td v-on:click="calculatePercenage">%</td>
      <td class="lastColumn"><svg width="10px" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path fill="#fff" d="M272 96a48 48 0 1 0 -96 0 48 48 0 1 0 96 0zm0 320a48 48 0 1 0 -96 0 48 48 0 1 0 96 0zM400 288c17.7 0 32-14.3 32-32s-14.3-32-32-32H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H400z"/></svg></td>
    </tr>
    <tr>
        <td v-on:click="getNumber(7)">7</td>
        <td v-on:click="getNumber(8)">8</td>
        <td v-on:click="getNumber(9)">9</td>
        <td class="lastColumn">x</td>
    </tr>
    <tr>
        <td v-on:click="getNumber(4)">4</td>
        <td v-on:click="getNumber(5)">5</td>
        <td v-on:click="getNumber(6)">6</td>
        <td class="lastColumn">-</td>
    </tr>
    <tr>
        <td v-on:click="getNumber(1)">1</td>
        <td v-on:click="getNumber(2)">2</td>
        <td v-on:click="getNumber(3)">3</td>
        <td class="lastColumn" 
        @click="processOutput">+</td>
    </tr>
    <tr>
        <td colspan="2" v-on:click="getNumber(0)">0</td>
        <td  v-on:click="getDok()">.</td>
        <td class="lastColumn">=</td>
    </tr>    
  </tbody>
</table>
    </div>
</template>



<script>
export default {
    props: {
        msg: String
    }, 
    data(){
        return{
            output: ""
        }
    }, 
    methods: {
        clearField() {
            this.output = 0;
        }, 
        setNagativerOrPosiive(){
            this.output = this.output[0] === '-' ? this.output.slice(1) : `-${this.output}`;
        }, 
        calculatePercenage(){
            this.output = parseFloat(this.output)/100; 
        }, 
        getNumber(number){
             this.output = `${this.output}${number}`
        }, 
        getDot(){
            if(this.output.indexOf('.') === -1){
                this.output = this.output+'.';
            }
        }, 
        processOutput(){
            this.operation = (a,b) => {
            return parseFloat(a) + parseFloat(b) 
            }
        }, 
        updateOutput(){
            this.operation = ``
        }
    }
}

</script>

<style scoped>
    .output{
        background-color: #333;
        color:#fff;
    }
    .lastColumn{
        background-color: orange;
        color:#fff;
    }
    .lastColumn:active{
        background-color: #333;
        color:#fff;
    }

</style>