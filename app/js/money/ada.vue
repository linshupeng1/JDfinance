<template lang="html">
  <Panel title="神劵满" :class="$style.panel">
    <section :class="$style.content">
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t17407/121/1977672487/47678/b8401acf/5ae1afdcNe567341a.jpg?width=750&height=280" alt="">
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
	components: {
		Panel,
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
    .content {
        img {
            width: 100%;
        }
    }
}
</style>
