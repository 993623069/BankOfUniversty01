<template>
	<view class="content-container">
		<view class="content-list">
			<view class="content-list-title">
				<image class="list-title-bg" src="../../static/content-list-title-bg.png"></image>
				<text class="list-title">{{list.title}}</text>
			</view>
			
		  <ul class="content-body-list">
			  <li v-for="(item,index) in list.content" :key="index">
				 <view class="body-content-img">
					 <image class="content-img-file" 
					 v-if="item.type == 0"
					 src="../../static/content-list-file.png"></image>
					 <image class="content-img" 
					 v-if="item.type == 1"
					 src="../../static/content-list-play.png"></image>
				 </view>
				 <view class="body-content">
					 {{item.msg}}
				 </view>
				  <view class="body-content-status">
					  <image 
					  class="content-status" 
					  v-if="item.status == 1"
					  src="../../static/content-list-finish.png"></image>
				  </view>
			  </li>
		  </ul>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			list:{
				type:Object,
				default:()=>{
					return []
				}	
			}

		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.content-container{
	padding: 15px;
	margin-top: 20px;
}
.content-list{
	width:100%;
	border: 3px solid #CF1440;
	border-radius: 5px;
}
.content-list-title{
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	color: #FFFFFF;
	position: relative;
	top: -27px;
}
.list-title-bg{
	width: 200px;
	height:40px;
}
.list-title{
	font-size: 20px;
	font-weight: 700;
	top: -35px;
	position: relative;
}
.list-title::after{
	content:'';
	display: inline-block;
	background-color: #FFFFFF;
	vertical-align: middle;
	margin-right: 7px;
	border-radius: 4px;
	width: 6px;
	height: 6px;
	margin-left: 4px;
}
.list-title::before{
	content:'';
	display: inline-block;
	width: 4px;
	height: 4px;
	background-color: #FFFFFF;
	vertical-align: middle;
	margin-right: 7px;
	border-radius: 4px;
}


/////////////////////////////////
.content-body-list{
	padding: 0;
	margin: -30px 15px 0;
}
ul li{
	list-style-type:none;
	margin:0;
	padding:0;
	display: flex;
	flex-direction: row;
	padding: 0 0 0 15px;
	background-color: #FF8903;
	margin-bottom: 20px;
	border-radius: 5px;
	shadow: 0px 5px 4px #FFC88A;
}
.body-content{
	color:#FFFFFF;
	flex:1;
	padding: 10px;
	font-weight: 600;
	    font-family: fangsong;
}
.content-img{
	width:25px;
	height: 30px;
	width: 25px;
	height: 26px;
	position: relative;
	top: 13px;
	
}
.content-img-file{
	width: 20px;
	height: 25px;
	padding: 0 3px;
	width: 25px;
	height: 26px;
	position: relative;
	top: 13px;
}
.body-content-status{
	display: flex;
	justify-content: center;
	align-items: center;
	width: 60px;
}
.content-status{
	height: 50px;
	width: 60px;
	position: relative;
	right: -10px;
}
</style>
