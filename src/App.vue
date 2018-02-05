<template>
  <div id="app">
  	<div id="container" :style="{width:appStyle.width+'px',height:appStyle.height+'px'}">
	   	<topNav :width="appStyle.width"></topNav>
	    <router-view/> 	  		
  	</div>	
  </div>
</template>

<script>
	import topNav from '@/components/topNav';
	import leftNav from '@/components/leftNav';
	
	export default {
	  name: 'app',
	  components: {
		  topNav,
		  leftNav
		},
		data () {
			return {
				appStyle:{
					width:1024,
					height:670
				}
			}
		},
		methods:{
			
		}
	}
</script>
<style lang="less">
	
	.box-shadow(@style, @c) when (iscolor(@c)) {
	  -webkit-box-shadow: @style @c;
	  box-shadow:         @style @c;
	}
	.box-shadow(@style, @alpha: 50%) when (isnumber(@alpha)) {
	  .box-shadow(@style, rgba(0, 0, 0, @alpha));
	}
	

	body{
		padding: 0;
		margin: 0;
	}

	#app {
	  font-family: 'Avenir', Helvetica, Arial, sans-serif;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
	  text-align: center;
	  color: #2c3e50;
	  margin: 60px auto;
	}	
	
	#container{
	  border:1px solid #ddd;	
	  margin: 0 auto;
	  .box-shadow(0 4px 8px 0,20%)
	}	
</style>