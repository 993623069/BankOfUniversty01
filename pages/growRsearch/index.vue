<template>
	<view class="grow-rsearch">
		<view class="header">
			<image src="../../static/grow-rsearch-bg.png" class="grow-rsearch-bg"></image>
			<view class="header-img-list">
			   <image src="../../static/grow-rsearch-logo.png" class="grow-rsearch-logo"></image>
				<image src="../../static/grow-rsearch-title.png" class="grow-rsearch-title"></image>
				<image src="../../static/grow-rsearch-laotouer.png" class="grow-rsearch-laotouer"></image>
			</view>
			
		</view>
		<view class="content-list">
			  <image v-for="(item,imgIndex) in imgList" :src="item.path" class="grow-rsearch-list" :key="imgIndex"></image>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgList:[
					{path:'../../static/grow-rsearch-list01.png',uuid:''},
					{path:'../../static/grow-rsearch-list01.png',uuid:''},
				    {path:'../../static/grow-rsearch-list01.png',uuid:''},
					{path:'../../static/grow-rsearch-list01.png',uuid:''},
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.grow-rsearch{
	border: 2px solid #FF8802;
	margin: 10px 10px;
	background-color: #FFE7CC;
	min-height: 100%;
}
.grow-rsearch-bg{
	width: 100%;
	height: 650upx;
}
.header{
	display: flex;
	flex-direction: column;
}
.header-img-list{
	position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: auto;
    width: 100%;
    align-items: center;
}
.grow-rsearch-logo{
	width:200px;
	margin: 20px 0;
	height: 35px;
	
}
.grow-rsearch-title{
	width:750upx;
	height: 100px;
	position: relative;
	left: -12px;
}
.grow-rsearch-laotouer{
	width: 260px;
	position: relative;
	left: -12px;
	top: -16px;
}
.content-list{
	margin-top: 85px;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
.grow-rsearch-list{
	width:260px;
	margin: 10px 0;
	height: 45px;
}
</style>
