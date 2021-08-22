
<template>
	<view class="function-center">
		<!--01------------头部背景图---------------------->
		<view class="header-banner" >
			 <button @click="pageBack" class="page-back">< 返回</button>
		     <image class="fun-center-font" src="/static/fun-center-font.png"></image>
			 <!-- <image class="fun-center-border-bg" src="/static/fun-center-border-bg.png"></image> -->
		</view>
		<!-- --02---------------列表内容----------------- -->
		<view class="text-area">
			<contentList :list="list1"/>
			<contentList :list="list2"/>
		</view>
	</view>
</template>

<script>
	import contentList  from '../../components/contentList/index.vue'
	export default {
		components:{
			contentList
		},
		data() {
			return {
				title: 'Hello',
				list1:
					{
						title:'初出茅庐',
						content:[
							{type:1,msg:'新冠病毒感染和肺炎防控知识的肺炎防控控知',status:1},
						    {type:1,msg:'新冠病毒感染和肺炎防控知识的肺炎防控控知',status:1},
						    {type:0,msg:'新冠病毒感染和肺炎防控知识的肺炎防控控知',status:0},
						]
					},
					list2:
						{
							title:'勇往之前',
							content:[
								{type:1,msg:'新冠病毒感染和肺炎防控知识的肺炎防控控知',status:1},
							    {type:1,msg:'新冠病毒感染和肺炎防控知识的肺炎防控控知',status:1},
							    {type:0,msg:'新冠病毒感染和肺炎防控知识的肺炎防控控知',status:0},
							]
						},
				
			}
		},
		onLoad() {

		},
		methods: {
			pageBack(){
				
			}
		}
	}
</script>

<style>
.function-center{
	background-color: #FFE7CD;
	min-height: 100%;
	height:auto;
}
.header-banner{
	width: 750upx;
	height: 550upx;
	background-image: url(../../static/fun-center-bg.png);
	background-repeat: no-repeat;
	background-size: 100%;
}
.page-back{
	border-radius: 10px;
	border: 1px solid #FFFFFF;
	color:#FFFFFF;
	width:80px;
	height: 30px;
	font-size:14px;
	background-color: rgba(0,0,0,0);
	position: absolute;
	top:10px;
	left:10px;
	line-height: 1.8;
	
}
.fun-center-font{
	width: 160px;
	height: 40px;
	position: absolute;
	right: 10px;
	top: 47px;
}
.un-center-border-bg{
	width:100%;
	height: 40px;
	margin:0 10px;
}
</style>
