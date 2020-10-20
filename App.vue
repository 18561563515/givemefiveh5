<script>

	/* 获取URL，为了给php接口传参 */
		var url = location.href;
		/* 如果二次分享URL带参数，需要过滤后，方能正常分享 */
		var oldurl = 'http://3w.donglianguoji.com/app/givemefiveh5'; //这是要分享的地址，和下面的微信配置分享地址应该保持一致
		if (location.href.indexOf('from') !== -1) {
			history.pushState(null, null, oldurl);
			location.reload();
		}
	export default {
		onLaunch: function() {
			var jweixin = require('jweixin-module') //引入jssdk
						uni.request({
							url:'http://3w.donglianguoji.com/api/weixin/weixin.php?url='+url,
							success: (e) => {
								console.log(e.data)
								let bgm = new Audio()
								bgm.src = 'http://3w.donglianguoji.com/app/givemefive/bgm.mp3'
								bgm.loop = true
								bgm.play()
								jweixin.config({
								  debug: false,
								  appId: e.data.appId,
								  timestamp: e.data.timestamp,
								  nonceStr: e.data.nonceStr,
								  signature: e.data.signature,
								  jsApiList: ['onMenuShareTimeline', 'onMenuShareAppMessage', 'onMenuShareQQ', 'onMenuShareWeibo', 'onMenuShareQZone',
												
								  ]
								
								});
								
								
								jweixin.ready(function(){  
							 
							 var shareData = {
							     title: '与奥共舞 创领未来',
							     desc: '奥森多5周年庆典',
							     link: 'http://3w.donglianguoji.com/app/givemefiveh5', //分享地址
							     imgUrl: 'http://3w.donglianguoji.com/app/givemefiveh5/logo1.jpg', //分享logo
							     success: function(res) {
							         //分享成功
							         alert('您已分享成功')
							     },
							     cancel: function(res) {
							           alert('已取消分享');
							     }
							 };
							 jweixin.onMenuShareAppMessage(shareData);
							 jweixin.onMenuShareTimeline(shareData);
							 jweixin.onMenuShareQQ(shareData);
							 jweixin.onMenuShareWeibo(shareData);
							 jweixin.onMenuShareQZone(shareData);
							 
								/* jweixin.hideOptionMenu(); 
								jweixin.showMenuItems({
									menuList:[
										'menuItem:share:appMessage',
										'menuItem:share:timeline'
									]
								}); */
						});
								
								
								
							}
						})

},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
</style>
