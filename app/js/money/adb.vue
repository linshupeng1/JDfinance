<template lang="html">
  <Panel title="理财专享" :class="$style.panel">
    <section :class="$style.content">
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t17557/268/1745067789/52958/4fb44a40/5ad5bbf5N6b27ccf0.jpg?width=750&height=200" alt="">
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
