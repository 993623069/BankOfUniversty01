
<template>
	<view class="honorary-archives">
		<!--01------------头部背景图---------------------->
		<view class="header-banner" >
			 <button @click="pageBack" class="page-back">< 返回</button>
			 <view class="center-font-container">
				 <image class="center-font" src="../../static/honorary-archives-text.png"></image>
			 </view>
		    <view class="header-tab-list">
				<ul class="header-tab-list-container">
					<li v-for="(item,index) in tabList" 
					   :key="index" 
					    @click="changeTab(item,index)" 
						class="header-tab"
						:class="{'fontWeight':tabActiveIndex === item.index}">
						{{item.text}}
					</li>
				</ul>
			</view>
		</view>
		<!-- --02---------------列表内容----------------- -->
		<view class="body-content">
			<myTeam v-if="tabActiveIndex===0"/>
			<certifyInfor v-if="tabActiveIndex===1"/>
			<scoreRank v-if="tabActiveIndex===2"/>
		</view>
	</view>
</template>

<script>
	import scoreRank  from '../../components/scoreRank'
	import certifyInfor  from '../../components/certifyInfor'
	import myTeam  from '../../components/myTeam'
	export default {
		components:{
			scoreRank,
			certifyInfor,
			myTeam
		},
		data() {
			return {
				tabActiveIndex:0,
				title: 'Hello',
				tabList:[
					{text:'我的社团',index:0},
					{text:'社交证',index:1},
					{text:'积分排行',index:2}
				],
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
				
			},
			changeTab(item,index){
				this.tabActiveIndex=item.index
			}
		}
	}
</script>

<style>
.honorary-archives{
	background-color: #A10024;
	min-height: 100%;
	height:auto;
	display: flex;
	flex-direction: column;
	background: linear-gradient( #D80E2D,#A10024); /* 标准的语法 */
}
.header-banner{
	width: 750upx;
	height: 550upx;
	background-image: url(../../static/honorary-archives-bg.png);
	background-repeat: no-repeat;
	background-size: 100%;
	padding-bottom: 30px;
}
.page-back{
	border-radius: 10px;
	border: 1px solid #FFFFFF;
	background-color: #B50029;
	color:#FFFFFF;
	width:80px;
	height: 30px;
	font-size:14px;
	position: absolute;
	top:20px;
	left:10px;
	line-height: 1.8;
	
}
.center-font-container{
	margin-top: 40px;
	display: flex;
	position: relative;
	top: 90px;
	justify-content: center;
}
.center-font{
	width: 210px;
	height: 60px;
}
.un-center-border-bg{
	width:100%;
	height: 40px;
	margin:0 10px;
}
////////////
.header-tab-list{
	position: relative;
	top:240upx;
	padding: 10px;
	background-color: #FA2858;
	margin: 0 15px;
	border-radius: 8px;
	box-shadow: #ae0228 0px 0px 10px;
}
.header-tab-list-container{
	margin: 0 10px;
	display: flex;
}
.header-tab{
	flex:1;
	color:#FFFFFF;
	text-align: center;
}
.header-tab:nth-child(2){
	border-left: #FFFFFF 1px solid;
	border-right: #FFFFFF 1px solid;
}
////////////
.body-content{
	flex:1;
	border-top-left-radius: 15px;
	border-top-right-radius: 15px;

	margin-top: -15px;
}
.fontWeight{
	font-weight: 600;
}
</style>
