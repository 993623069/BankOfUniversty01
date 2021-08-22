<template>
	<view class="certify-infor">
		<view class="infor-title-container">
			<view class="infor-title">社团证书</view>
		</view>
		
		<view class="infor-content">
			<view class="infor-content-list">
				<view class="infor-item">
					<span class="infor-item-key">证书名称：</span>{{infor.bookName}}
				</view>
				<view class="infor-item">
					<span class="infor-item-key">证书编号：</span>{{infor.code}}
				</view>
				<view class="infor-item">
					<span class="infor-item-key">持证人：</span>{{infor.name}}
				</view>
				<view class="infor-item">
					<span class="infor-item-key">获取时间：</span>{{infor.haveTime}}
				</view>
			</view>
			<image src="../static/infor-star.png" class="infor-star"></image>
		</view>
	</view>
</template>

<script>
	export default {
		name:"certifyInfor",
		data() {
			return {
				infor:{
					bookName:'证书老字号',
					code:'0zzzzzzzzz',
					name:'王晓欸',
					haveTime:'2020-02-02'
				}
			};
		}
	}
</script>

<style>
.certify-infor{
	margin: 30px 10px 15px;
	border-radius: 5px;
	background-color: #FFFFFF;
	padding: 15px 10px 10px 10px;
}
.infor-title-container{
	position: relative;
	    display: flex;
	    justify-content: center;
	    top: -33px;
}
.infor-title{
	width: 120px;
	    background-color: #FF8903;
	    text-align: center;
	    padding: 5px 10px;
	    border-radius: 10px;
	    border: 2px solid #fff;
	    color: #fff;
	    font-weight: 600;
		 box-shadow: 0px 7px 7px -7px #ff8903;
}
.infor-content{
	display: flex;
	border: 1px solid #BEBEBE;
	padding: 10px;
}
.infor-content-list{
	flex:1;
}
.infor-star{
	width:60px;
	height: 70px;
}
.infor-item{
	padding: 10px 10px;
	display: flex;
	color:#000000;
	
}
.infor-item-key{
	display: inline-block;
	width: 88px;
	text-align: right;
	color:#828282;
}
</style>
