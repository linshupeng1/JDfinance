<template lang="html">
<Panel title="下载APP" :class="$style.panel">
  <section :class="$style.content">
    a
  </section>
</Panel>
</template>

<script>
import Panel from "../core/panel.vue"
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
    .content {}
}
</style>
