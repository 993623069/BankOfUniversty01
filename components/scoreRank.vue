<template>
	<view class="score-rank">
	    <view class="header">
			<ul class="header-container">
				<li v-for="(item,tabIndex) in tabList" 
				   :key="tabIndex" 
				   class="header-tab-item"
				   @click="changeTab(item)"
				   :class="{'tab-item-active':tabItemIndex===tabIndex}">
					<text class="item-name">{{item.text}}</text>
					<span class="tab-active-item"></span>
				</li>
			</ul>
		</view>
		<view class="body-content">
			<ul class="body-content-list">
				<li v-for="(item,tabIndex) in scoreList[tabItemIndex]" 
				    :key="tabIndex" 
					 class="content-list-item"
					:class="[levelBg[item.level-1]]">
					<view class="tab-item-left">
						<image :src="'/static/level0'+item.level+'.png'"
						        class="tab-item-img"
						        v-if="item.level < 4"></image>
						<text v-else>{{item.level}}</text>
					</view>
					
					<text class="item-name">{{item.name}}</text>
					<view class="tab-item-right">
						{{item.score}}
					</view>
				</li>
			</ul>
		</view>
	</view>
</template>

<script>
	export default {
		name:"scoreRank",
		data() {
			return {
				tabItemIndex:0,
                levelBg:['item-level-1','item-level-2','item-level-3'],
				scoreList:[
					[{level:1,name:'托尼斯达1',score:1000},
					{level:2,name:'托尼斯2',score:900},
					{level:3,name:'托尼斯2',score:800},
					{level:4,name:'托尼斯2',score:700},
					{level:5,name:'托尼斯2',score:600},
					{level:6,name:'托尼斯2',score:500},
					{level:7,name:'托尼斯2',score:400},
					{level:8,name:'托尼斯2',score:300},
					],
					[
					{level:1,name:'第一',score:1000},
					{level:2,name:'第二',score:900},
					{level:3,name:'第三',score:800},
					{level:4,name:'托尼斯2',score:700},
					{level:5,name:'托尼斯2',score:600},
					{level:6,name:'托尼斯2',score:500},
					{level:7,name:'托尼斯2',score:400},
					{level:8,name:'托尼斯2',score:300},
					],
					],
				tabList:[{
					index:0,
					key:'',
					text:'个人积分排行'
				},{
					index:1,
					key:'',
					text:'小组积分排行'
				}]
			};
		},
		methods:{
			changeTab(item,index){
				this.tabItemIndex=item.index
			}
		}
	}
</script>

<style>
.score-rank{
	border-top-left-radius: 15px;
	border-top-right-radius: 15px;
	margin-top: -15px;
	background-color: #fff;
	padding-top: 10px;
}
.header-container{
	display: flex;
	border-bottom: 1px solid #DBDBDB;
}

.header-tab-item{
	flex:1;
	text-align: center;
	padding: 10px;
	color:#969696;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
.tab-item-active > .item-name{
	color:#000000;
}
.tab-active-item{
	height:0;
}
.tab-item-active >.tab-active-item
{    height: 3px;
    background-color: #B6012A;
    width: 50px;
    position: relative;
    bottom: -9px;}
	///////////
	.body-content-list{
		margin-top: 5px;
		padding: 15px 20px;
		    font-size: 16px;
	}
	.content-list-item{
		display: flex;
		padding: 10px 16px;
		margin-bottom: 10px;
		align-items: center;
		background-color: #F2F2F2;
		border-radius: 20px;
	}
	.tab-item-left{
		width: 40px;
		display: flex;
		justify-content: center;
		align-items: center;
		
	}
	.tab-item-img{
		width: 30px;
		height: 35px;
	}
	.tab-item-right{
		width: 100px;
		overflow: hidden;
		text-overflow: ellipsis;
		text-align: center;
	}
	.item-name{
		padding: 0 10px;
		flex:1;
	}
	.item-level-1{
		  background-image: linear-gradient(to #EEB655, #EEB655 , #F3CD7E);
	}
	.item-level-2{
		  background-image: linear-gradient(to #94A3AA, #94A3AA , #C5D2DA);
	}
	.item-level-3{
		  background-image: linear-gradient(to #BC7243, #BC7243 , #F4BFA0);
	}
</style>
