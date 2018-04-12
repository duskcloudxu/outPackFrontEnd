<template>
	<div class="manage_page fillcontain">
		<el-row style="height: 100%;">
	  		<el-col :span="4"  style="min-height: 100%; background-color: #324057;">
				<el-menu :default-active="defaultActive" style="min-height: 100%;" theme="dark" router>
					<el-menu-item index="manage"><i class="el-icon-menu"></i>首页</el-menu-item>
					<el-submenu index="2">
						<template slot="title"><i class="el-icon-document"></i>合同模板</template>
						<el-menu-item index="userList">模板库</el-menu-item>
						<el-menu-item index="shopList">我的模板</el-menu-item>
						<el-menu-item index="foodList">委托起草</el-menu-item>
					</el-submenu>
					<el-submenu index="3">
						<template slot="title"><i class="el-icon-plus"></i>帮审合同</template>
					</el-submenu>
					<el-submenu index="4">
						<template slot="title"><i class="el-icon-star-on"></i>合同管理</template>
						<el-menu-item index="document">全部文件</el-menu-item>
                        <el-menu-item index="">待自己签</el-menu-item>
                        <el-menu-item index="">待他人签</el-menu-item>
                        <el-menu-item index="">已完成</el-menu-item>
                        <el-menu-item index="">已过期</el-menu-item>
                        <el-menu-item index="">已撤销</el-menu-item>
                        <el-menu-item index="">已拒签</el-menu-item>
                        <el-menu-item index="">草稿箱</el-menu-item>
					</el-submenu>
                    <el-submenu index="5">
                        <template slot="title"><i class="el-icon-setting"></i>账号设置</template>
                    </el-submenu>

				</el-menu>
			</el-col>
			<el-col :span="20" style="height: 100%;overflow: auto;">
				<keep-alive>
				    <router-view></router-view>
				</keep-alive>
			</el-col>
		</el-row>
    </div>
</template>

<script>
    import ElCol from "element-ui/packages/col/src/col";
    export default {
        components: {ElCol},
        computed: {
			defaultActive: function(){
				return this.$route.path.replace('/', '');
			}
		},
    }
</script>


<style lang="less" scoped>
	@import '../style/mixin';
	.manage_page{

	}
</style>
