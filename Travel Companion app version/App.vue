<script>
	export default {
		onLaunch: function() {
		            console.log('App Launch');
					plus.screen.lockOrientation( 'portrait-secondary');//180度竖排锁定
					plus.screen.lockOrientation('portrait-primary') //竖屏锁定
		        },
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>
// App.vue或其他根页面
<script>
export default {
	
}
</script>
<style>
	
	@import url("./download/font_4102663_cretifjzbvp/iconfont.css");
	
</style>
 
<style lang="scss">
page {
  width: 100%;
  height: 100%;
}
</style>

