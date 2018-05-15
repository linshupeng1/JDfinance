<template lang="html">
  <Panel title="金融头条" :class="$style.panel">
    <section :class="$style.content">
      <swiper :options="options">
        <swiper-slide>签到领流量，1元500M！<em>></em></swiper-slide>
        <swiper-slide>百万白条劵免费送，速来领取！<em>></em></swiper-slide>
      </swiper>
    </section>
  </Panel>
</template>

<script>
import {
	swiper,
	swiperSlide
} from "vue-awesome-swiper"
import Panel from "../core/panel.vue"
export default {
	components: {
		Panel,
		swiper,
		swiperSlide,
	},
	data() {
		return {
			options: {
				autoplay: true,
				loop: true,
				direction: "vertical"
			}
		}
	}
}
</script>

<style lang="scss">
.swiper-container-vertical {
    height: 72px;
    .swiper-slide {
        font-size: 26px;
        color: #333;
        em {
            float: right;
            color: #ddd;
            margin-right: 20px;
        }
    }
}
</style>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    > h4 {
        display: none;
    }
    margin-top: 120px!important;
    .content {
        height: 72px;
        line-height: 72px;
        overflow: hidden;
        padding-left: 100px;
    }
}
</style>
