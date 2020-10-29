<template>
	<view class="list-item" @click="$emit('click')" >
	   <image :src=item.image style="width: 365rpx; height: 365rpx;" class="rounded" mode="aspectFill">
	   </image>
	   
	   <view class="rounded-circle px-2 flex  align-center" style="position: absolute;left: 15rpx;top: 15rpx;
	   background-color: rgba(0,0,0,0.4);">
		   <text  class="iconfont iconbizhongguanli  text-warning  mr-1"></text><text class="text-white font">{{item.money}}</text>
	   </view>
	   
	   <view class="rounded-circle  px-2  flex  align-center" style="position: absolute;right:15rpx;top: 15rpx; background-color: rgba(0,0,0,0.4);">
		   <text class="font-sm text-white">人气：</text><text class="text-white  font-sm">{{item.hot}}</text>
	   </view>
	   
	   <view class="rounded-circle flex align-center " style=" position: absolute;left: 15rpx; bottom: 15rpx;">
		   <text  class=" text-white font">{{item.title}}</text>
	   </view>
	   
	   <view v-if="item.status === '已结束'" class="rounded-circle px-2 flex align-center" style="position: absolute;right: 15rpx; bottom: 15rpx; background-color: rgba(0,0,0,0.4);">
	       <text style="width: 20rpx; height: 20rpx;" class="rounded-circle bg-danger mr-1"></text><text class="text-white font-sm">{{ item.status }}</text>
	   </view>
	  <view v-else class="rounded-circle px-2 flex align-center" style="position: absolute;right: 15rpx; bottom: 15rpx; background-color: rgba(0,0,0,0.4);">
		   <text style="width: 20rpx; height: 20rpx;" class="rounded-circle bg-danger-1 mr-1"></text><text class="text-white font-sm">{{ item.status }}</text>
	  </view>

	</view>
</template>

<script>
	export default{
		props:{
			item:Object,
			index:[Number,String]
			
		},
		computed:{
			
		}
		
	}
</script>

<style>
</style>
