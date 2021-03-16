<template>
	<div class="markdown">
		<div class="left">
			<el-row class="tac">
				<el-col :span="12" style="width: 100%;">
					<el-menu
						default-active="2"
						class="el-menu-vertical-demo"
						background-color="#545c64"
						text-color="#fff"
						active-text-color="#ffd04b"
						@select="jump($event)"
						style="border: none;"
					>
						<el-menu-item index="随手记">
							<i class="el-icon-menu"></i>
							<span slot="title">随手记</span>
						</el-menu-item>
						<el-menu-item index="植树">
							<i class="el-icon-menu"></i>
							<span slot="title">植树</span>
						</el-menu-item>
						<el-menu-item index="日历">
							<i class="el-icon-menu"></i>
							<span slot="title">日历</span>
						</el-menu-item>
						<el-menu-item index="好友">
							<i class="el-icon-setting"></i>
							<span slot="title">好友</span>
						</el-menu-item>
					</el-menu>
				</el-col>
			</el-row>
		</div>
		<div class="content"></div>
		<div class="right"></div>
	</div>
</template>

<script>
export default {
	methods: {
		jump(e) {
			console.log(e);
		},
	}
};
</script>

<style scss>
.markdown {
	height: 100vh;
	width: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-wrap: wrap;
}

.left {
	width: 20%;
	height: 100vh;
	background-color: #2c3e50;
}

.content {
	flex: 1;
	height: 100vh;
	background-color: #42b983;
}

.right {
	width: 10%;
	height: 100vh;
	background-color: #bcdef3;
}
</style>
