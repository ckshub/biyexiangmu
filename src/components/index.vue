<template>
	<div class="login">
		<el-form class="form" :rules="rules" :model="form" ref="form">
			<h3>登录界面</h3>
			<el-form-item label="用户名" label-width="80px" prop="name"><el-input class="item" v-model="form.name"></el-input></el-form-item>
			<el-form-item label="密码" label-width="80px" prop="password"><el-input class="item" type="password" v-model="form.password"></el-input></el-form-item>
			<el-form-item><el-button type="primary" @click="onSubmit">登录</el-button></el-form-item>
		</el-form>
	</div>
</template>

<script>
export default {
	data() {
		return {
			form: {},
			rules: {
				name: [{ required: true, message: '请输入用户名', trigger: 'blur' }, { min: 3, max: 5, message: '长度在 3 到 5 个字符', trigger: 'blur' }],
				password: [{ required: true, message: '请输入密码', trigger: 'blur' }, { min: 6, max: 12, message: '长度在 6 到 12 个字符', trigger: 'blur' }]
			}
		};
	},
	methods: {
		onSubmit() {
			this.$refs['form'].validate(valid => {
				if (valid) {
					this.$router.push('/home');
				} else {
					return false;
				}
			});
		}
	}
};
</script>

<style scoped>
.login {
	background-color: #bcdef3;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
}
.form {
	width: 40%;
	margin-bottom: 20vh;
	background-color: white;
	border-radius: 2px;
	padding: 5% 3%;
}
.item {
	width: 75%;
}
</style>
