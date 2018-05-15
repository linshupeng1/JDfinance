<template lang="html">
  <Panel title="精品推荐" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.arrow">更多尖货></div>
      <Slider :options="options" :items="items" cname="product-slider"></Slider>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
import Slider from "../core/slider.vue";
export default {
	components: {
		Panel,
		Slider,
	},
	data() {
		return {
			items: [{
				href: "home1",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t17692/108/1667948905/47352/b3b5fec5/5ad4077bN829fc64d.jpg?width=335&height=421"
			}, {
				href: "home2",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t17017/315/1681990516/35892/46d5d0e/5ad40797Nd8624d82.jpg?width=335&height=421"
			}, {
				href: "home3",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t17977/1/1701720589/44385/219809f6/5ad407a8N8feeb421.jpg?width=335&height=421"
			}, {
				href: "home4",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t18598/49/1683491486/34072/cb622afa/5ad407b7N95527875.jpg?width=335&height=421"
			}],
			options: {
				// pagination: {
				// 	el: '.swiper-pagination',
				// 	clickable: true
				// },
				slidesPerView: 2.3,
				spaceBetween: 30,
				freeMode: true
			}
		}
	}
}
</script>
<style lang="scss">
.product-slider {
    .swiper-container {
        box-sizing: border-box;
        padding: 0 24px;
        .swiper-slide {
            a {
                display: inline-block;
                width: 100%;
                img {
                    width: 100%;
                    display: block;
                    border: 1px solid #eee;
                    height: 314px;
                }
            }
        }
    }
}
</style>
<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .content {
        padding-bottom: 40px;
        position: relative;
        .arrow {
            position: absolute;
            font-size: 28px;
            color: #999;
            right: 20px;
            top: -70px;
        }
    }
}
</style>
