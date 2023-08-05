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
      <td>÷</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Larry</td>
      <td>the Bird</td>
      <td>@twitter</td>
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