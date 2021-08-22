<template>
	<view class="my-team">
		<view class="header">{{teamObj.name}}</view>
		<view class="team-list">
			<view class="team-list-group-leader">
			   <view class="leader-name">{{teamObj.leader.name}}</view>
			   <view class="leader-name-star">
				   <image src="../static/leader-flag.png" class="leader-name-star-img"></image>
				   <text class="leader-name-key">组长</text>
				 </view>
			</view>
			<view class="team-list-group">
			   <view class="group-name-star">
				   <image src="../static/member-flag.png" class="group-name-star-img"></image>
				   <text class="group-name-key">成员</text>
				 </view>
				 <view class="group-list">
					 <view class="list-content-item"
					    v-for="(item,gruoupIndex) in teamObj.groupList"
						:key="gruoupIndex">
					   <text>{{item.name}}</text>	 
					 </view>
				 </view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"myTeam",
		data() {
			return {
				teamObj:{
					name:'虎狼之师：',
					leader:{name:'小小组长',code:13242,id:898},
					groupList:[
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
						{name:'成员1',id:110},
					]
				}
			};
		}
	}
</script>

<style>
.header{
	color: #ffffff;
	    font-size: 20px;
	    text-align: center;
	    margin-top: 10px;
}
.team-list{
	margin: 10px 15px;
}
.team-list-group-leader{
	    background-color: #ffffff;
	    padding: 15px;
	    border-radius: 5px;
		margin-bottom: 15px;
}
.team-list-group{
	    background-color: #ffffff;
	    padding: 15px;
	    border-radius: 5px;
		margin-bottom: 15px;
}
.leader-name{
	text-align: center;
	font-size: 16px;
	position: relative;
	top: 6px;
}
.leader-name-star{
	width: 60px;
	height: 100%;
	margin-top: -20px;
	display: flex;
	justify-content: center;
	align-items: center;
	color:#FF8903;
	padding: 5px 10px;
	border-radius: 20px;
}
.group-name-star{
	color:#920525;
	    width: 60px;
	    padding: 5px 10px;
	    background-color: #E9CDD3;
	    text-align: center;
	    border-radius: 20px;
}
.leader-name-star{
	width: 60px;
	padding: 5px 10px;
	background-color: #FFE7CC;
	text-align: center;
	border-radius: 20px;
}
.leader-name-star-img,.group-name-star-img{
	width:20px;
	height:20px;
}
.leader-name-key,.group-name-key{
	margin-left: 2px;
}
.group-name-key{
	position: relative;
	top: -4px;
}
.list-content-item{
	padding: 10px;
	text-align: center;
	border-bottom: 1px solid #DADADA;
}
</style>
