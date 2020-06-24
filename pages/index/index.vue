<template>
	<view class="uni-container">
		<image src="../../static/componentIndex.png" class="uni-header-image"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
			console.log('onLoad()');
		},
		methods: {

		} 
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
	.uni-header-image{
		width: 50upx;
		height: 50upx;
		
	}
</style>
