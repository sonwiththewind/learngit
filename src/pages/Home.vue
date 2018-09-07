<!-- Home.vue -->
<template>
	<div class="container">
		<!-- 由于html不区分大小写，所以js中驼峰命名方式在html中要改成用短横线连接的形式 -->
		<home-header></home-header>
		<div class="content">
			<ul class="cont_ul">
				<list
					v-for="item in items"
					key = "index"
					:price="item.price"
					:title="item.title">
				</list>
			</ul>
		</div>
	</div>
</template>
<style>
	.container {
		max-width: 640px;
		margin: 0 auto;
		overflow-x: hidden;
	}
	.cont_ul {
		padding-top: 0.05rem;
		margin: 0 -0.12rem;
	}
	.cont_ul:after {
		content: "";
		display: block;
		width: 0;
		height: 0;
		clear: both;
	}
</style>
<script>
	// 导入要用到的子组件
	import HomeHeader from '../components/HomeHeader'
	import List from '../components/List'
 
	export default {
		data () {
			return {
				items: [
					{ price: "1999.00", title: "m1固定版" },
					{ price: "2999.00", title: "m1万能安装版" },
//					{ price: "399.00", title: "" },
//					{ price: "998.00", title: "孟子" },
//					{ price: "99.00", title: "道德经" },
//					{ price: "89.00", title: "老子" },
//					{ price: "188.00", title: "金刚经" },
//					{ price: "209.00", title: "易筋经" },
				]
			}
		},
		// 在components字段中，包含导入的子组件
		components: {
			HomeHeader,
			List
		}
	}
</script>
