<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
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
	@import url("//at.alicdn.com/t/font_1238779_co2ic3p9di5.css");
	/*状态栏设置 */
	.status_bar{
		height: var(--status-bar-height);
	}
</style>
