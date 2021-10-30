<template>
  <el-form
    :model="controls"
    :rules="rules"
    ref="form"
    @submit.native.prevent="onSubmit"
  >
    <h2>Добавить комментарий</h2>
    <el-form-item label="Ваше имя" prop="name">
      <el-input v-model.trim="controls.name" />
    </el-form-item>
    <el-form-item label="Ваш комментарий" prop="text">
      <el-input
        type="textarea"
        v-model="controls.text"
        resize="none"
        :rows="2"
      />
    </el-form-item>
    <el-form-item>
      <el-button
        type="primary"
        native-type="submit"
        round
      >
        Добавить комментарий
      </el-button>
    </el-form-item>
  </el-form>
</template>

<script>
    export default {
      data() {
        return {
          controls: {
            name: '',
            text: ''
          },
          rules: {
            name: [
              { required: true, message: 'Имя не должно быть пустым', trigger: 'blur' }
            ],
            text: [
              { required: true, message: 'Введите ваш комментарий', trigger: 'blur' }
            ]
          }
        }
      },
      methods: {
        onSubmit() {
          this.$refs.form.validate(valid => {
            if (valid) {
              console.log('Form is submit')
            } else {
              console.log('error submit!!');
              return false;
            }
          });
        }
      }
    }
</script>

<style scoped>

</style>
