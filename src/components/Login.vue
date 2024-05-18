<script lang="ts">
import {
  ElContainer,
  ElMain,
  ElCard,
  ElRow,
  ElForm,
  ElFormItem,
  ElInput
} from 'element-plus'

import { reactive } from 'vue'

const ruleForm = reactive({
  pass: '',
  checkPass: '',
  age: '',
})

export default {
  components: {
    ElContainer,
    ElMain,
    ElCard,
    ElRow,
    ElForm,
    ElFormItem,
    ElInput
  },
  data() {
    return {
      ruleForm: {
        pass: '',
        checkPass: '',
        age: '',
      },
    };
  },
}
</script>

<template>
  <div class="common-layout">
    <el-container>
      <el-main label-position="left" label-width="auto">
        <el-row class="row-bg" justify="center">
          <el-card>
            <p v-for="o in 4" :key="o" class="text item">{{ 'List item ' + o }}</p>
            <el-form>
              <el-form-item label="Name">
                <el-input />
              </el-form-item>
              <el-form-item label="Password" prop="pass">
                <el-input type="password" autocomplete="off" />
              </el-form-item>
            </el-form>
          </el-card>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<style scoped></style>
