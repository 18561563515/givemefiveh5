<template>
	<view class="content">

		<swiper class="swiper" :indicator-dots="false" :autoplay="false" :interval="200" :duration="300" :current="current"
		 :vertical="true" @change="swChange" :disable-touch="disableTouch">
			<swiper-item>
				<view class="swiper-item1 uni-bg-red">
					<!-- <view class="down"></view> -->

					

								<view class="logo">
									<image src="../../static/logo.png" mode="widthFix" class="logopic"></image>
								</view>
								<view class="title">

								</view>
								<view class="five" @click="handClick">

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

								<view class="down"></view>

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
											<text class="zi-left animated fadeInLeft yanchi2s" v-show="classa">14:05-14:25</text>
											<view class="yuan"></view>
											<text class="zi-right animated fadeInRight yanchi2s" v-show="classa">Iris及CLC致辞</text>
										</view>
										<view class="time-line">
											<text class="zi-left animated fadeInLeft yanchi3s" v-show="classa">14:25-14:50</text>
											<view class="yuan"></view>
											<text class="zi-right animated fadeInRight yanchi3s" v-show="classa">“爱的传递”公益拍卖</text>
										</view>
										<view class="time-line">
											<text class="zi-left animated fadeInLeft yanchi4s" v-show="classa">14:50-14:55</text>
											<view class="yuan"></view>
											<text class="zi-right animated fadeInRight yanchi4s" v-show="classa">庆生蛋糕</text>
										</view>
										<view class="time-line">
											<text class="zi-left animated fadeInLeft yanchi5s" v-show="classa">14:55-15:00</text>
											<view class="yuan"></view>
											<text class="zi-right animated fadeInRight yanchi5s" v-show="classa">合影</text>
										</view>
										<view class="time-line">
											<text class="zi-left animated fadeInLeft yanchi6s" v-show="classa">15:00-15:10</text>
											<view class="yuan"></view>
											<text class="zi-right animated fadeInRight yanchi6s" v-show="classa">茶歇及文化Lab实验室</text>
										</view>
										<view class="time-line">
											<text class="zi-left animated fadeInLeft yanchi7s" v-show="classa">15:10-16:00</text>
											<view class="yuan"></view>
											<text class="zi-right animated fadeInRight yanchi7s" v-show="classa">团队活动-油画拼图（上海办）</text>
										</view>
									</view>
								</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item2 uni-bg-blue">
								<view class="down"></view>
								<view class="baiban1">
									<text style="color: #920783;font-size: 42rpx;line-height: 56rpx;text-align: center;font-weight: bold;">乐高墙</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">这5年来，300多人的团队，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">1825天的风雨同行，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">成就今天的“与奥共伍，创领未来”！</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">这些关键字由我们点点滴滴的</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">成果汇聚而成。</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">邀请参与现场版<text style="color: #920783;">乐高墙有奖问答</text>，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">找出藏在乐高墙积木下的小惊喜，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">揭开它的神秘面纱，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classd">答题赢得精美礼品。</text>
									<view class="pic-box animated fadeInUp yanchi05s" v-show="classd">
										<image src="../../static/picd.png" mode="widthFix" class="pictu animated bounceIn yanchi1s pictud " v-show="classd"></image>
									</view>
								</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item2 uni-bg-blue">

								<view class="down"></view>

								<view class="baiban1">
									<text style="color: #920783;font-size: 42rpx;line-height: 56rpx;text-align: center;font-weight: bold;">公益拍卖</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">作为一家具有社会责任的企业，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">参与公益一直是我们的优良传统，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">在庆祝奥森多5周年之际，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">我们以感恩之心回馈社会。</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">诚邀加入<text style="color: #920783;"> “爱的传递”公益拍卖</text>，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">为“宝贝之家”的重病孤儿提供医疗援助，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classb">缔造生命的希望！</text>
									<view class="pic-box animated fadeInUp yanchi05s" v-show="classb">
										<image src="../../static/pic1.png" mode="widthFix" class="pictu animated rotateIn yanchi1s pictu1 " v-show="classb"></image>
										<image src="../../static/pic2.png" mode="widthFix" class=" pictu animated rotateIn  yanchi2s pictu2" v-show="classb"></image>
										<image src="../../static/pic3.png" mode="widthFix" class=" pictu animated rotateIn  yanchi3s pictu3" v-show="classb"></image>
										<image src="../../static/pic4.png" mode="widthFix" class=" pictu animated rotateIn  yanchi4s pictu4" v-show="classb"></image>
									</view>
								</view>
							</view>
						</swiper-item>
						<swiper-item>
							<view class="swiper-item2 uni-bg-blue">
								<view class="down"></view>
								<view class="baiban1">
									<text style="color: #920783;font-size: 42rpx;line-height: 56rpx;text-align: center;font-weight: bold;">文化Lab实验室</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">奥森多成立5年来，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">我们致力于打造行业内最专业、</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">最优秀的团队。</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">邀请参与现场版<text style="color: #920783;">文化Lab实验室</text>，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">通过游戏体验，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">获得文化DNA认证，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classe">完成文化的自我进化。</text>
									<view class="pic-box animated fadeInUp yanchi05s" v-show="classe">
										<image src="../../static/pice1.png" mode="widthFix" class="pictu animated flipInY yanchi1s pictue1 " v-show="classe"></image>
										<image src="../../static/pice2.png" mode="widthFix" class="pictu animated flipInX yanchi2s pictue2 " v-show="classe"></image>
									</view>
								</view>
							</view>
						</swiper-item>
						
						<swiper-item>
							<view class="swiper-item2 uni-bg-blue">
								<view class="down"></view>
								<view class="baiban1">
									<text style="color: #920783;font-size: 42rpx;line-height: 56rpx;text-align: center;font-weight: bold;">油画拼图</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classf">   5年来取得的成就，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classf">离不开具有高效执行力的团队，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classf">更离不开每一位的辛勤付出。</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classf">邀请参与现场版<text style="color: #920783;">“油画拼图”</text>活动，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classf">用手中的画笔为奥森多五周年庆典画面添彩，</text>
									<text class="ziyanse animated fadeInUp yanchi05s" v-show="classf">留下最美好的纪念。</text>
									<view class="pic-box animated fadeInUp yanchi05s" v-show="classf">
										<image src="../../static/picf1.png" mode="widthFix" class="pictu animated rotateIn yanchi1s pictuf1 " v-show="classf"></image>
										<image src="../../static/picf2.png" mode="widthFix" class="pictu animated rotateIn yanchi2s pictuf2 " v-show="classf"></image>
									</view>
								</view>
							</view>
						</swiper-item>
						
						
						<swiper-item>

							<view class="swiper-item uni-bg-blue">
								<view class="logo-box">
									<image src="../../static/xiaologo.png" mode="widthFix" class="dalogo"></image>
									<image src="../../static/logo.png" mode="widthFix" class="xiaologo"></image>
								</view>
								<view class="biaoti2">
									<text>诚邀您参加Ortho中国</text>
									<text>5周年庆典</text>
								</view>
								<image src="../../static/xiao5.png" mode="widthFix" class="xiao5"></image>
								<view class="biaoti3">
									<text class="daxiao1" v-show="classc">时间：2020.10.26 13:45</text>
									<text class="daxiao2" v-show="classc">地点：上海办公室</text>
								</view>
								<view class="erweima-box">
									<view class="erweima">
										<image src="../../static/erweima1.png" mode="widthFix" class="erweima1"></image>
										<text>参与有奖问答</text>
										<text>好礼等你拿</text>
									</view>
									<view class="erweima">
										<image src="../../static/erweima2.png" mode="widthFix" class="erweima2"></image>
										<text>网络同步直播</text>
										<text>敬请期待</text>
									</view>
								</view>
							</view>


						</swiper-item>
					</swiper>
				</view>
				
</template>

<script>
	let bgm = new Audio()
	bgm.src = 'http://3w.donglianguoji.com/app/givemefive/music4.mp3'
	bgm.loop = true
	export default {
		data() {
			return {
				title: 'Hello',
				classa: false,
				classb: false,
				disableTouch:true,
				classc: false,
				classd: false,
				classe: false,
				classf: false,

				current: 0
			}
		},
		onLoad() {

			
			

		},
		methods: {
			swChange(e) {
if (e.detail.current == 0  ) {
					this.disableTouch = true
					// bgm.stop()
				}
				if (e.detail.current != 1) {
					this.classa = false
				} else {
					this.classa = true
				}

			if (e.detail.current != 2) {
								this.classd = false
							} else {
								this.classd = true
							}
							
				if (e.detail.current != 3) {
					this.classb = false
				} else {
					this.classb = true
				}
if (e.detail.current != 4) {
					this.classe = false
				} else {
					this.classe = true
				}
				if (e.detail.current != 5) {
									this.classf = false
								} else {
									this.classf = true
								}

				if (e.detail.current != 6) {
					this.classc = false
				} else {
					this.classc = true
				}


				this.current = e.detail.current
			},
			
			
			handClick(){
				
				bgm.play()
				this.current = 1
				// this.classa = true
				this.disableTouch = false
			}
			
			
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

		position: relative;

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

		position: relative;

	}

	.baiban {
		padding: 45rpx 20rpx;
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
		margin: 0 30rpx;
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
.yanchi05s {
		animation-delay: 0.5s;
	}
	.yanchi1s {
		animation-delay: 1s;
	}

	.yanchi2s {
		animation-delay: 2s;
	}

	.yanchi3s {
		animation-delay: 3s;
	}

	.yanchi4s {
		animation-delay: 4s;
	}

	.yanchi5s {
		animation-delay: 5s;
	}

	.yanchi6s {
		animation-delay: 6s;
	}

	.yanchi7s {
		animation-delay: 7s;
	}

	.yanchi8s {
		animation-delay: 7s;
	}

	.ziyanse {
		font-size: 32rpx;
		line-height: 70rpx;
		color: #535353;
		text-align: center;
	}

	.pic-box {
		display: flex;
		flex-direction: row;
		justify-content: center;
		flex-wrap: wrap;
		margin-top: 30rpx;
	}

	.pictu1 {
		width: 276rpx;
		height: 270rpx !important;
		display: block;
	}

	.pictu2 {
		width: 263rpx;
		height: 270rpx !important;		
		display: block;
	}

	.pictu3 {
		width: 274rpx;
		height: 280rpx !important;		
		display: block;
	}

	.pictu4 {
		width: 262rpx;
		height: 280rpx !important;		
		display: block;
	}
.pictud {
		width: 536rpx;
		height: 487rpx !important;		
		display: block;
	}
	.pictue1 {
			width: 436rpx;
			height: 279rpx !important;		
			display: block;
		}
		.pictue2 {
				width: 436rpx;
				height: 295rpx !important;		
				display: block;
			}
			.pictuf1 {
					width: 515rpx;
					height: 288rpx !important;		
					display: block;
				}
				.pictuf2 {
						width: 515rpx;
						height: 342rpx !important;		
						display: block;
					}
	.pictu {
		margin: 10rpx;
	}




	.logo-box {
		width: 100%;
		height: 81rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		margin-top: 30rpx;
	}


	.xiaologo {
		width: 166rpx;
		height: 61rpx;
		display: block;
		margin-right: 45rpx;

	}

	.dalogo {
		width: 185rpx;
		height: 81rpx;
		display: block;
		margin-left: 60rpx;
	}

	.biaoti2 {
		font-size: 48rpx;
		color: #fff;
		font-weight: bold;
		line-height: 74rpx;
		text-align: center;
		display: flex;
		flex-direction: column;
		margin-top: 109rpx;
		letter-spacing: 2px;
	}

	.xiao5 {
		width: 162rpx;
		height: 322rpx;
		display: block;
		margin: 0 auto;
		margin-top: 49rpx;
	}

	.biaoti3 {
		font-size: 40rpx;
		color: #fff;
		font-weight: bold;
		line-height: 70rpx;
		text-align: center;
		display: flex;
		flex-direction: column;
		margin-top: 50rpx;
		letter-spacing: 2px;
	}

	.erweima-box {
		display: flex;
		flex-direction: row;
		justify-content: center;
		font-size: 27rpx;
		color: #fff;
		line-height: 38rpx;
		text-align: center;
		margin-top: 50rpx;
	}

	.erweima {
		display: flex;
		flex-direction: column;
		margin: 0 34rpx;
	}

	.erweima1,
	.erweima2 {
		width: 244rpx;
		height: 244rpx;
	}

	.daxiao1 {
		animation: daxiao1 0.8s infinite ease-in;
	}

	.daxiao2 {
		animation: daxiao2 0.8s infinite ease-in;
	}

	@keyframes daxiao1 {
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

	@keyframes daxiao2 {
		0% {
			transform: scale(0.9);
		}

		50% {
			transform: scale(1);
		}

		100% {
			transform: scale(0.9);
		}
	}

	.down {
		width: 48rpx;
		height: 48rpx;
		background: url(../../static/down.png) no-repeat center center;
		background-size: 100% 100%;
		position: absolute;
		bottom: 20rpx;
		left: 50%;
		margin-left: -24rpx;
		animation: shangxia .8s ease infinite;
		z-index: 20;
	}

	@keyframes shangxia {
		0% {
			bottom: 20rpx;
		}

		50% {
			bottom: 30rpx;
		}

		100% {
			bottom: 20rpx;
		}
	}
</style>
