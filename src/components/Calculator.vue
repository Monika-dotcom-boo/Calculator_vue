<template>
    <div class="Hello"></div>
    <h1>{{msg}}</h1>

    <div class="col-md-4 m-3">
        <table class="table table-bordered">
  <tbody>
    <tr>
      <td>C</td>
      <td>+/-</td>
      <td>%</td>
      <td class="lastColumn"><svg width="10px" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M272 96a48 48 0 1 0 -96 0 48 48 0 1 0 96 0zm0 320a48 48 0 1 0 -96 0 48 48 0 1 0 96 0zM400 288c17.7 0 32-14.3 32-32s-14.3-32-32-32H48c-17.7 0-32 14.3-32 32s14.3 32 32 32H400z"/></svg></td>
    </tr>
    <tr>
        <td>7</td>
        <td>8</td>
        <td>9</td>
        <td class="lastColumn">x</td>
    </tr>
    <tr>
        <td>4</td>
        <td>5</td>
        <td>6</td>
        <td class="lastColumn">-</td>
    </tr>
    <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
        <td class="lastColumn">+</td>
    </tr>
    <tr>
        <td colspan="2">0</td>
        <td>.</td>
        <td>=</td>
    </tr>    
  </tbody>
</table>
    </div>
</template>



<script>
export default {
    props: {
        msg: String
    }
}

</script>

<style scoped>
    .lastColumn{
        background-color: orange;
        color:#fff;
    }

    .lastColumn:active{
        background-color: #333;
        color:#fff;
    }
</style>