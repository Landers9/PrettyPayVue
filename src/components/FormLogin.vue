<template>
  <el-row :gutter="0" type="flex" justify="center">
    <el-col :xs="20" :sm="10" :md="8">
      <el-card class="box-card">
        <h4>Enter your email and password to continue</h4>
        <el-form :model="formLabelAlign">
          <el-form-item>
            <el-input
              v-model="formLabelAlign.name"
              placeholder="Email"
            ></el-input>
          </el-form-item>
          <el-form-item>
            <el-input
              v-model="formLabelAlign.region"
              placeholder="Password" 
            ></el-input>
          </el-form-item>
          <el-form-item>
            <el-button type="primary" class="btn-send" @click="submitForm('numberValidateForm')">Sign in
            </el-button>
          </el-form-item>
          <h5>You don't have account ?</h5>
          <el-form-item>
            <el-button type="primary" class="btn-inscription" @click="submitForm('numberValidateForm')">Sign up
            </el-button>
          </el-form-item>
        </el-form>
        <h5><a href="#">Password forgot ?</a></h5>
      </el-card>
    </el-col>
  </el-row>
</template>

<script>
export default {
  data() {
    return {
      labelPosition: "left",
      formLabelAlign: {
        name: "",
        region: "",
        type: "",
      },
    };
  },
};
</script>

<style scoped>
.text {
  font-size: 14px;
}

.item {
  padding: 18px 0;
}

.box-card {
  width: 100%;
}

.btn-send {
  width: 100%;
  color:#fff;
}

.btn-inscription{
  width: 100%;
  background-color: #000;
  color:#fff;
  border: none;
}

a{
    text-decoration: none;
    color:rgb(37, 71, 182);
}
</style>
