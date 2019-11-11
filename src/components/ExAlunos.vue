<template>
<table>
    <thead>
    <tr>
      <th>Regional</th>
      <th>Média</th>
    </tr>
    </thead>

    <tbody>
      <tr v-for="exalunosData in exalunosDataList.regionals" :key="exalunosData.description" class="exalunos-data">
      <td>{{exalunosData.description}}</td>
      <td>{{exalunosData.average}}</td>
      </tr>
    </tbody>
</table>
</template>
<script>
export default {
  name: "ExAlunos",
  data() {
    return {
      exalunosDataList: []
    };
  },
  created: function() {
    this.getExAlunosData();
  },
  methods: {
    getExAlunosData() {
      fetch("exalunos.json")
        .then(response => response.json())
        .then(data => {this.exalunosDataList = data;
         })
   
  }
  }
};
</script>
<style>
table {
  font-family: 'Optima', sans-serif;
  width: 750px;
  border-collapse: collapse;
  border: 3px solid #44475C;
  margin: auto;

}

table th {
  text-transform: uppercase;
  text-align: center;
  background: #44475C;
  color: #FFF;
  padding: 8px;
  min-width: 30px;
}

table td {
  text-align: center;
  padding: 8px;
  border-right: 2px solid #7D82A8;
}
table td:last-child {
  border-right: none;
}
table tbody tr:nth-child(2n) td {
  background: #D4D8F9;
}
</style>