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
              <input v-model="selected_number" type="number" min=1 />
            </td>
            <td>
              <input v-model="calc_count" type="number" min="1" />
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
      <table border="1">
        <thead>
          <tr>
            <th>value1</th>
            <th>type</th>
            <th>value2</th>
            <th>=</th>
            <th>ans</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="n in parseInt(calc_count)">
            <td>{{selected_number}}</td>
            <td>{{type}}</td>
            <td>{{n}}</td>
            <td>=</td>
            <td v-if="type=== '+'">{{n+parseInt(selected_number)}}</td>
            <td v-else-if="type=== '-'">{{n-parseInt(selected_number)}}</td>
            <td v-else-if="type=== '*'">{{n*parseInt(selected_number)}}</td>
            <td v-else-if="type=== '/'">{{n/parseInt(selected_number)}}</td>
          </tr>
        </tbody>
      </table>
    </div>
</template>

<script>
    export default {
        name: "Calc",
        data(){
          return{
            name:'calc',
            type:'',
            calc_count:1,
            selected_number:1

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
