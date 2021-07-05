<template>
	<view class="page_edu">
		<view class="page_edu_header">
			<view class="header">
				<image src="/static/icon_main.png" class="btn"></image>
				<view class="input">
					<image src="/static/search.png" class="search"></image>
					<input type="text" value="" placeholder="搜索功能" />
				</view>
				<image src="/static/msg.png" class="btn"></image>
			</view>
			<view class="header_content">
				<view class="left">
					<text class="title"><u-icon label="" size="30" name="https://cdn.uviewui.com/uview/example/button.png">
					
				</u-icon>
			开启智慧洗涤之旅</text>
					<text class="sub_title">省水、省电、省时</text>
					<text class="btn">Intelligent wash</text>
				</view>
				<view>
					<image src="/static/wa7.png" style="width: 260px;height: 165px;"></image>
				</view>
			</view>
		</view>
		<view class="page_content">
			
		
			<view class="ad">
			
				<view class="ad_btn">
					
					<text class="title">享受智慧家居，提高生活品质</text>
					<text class="sub_title">您的洗涤好帮手</text>
				</view>
				<image src="/static/tag.png" class="bg"></image>
			</view>
		</view>
		<scroll-view scroll-x="true" class="slider">
			<template v-for="(it, i) in records">
				<view class="item" :key="'slider_item_'+i" :style="{background: it.bg, marginRight: i === records.length - 1 ? '15px' : '0px'}">
					<view class="item_content">
				
						<image class="image" :src="it.icon"></image>
						<text class="free"> Wash</text>
					</view>
				</view>
			</template>
		</scroll-view>
		<u-button  type="success" :ripple="true" ripple-bg-color="#909399">
		<u-icon name="checkbox-mark" color="#2979ff" size="28"></u-icon>	已经放入餐具，即时开始洗涤
		</u-button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			
				records: [{
						bg: 'linear-gradient(-30deg,rgba(171,218,255,1),rgba(215,239,255,1))',
						
						subColor: '#15639F',
						icon: '/static/wa4.png',
						isFree: true
					},
					{
						bg: 'linear-gradient(-30deg,rgba(192,253,227,1),rgba(224,252,240,1))',
					
						subColor: '#07B77B',
						icon: '/static/wa2.png',
						isFree: false
					},
					{
						bg: 'linear-gradient(-30deg,rgba(171,218,255,1),rgba(215,239,255,1))',
						// title: '教师考情分析',
						// mainTeacher: '小A',
						// subTitle: '标题名称',
						subColor: '#15639F',
						icon: '/static/wa3.png',
						isFree: true
					}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	
	page {
		width: 100%;
		background-color: #ebebeb;
	}
</style>
<style lang="scss" scoped>
		// @import "uview-ui/index.scss";
	@function realSize($args) {
		@return $args / 1.5;
	}

	.page_edu {
		width: 100%;
	}

	.page_edu_header {
		padding-top: var(--status-bar-height);
		background-color: #0bc99d;
		width: 100%;
		height: realSize(415px);

		.header {
			display: flex;
			flex-direction: row;
			align-items: center;
			padding: realSize(20px);

			.btn {
				width: realSize(36px);
				height: realSize(30px);
			}

			.input {
				height: realSize(59px);
				width: 100%;
				margin-left: realSize(20px);
				margin-right: realSize(20px);
				background: rgba(255, 255, 255, 1);
				border-radius: realSize(30px);
				display: flex;
				flex-direction: row;
				align-items: center;

				.search {
					width: realSize(30px);
					height: realSize(30px);
					margin-left: realSize(20px);
					margin-right: realSize(20px);
				}
			}
		}

		.header_content {
			display: flex;
			flex-direction: row;

			.left {
				display: flex;
				flex-direction: column;
				width: 57%;
				margin-top: 10px;
				margin-left: 15px;
				margin-right: 15px;

				.title {
					width: realSize(419px);
					height: realSize(59px);
					font-size: realSize(47px);
					font-weight: bold;
					color: rgba(255, 255, 255, 1);
				}

				.sub_title {
					margin-top: 3px;
					font-size: realSize(18px);
					font-weight: 400;
					color: rgba(255, 255, 255, 1);

					background: linear-gradient(0deg, rgba(120, 255, 224, 1) 0%, rgba(255, 255, 255, 1) 100%);
					-webkit-background-clip: text;
					-webkit-text-fill-color: transparent;
				}

				.btn {
					margin-top: 3px;
					width: realSize(198px);
					height: realSize(60px);
					background: linear-gradient(-30deg, rgba(252, 135, 29, 1), rgba(246, 185, 9, 1));
					box-shadow: 0px 4px 10px 0px rgba(255, 121, 0, 0.5);
					border-radius: realSize(30px);
					color: rgba(255, 255, 255, 1);
					display: flex;
					align-items: center;
					justify-content: center;
				}
			}
		}
	}

	.page_content {
		width: 100%;
		margin-top: -74px;

		.menu {
			margin-left: 10px;
			margin-right: 10px;
			padding-left: 10px;
			padding-right: 10px;
			height: realSize(176px);
			background: rgba(255, 255, 255, 1);
			box-shadow: 0px 10px 10px 0px rgba(0, 161, 124, 0.1);
			border-radius: 10px;
			display: flex;
			flex-direction: row;
			align-items: stretch;
			justify-content: space-between;

			.item {
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: center;

				.img_view {
					width: 60px;
					height: 60px;
					border-radius: 30px;
					display: flex;
					align-items: center;
					justify-content: center;

					.image {
						width: 300px;
						height: 100px;
					}
				}

				.txt {
					margin-top: 5px;
					font-size: 14px;
					color: rgba(51, 51, 51, 1);
				}
			}
		}

		.s_menu {
			display: flex;
			flex-direction: row;
			align-items: stretch;
			justify-content: space-between;
			margin-top: 15px;
			margin-left: 10px;
			margin-right: 10px;
			padding-left: 10px;
			padding-right: 10px;

			.item {
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: center;

				.image {
					width: 100px;
					height: 100px;
				}

				.txt {
					margin-top: 5px;
					font-size: 14px;
					color: rgba(51, 51, 51, 1);
				}
			}
		}

		.ad {
			width: 100%;
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: center;

			.bg {
				position: absolute;
				width: 80px;
				height: 105px;
				left: 0;
			}

			.ad_btn {
				width: 100%;
				height: 63px;
				margin: 30px;
				background: linear-gradient(0deg, rgba(253, 155, 28, 1), rgba(251, 197, 33, 1));
				border-radius: 67px;
				display: flex;
				flex-direction: column;
				align-items: center;
				justify-content: center;

				.title {
					font-size: realSize(38px);
					font-family: PingFang-SC-Heavy;
					font-weight: 800;
					color: rgba(255, 255, 255, 1);
				}

				.sub_title {
					background: linear-gradient(0deg, rgba(255, 128, 37, 1), rgba(255, 153, 32, 1));
					box-shadow: 0px 4px 5px 0px rgba(92, 53, 48, 0.3), 0px 1px 0px 0px rgba(228, 228, 228, 1);
					border-radius: realSize(24px);
					font-size: realSize(24px);
					font-family: PingFang-SC-Heavy;
					font-weight: 800;
					font-style: italic;
					color: rgba(255, 236, 177, 1);
					line-height: realSize(26px);
				}
			}
		}
	}

	.slider {
		white-space: nowrap;
		width: 100%;
		background-color: white;

		.item {
			display: inline-block;
			margin-left: 15px;
			margin-top: 13px;
			margin-bottom: 13px;
			width: 30%;
			height: 195px;
			border-radius: 10px;

			.item_content {
				display: flex;
				flex-direction: row;

				.title {
					width: 36%;
					margin: 20px;
					display: flex;
					flex-direction: column;
					
					.first {
						font-size: 16px;
						color:rgba(46,65,69,1);
					}
					.main {
						font-size: 13px;
						color:rgba(79,103,101,1);
						margin-top: 5px;
					}
					.sub {
						width: 60px;
						font-size: 10px;
						margin-top: 20px;
						background:rgba(255,255,255,0.4);
						border-radius:5px;
						display: flex;
						align-items: center;
						justify-content: center;
					}
				}

				.image {
					margin-top: 1px;
					width: 380px;
					height: 180px;
				}

				.free {
					background: rgba(11, 147, 252, 1);
					border-radius: 0px 0px 22px 22px;
					width: 45px;
					height: 50px;
					display: flex;
					align-items: center;
					justify-content: center;
					color: #FFFFFF;
					font-size: 14px;
				}
			}
		}
	}
</style>
