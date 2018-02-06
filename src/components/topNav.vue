<template>
	<div id="topNav" v-bind:style="{width : width + 'px'}">
		<div class="logo">
			<img src="../assets/img/logo.png" class="logoImg" />
			<a href="" class="logoTitle">鬼少云音乐</a>
		</div>
		<div class="nav">
			<div class="back">
				<i class="iconfont icon-back"></i>
			</div>
			<div class="forward">
				<i class="iconfont icon-more"></i>
			</div>			
		</div>
		<div class="seach">
			<input type="text" value="搜索音乐，歌手，歌词，用户" onfocus="javascript:if(this.value=='搜索音乐，歌手，歌词，用户'){this.value='';}" onblur="javascript:if(!this.value){this.value='搜索音乐，歌手，歌词，用户';}"/>
			<i class="iconfont icon-search"></i>
		</div>
		
		<div class="windowTools">
			<i class="iconfont icon-MAXIMIZE"></i>
			<i class="iconfont icon-subtract"></i>
			<i class="iconfont icon-weigouxuan"></i>
			<i class="iconfont icon-close"></i>
		</div>
		<div class="appTools">
			<i class="iconfont icon-clothes"></i>
			<i class="iconfont icon-email"></i>
			<i class="iconfont icon-set"></i>
		</div>		
		<div class="user" id="user">
			<div class="head">
				<img src="../assets/img/user.png"/>
			</div>
			<div class="userNameBox">
				<span class="userName">未登录</span>
				<i class="iconfont icon-down"></i>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		name:'Home',
		data () {
			return {
				test:'Mr.king'
			}
		},
		props:['width']
	}
</script>
<style lang="less" scoped>
	
	@base:#d23023;
	@height:50px;
	
	#topNav{
		border-bottom:1px solid #ddd;
		background:@base;
		min-width:1024px;
		height:@height;
		transition: all 0.2s;
	}
	
	.logo{
		height:@height;
		line-height:@height;
		width:140px;
		float:left;
		text-align:center;		
		.logoImg{
			width:20px;
			height:20px;
			vertical-align:-4px;
		}
		.logoTitle{
			text-decoration: none;
			color:#fff;
			font-size:18px;
		}	
	}
	
	.nav{
		float:left;
		margin-left:52px;
		position:relative;
		width:65px;
		height:@height;
		div{
			border:1px solid #be140f;
			width:26px;
			line-height:20px;
			height:20px;
			float: left;
			position:absolute;
			top:50%;
			transform: translateY(-50%);
			color:#ec6d59;
			font-weight: bold;
		}
		.back{
			left:0;
			border-right:none;
			border-top-left-radius: 3px;
			border-bottom-left-radius: 3px;
		}
		.forward{
			left:26px;
			border-top-right-radius: 3px;
			border-bottom-right-radius: 3px;			
		}
	}
	
	.seach{
		float:left;
		height:@height;		
		position:relative;
		input{
			position:absolute;
			top:50%;
			transform: translateY(-50%);
			color:#ec6d59;	
			background:#b13023;
			border:none;
			border-radius: 11px;
			height:22px;
			width:198px;
			padding: 0 10px;
			outline: none;	
			line-height: 22px;
			color:#dfa094;
			font-size:12px;
			&:focus + .icon-search,&:focus{
				color:#fff;					
			}
		}
		.icon-search{
			position:absolute;
			top:50%;
			transform: translateY(-50%);			
			left:195px;
			font-size:14px;
			color:#dfa094;
		}
	}
	
	.user{
		float:right;
		height:@height;		
		font-size:13px;	
		color:#ecdcdc;
		.head{
			width:24px;
			height:24px;
			border-radius:12px;
			overflow: hidden;
			float: left;
			background:#ddd;
			margin:12px 5px;
			cursor:pointer; 
			img{
				width:100%;
				height:100%;
			}
		}
		.userNameBox{
			height:@height;	
			line-height: @height;
			cursor:pointer; 
			float: left;
			&:hover{
				color:#fff;
			}
			.iconfont{
				font-size:4px;
				margin-left:4px;
			}			
		}
	}
	
	.windowTools{
		float:right;
		height:@height;	
		line-height: @height;	
		font-size:13px;	
		color:#ccdcdc;	
		padding:0 12px;
		.iconfont{
			cursor:pointer; 
			margin:0 2px;
			&:hover{
				color:#fff;
			}
		}	
	}
	.appTools{
		float:right;	
		font-size:13px;	
		color:#ccdcdc;	
		padding:2px 12px 2px 6px;
		margin-top:15px;
		border-right:1px solid #b13023;
		.iconfont{
			cursor:pointer; 
			margin-left:18px;
			margin-right:5px;
			&:hover{
				color:#fff;
			}
		}		
	}
</style>