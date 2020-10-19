<template>
	<view class="content">
		<swiper class="swiper" :indicator-dots="true" :autoplay="false" :interval="200" :duration="300" :current="current" :vertical="true" @change="swChange">
			<swiper-item>
				<view class="swiper-item1 uni-bg-red">
					<view class="logo">
						<image src="../../static/logo.png" mode="widthFix" class="logopic"></image>
					</view>
					<view class="title">

					</view>
					<view class="five">

					</view>
					<view class="zi">

					</view>
					<view class="shou">
						<image src="../../static/shou.png" mode="widthFix" class="picshou"></image>
					</view>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item2 uni-bg-green">
					<view class="logo">
						<image src="../../static/logo.png" mode="widthFix" class="logopic"></image>
					</view>
					<view class="baiban">
						<text class="huodongricheng">活动日程</text>
						<view class="time-line-box">
							<view class="time-line">
								<text class="zi-left animated fadeInLeft" v-show="classa">13:45-14:00</text>
								<view class="yuan">
									<view class="yuan-line">

									</view>
								</view>
								<text class="zi-right animated fadeInRight" v-show="classa">签到或进入直播平台</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi1s" v-show="classa">14:00-14:05</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi1s" v-show="classa">开场视频</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi2s" v-show="classa">14:05-14:20</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi2s" v-show="classa">Iris及CLC致辞</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi3s" v-show="classa">14:20-14:40</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi3s" v-show="classa">“爱的传递”公益拍卖</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi4s" v-show="classa">14:40-14:50</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi4s" v-show="classa">庆生蛋糕</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi5s" v-show="classa">14:50-15:00</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi5s" v-show="classa">合影</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi6s" v-show="classa">15:00-15:10</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi6s" v-show="classa">茶歇</text>
							</view>
							<view class="time-line">
								<text class="zi-left animated fadeInLeft yanchi7s" v-show="classa">15:10-16:00</text>
								<view class="yuan"></view>
								<text class="zi-right animated fadeInRight yanchi7s" v-show="classa">团队活动</text>
							</view>
						</view>
					</view>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item2 uni-bg-blue">
					<view class="baiban1">
						<text class="ziyanse animated fadeInUp" v-show="classb">作为一家具有社会责任的企业，</text>
						<text class="ziyanse animated fadeInUp yanchi1s" v-show="classb">参与公益一直是我们的优良传统，</text>
						<text class="ziyanse animated fadeInUp yanchi2s" v-show="classb">在庆祝奥森多5周年之际，</text>
						<text class="ziyanse animated fadeInUp yanchi3s" v-show="classb">我们以感恩之心回馈社会。</text>
						<text class="ziyanse animated fadeInUp yanchi4s" v-show="classb">诚邀加入<text style="color: #920783;"> “爱的传递”公益拍卖</text>，</text>
						<text class="ziyanse animated fadeInUp yanchi5s" v-show="classb">为“宝贝之家”的重病孤儿提供医疗援助，</text>
						<text class="ziyanse animated fadeInUp yanchi6s" v-show="classb">缔造生命的希望！</text>
						<view class="pic-box animated fadeInUp yanchi7s" v-show="classb">
							<image src="../../static/pic1.png" mode="widthFix" class="pictu1 pictu"></image>
							<image src="../../static/pic2.png" mode="widthFix" class="pictu2 pictu"></image>
							<image src="../../static/pic3.png" mode="widthFix" class="pictu3 pictu"></image>
							<image src="../../static/pic4.png" mode="widthFix" class="pictu4 pictu"></image>
						</view>
					</view>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item uni-bg-blue">C</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				classa: false,
				classb: false,
				current:0
			}
		},
		onLoad() {

		},
		methods: {
			swChange(e) {
				
				if (e.detail.current != 1) {
					this.classa = false
				} else {
					this.classa = true
				}
				
				if (e.detail.current != 2) {
					this.classb = false
				} else {
					this.classb = true
				}
				
				
				
				this.current = e.detail.current
			},
		}
	}
</script>

<style>
	@import url("../../static/animate.css");

	page {
		background: url(../../static/bg.png) no-repeat center top;
		background-size: 100% 100%;
	}

	.content {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
	}

	.swiper {
		width: 100%;
		height: 100%;
	}

	.swiper-item1 {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
		height: 100%;
	}

	.logo {
		height: 61rpx;
		width: 100%;
		margin-top: 46rpx;
	}

	.logopic {
		width: 166rpx;
		height: 61rpx;
		display: block;
		float: right;
		margin-right: 45rpx;
	}

	.title {
		width: 522rpx;
		height: 233rpx;
		background: url(../../static/title.png) no-repeat center center;
		background-size: cover;
	}

	.five {
		width: 213rpx;
		height: 425rpx;
		background: url(../../static/five.png) no-repeat center center;
		background-size: cover;
		animation: daxiao 0.8s infinite ease-in;
	}

	.zi {
		width: 503rpx;
		height: 65rpx;
		background: url(../../static/timu.png) no-repeat center center;
		background-size: cover;
	}

	.shou {
		width: 100%;
		/* height: 65rpx;
		background: url(../../static/timu.png) no-repeat center center;
		background-size: cover; */
	}

	.picshou {
		width: 100%;
		height: auto;
		display: block;
	}

	@keyframes daxiao {
		0% {
			transform: scale(1);
		}

		50% {
			transform: scale(0.9);
		}

		100% {
			transform: scale(1);
		}
	}



	.swiper-item2 {
		display: flex;
		flex-direction: column;
		align-items: center;
		height: 100%;
	}

	.baiban {
		padding: 45rpx 50rpx;
		background: rgba(255, 255, 255, .5);
		border-radius: 20rpx;
		margin-top: 45rpx;
		display: flex;
		flex-direction: column;
	}
.baiban1 {
	width: 666rpx;
		padding: 45rpx 0rpx;
		background: rgba(255, 255, 255, .5);
		border-radius: 20rpx;
		margin-top: 45rpx;
		display: flex;
		flex-direction: column;
		overflow: hidden;
	}
	.huodongricheng {
		color: #920783;
		font-weight: bold;
		font-size: 56rpx;
		text-align: center;
	}

	.time-line-box {
		margin-top: 47rpx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		height: 818rpx;
		overflow: hidden;
	}

	.time-line {
		display: flex;
		flex-direction: row;
		align-items: center;
	}

	.zi-left {
		color: #920783;
		font-size: 28rpx;
		font-weight: bold;
	}

	.zi-right {
		color: #2a2a2a;
		font-size: 28rpx;
	}

	.yuan {
		width: 28rpx;
		height: 28rpx;
		background: #fff;
		border-radius: 50%;
		margin: 0 40rpx;
		position: relative;
	}

	.yuan-line {
		position: absolute;
		width: 1px;
		height: 848rpx;
		border-right: 2px solid #fff;
		left: 50%;
		top: -20rpx;
		transform: translateX(-50%);
	}
	.yanchi1s{
		animation-delay: 1s;
	}
	.yanchi2s{
		animation-delay: 2s;
	}
	.yanchi3s{
		animation-delay: 3s;
	}
	.yanchi4s{
		animation-delay: 4s;
	}
	.yanchi5s{
		animation-delay: 5s;
	}
	.yanchi6s{
		animation-delay: 6s;
	}
	.yanchi7s{
		animation-delay: 7s;
	}
	.yanchi8s{
		animation-delay: 7s;
	}
	
	.ziyanse{
		font-size: 32rpx;
		line-height: 70rpx;
		color: #535353;
		text-align: center;
	}
	
	.pic-box{
		display: flex;
		flex-direction: row;
		justify-content: center;
		flex-wrap: wrap;
		margin-top: 30rpx;
	}
	.pictu1{
		width: 276rpx;
		height: 270rpx;
	}
	.pictu2{
		width: 263rpx;
		height: 270rpx;
	}
	.pictu3{
		width: 274rpx;
		height: 280rpx;
	}
	.pictu4{
		width: 262rpx;
		height: 280rpx;
	}
	.pictu{
		margin: 10rpx;
	}
</style>
