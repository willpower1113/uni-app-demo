<template>
	<scroll-view class="uni-scroll">
		<view class="uni-title uni-logo">
			<image src="../../../static/componentHL.png" class="uni-img-logo"></image>
		</view>
		
		<view class="uni-common-mt">
			<text class="uni-exemple">
				{{titles[0]}}
			</text>
			<view class="uni-container uni-container-row">
				<view class="uni-block-horizontal red">1</view>
				<view class="uni-block-horizontal blue">2</view>
				<view class="uni-block-horizontal green">3</view>
			</view>
		</view>
		
		<view class="uni-common-mt">
			<text class="uni-exemple">
				{{titles[1]}}
			</text>
			<view class="uni-container uni-container-row-reverse">
				<view class="uni-block-horizontal red">1</view>
				<view class="uni-block-horizontal blue">2</view>
				<view class="uni-block-horizontal green">3</view>
			</view>
		</view>
		
		<view class="uni-common-mt">
			<text class="uni-exemple">
				{{titles[2]}}
			</text>
			<view class="uni-container uni-container-column">
				<view class="uni-block-vertical red">1</view>
				<view class="uni-block-vertical blue">2</view>
				<view class="uni-block-vertical green">3</view>
			</view>
		</view>
		
		<view class="uni-common-mt">
			<text class="uni-exemple">
				{{titles[3]}}
			</text>
			<view class="uni-container uni-container-column-reverse">
				<view class="uni-block-vertical red">1</view>
				<view class="uni-block-vertical blue">2</view>
				<view class="uni-block-vertical green">3</view>
			</view>
		</view>
		<view class="uni-common-mt">
			<text class="uni-exemple">
				{{titles[4]}}
			</text>
			<view class="uni-container-check-box">
						<button type="primary"  class="uni-content-button" @tap="onSetContent" data-value="flex-start">flex-start</button>
						<button type="primary"   class="uni-content-button">flex-end</button>
						<button type="primary" class="uni-content-button">center </button>
						<button type="primary"   class="uni-content-button">space-between</button>
						<button type="primary"   class="uni-content-button">space-around</button>
			</view>
		</view>
		
		
	</scroll-view>
</template>

<script>
	export default {
		data() {
			return {
				titles:['flex-direction:row（从左到右,水平分布）'
				,'flex-direction:row-reverse（从右到左,水平分布）'
				,'flex-direction:cloum（从上到下,垂直分布）'
				,'flex-direction:cloum-reverse（从下到上,垂直分布）'
				,'justify-content 属性设置'],
				
			}
		},
		methods: {
			onSetContent(e){
				console.log(e.currentTarget.dataset.value)
				
			}
		}
	}
</script>

<style>
	.uni-logo{
		display: flex;
		justify-content: center;
	}
	
	.uni-exemple{
		margin-left: 15upx;
		font-weight: 600;
		font-size: 28upx;
	}
	
	.uni-img-logo{
		width: 100upx;
		height: 100upx;
		margin-top: 50upx;
		margin-bottom: 50upx;
	}
	
	.uni-container-row{
		display: flex;
		flex-direction: row;
		margin-top: 20upx;
	}
	
	.uni-container-row-reverse{
		display: flex;
		flex-direction: row-reverse;
		margin-top: 20upx;
	}
	
	.uni-container-column{
		display: flex;
		flex-direction: column;
		margin-top: 20upx;
	}
	
	.uni-container-column-reverse{
		display: flex;
		flex-direction: column-reverse;
		margin-top: 20upx;
	}
	
	.uni-block-horizontal{
		width: 30%;
		height: 100upx;
	}
	
	.uni-block-vertical{
		width: 80%;
		height: 100upx;
	}
	
	.red{
		background-color:#ea0000;
	}
	
	.green{
		background-color:#00ff00;
	}
	
	.blue{
		background-color:#0000ff;
	}
	
	.uni-container-check-box{
		display: flex;
		flex-direction: row;	
		flex-wrap: wrap;
		justify-content: space-around;
	}
	
	.uni-content-button{
		width: auto;
		height: 80upx;
		margin-top: 20upx;
	}
</style>
