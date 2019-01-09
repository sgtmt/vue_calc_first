<template>
    <div class="calc">
      <h1>{{name}}</h1>
      <table border="1">
        <thead>
        <tr>
          <th>段数</th>
          <th>計算回数</th>
          <th>符号</th>
        </tr>
        </thead>
        <tbody>
        <tr>
          <td>
            <input v-model="dan_count" type="number" min=1 />
          </td>
          <td>
            <input v-model="calc_count" type="number" min=1 max=9 />
          </td>
          <td>
            <select v-model="type">
            <option disabled value="">please typed</option>
            <option>+</option>
            <option>-</option>
            <option>*</option>
            <option>/</option>
            </select>
          </td>
        </tr>
        </tbody>
      </table>
      <p>計算結果</p>
    </div>
</template>

<script>
    export default {
        name: "Calc",
        data(){
          return{
            name:'calc',
            type:''
          }
        }
    }
</script>

<style scoped>
table{
  text-align: center;
  display: inline-block;
}
</style>
