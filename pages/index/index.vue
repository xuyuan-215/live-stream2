<template>
  <view>
   <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="200"
   style="width: 750rpx;  height: 250rpx;">
	   <swiper-item>
		   <image src="../../static/banner1.jpg" style="width: 750rpx; height: 250rpx;"></image>
	   </swiper-item>
	   <swiper-item>
		   <image src="../../static/banner2.jpg"  style="width: 750rpx; height: 250rpx;" ></image>
	   </swiper-item>
   </swiper>
   
   <view class="flex flex-wrap">
	   <i-list v-for="(item,index) in list"
	   		   :key="index"
	   		   :item="item"
	   		   :index="index"
	   		   @click="openLive"
	   		   >
	   </i-list>
   </view>
   
	   
	</view>
</template>

<script>
	import iList from "@/components/common/i-list.vue"
	export default{
		components:{
			iList
		},
		data(){
			return{
				list:[
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'已结束'
					},
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'已结束'
					},
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'已结束'
					},
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'已结束'
					},
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'进行中'
					},
					{
						image:'../../static/me.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'已结束'
					},
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:18,
						title:'测试一下',
						status:'进行中'
					},
					{
						image:'../../static/me1.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'已结束'
					},
					{
						image:'../../static/me.jpg',
						money:25,
						hot:16,
						title:'测试一下',
						status:'进行中'
					},
					{
						image:'../../static/me.jpg',
						money:25,
						hot:15,
						title:'测试一下',
						status:'进行中'
					},
				]
			}
		},
		onLoad(){
			
		},
		methods:{
			openLive(){
				uni.navigateTo({
					url:'../live/live'
				});
				
			}
		}
		
	}
</script>

<style>
  .list-item{
	  width: 375rpx;
	  height: 375rpx;
	  padding: 5rpx;
	  box-sizing: border-box;
	  position: relative;
  }
  
  
  
</style>