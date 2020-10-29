<template>
	<view>
		<button @click="login">Login</button>
		<button open-type="getPhoneNumber" @getphonenumber="getPhoneNumber">getPhoneNumber</button>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			login(e) {  
				uni.login({  
					success: (res) => {  
						console.log("login", JSON.stringify(res));  
					}  
				})  
			},  
			getPhoneNumber(e) {  
				console.log(e.detail.errMsg);  
				console.log(e.detail.iv);  
				console.log(e.detail.encryptedData);  
			}

		}
	}
</script>

<style>

</style>
