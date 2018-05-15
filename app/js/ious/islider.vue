<template lang="html">
  <Panel title="轮播图" :class="$style.panel">
    <section :class="$style.slider">
      <Slider :items="items"></Slider>
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
				href: "ious",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t19978/8/68505992/20361/a0a10959/5ae317f8N6108af00.jpg?width=750&height=400"
			}, {
				href: "ious1",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t19411/51/2023159621/25756/c0a8f9cb/5ae317bdN90a8c34e.jpg?width=750&height=400"
			}, {
				href: "ious2",
				src: "//img12.360buyimg.com/jrpmobile/jfs/t18127/133/2026400105/47817/5a14a72c/5ae317edN25d1dbc7.png?width=750&height=400"
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
