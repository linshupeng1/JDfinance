<template lang="html">
  <Panel title="轮播图" :class="$style.panel">
    <section :class="$style.content">
      <Slider :items="items" :cname="$style.slider"></Slider>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
	components: {
		Panel,
		Slider,
	},
	data() {
		return {
			items: [{
				href: "home",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t18253/252/2000522394/20361/a0a10959/5ae1b168N74c8f1e2.jpg?width=750&height=400"
			}, {
				href: "home2",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t17017/220/2024924255/22513/37089e7/5ae1b1b7Nc31ce8a2.jpg?width=750&height=400"
			}, {
				href: "home3",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t18712/333/2027735516/20081/7bfe412/5ae1b2a0Nf2069048.png?width=750&height=400"
			}]
		}
	}
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    > h4 {
        display: none;
    }
    .slider {
        margin-top: 120px;
        img {
            width: 100%;
        }
    }
}
</style>
