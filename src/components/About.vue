<template>
  <h1>Liste des utilisateurs</h1>
  <!-- <el-table
    :data="
      users.filter(
        (data) =>
          !search || data.name.toLowerCase().includes(search.toLowerCase())
      )
    "
    style="width: 100%"
  >
    <el-table-column label="Date" prop="date"> </el-table-column>
    <el-table-column label="Email" prop="email"> </el-table-column>
    <el-table-column align="right">
      <template slot="header" slot-scope="scope">
        <el-input v-model="search" size="mini" placeholder="Type to search" />
      </template>
      <template slot-scope="scope">
        <el-button size="mini" @click="handleEdit(scope.$index, scope.row)"
          >Editer</el-button
        >
        <el-button
          size="mini"
          type="danger"
          @click="handleDelete(scope.$index, scope.row)"
          >Supprimer</el-button
        >
      </template>
    </el-table-column>
  </el-table> -->
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      users: [],
      search: "",
    };
  },
  methods: {
    handleEdit(index, row) {
      console.log(index, row);
    },
    handleDelete(index, row) {
      console.log(index, row);
    },
  },

  async created() {
    try {
      const res = await axios.get(`http://localhost:3001/users`);

      this.users = res.data;
    } catch (e) {
      console.error(e);
    }
  },
};
</script>
