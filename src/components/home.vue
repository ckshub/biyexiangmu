<template>
	<div class="home" @click="jump($event)">
		<div class="markdown"><i class="iconfont icon-tongxunlu"></i></div>
		<div class="tree"></div>
		<div class="time"></div>
		<div class="friend"></div>
	</div>
</template>

<script>
export default {
	methods: {
		jump(e) {
			console.log(e.toElement.className);
			this.$router.push({ path: `/${e.toElement.className}` });//跳转到相应的页面
		}
	}
};
</script>

<style scss>
.home {
	height: 100vh;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-wrap: wrap;
}

.markdown {
	height: 50%;
	width: 50%;
	background-color: #2c3e50;
}

.tree {
	height: 50%;
	width: 50%;
	background-color: #42b983;
}

.time {
	height: 50%;
	width: 50%;
	background-color: #bcdef3;
}

.friend {
	height: 50%;
	width: 50%;
	background-color: aquamarine;
}
</style>
