<template lang="html">
  <Panel title="每日签到" :class="$style.panel">
    <section :class="$style.content">
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t18319/288/2020359902/20747/e4c1e6d4/5ae28f3bN8d2fabad.png?width=375&height=233" alt="">
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t14215/140/1757206721/24186/81b4e53c/5a56c877Nee6cfc4d.jpg?width=375&height=233" alt="">
      <p>不抢白不抢</p>
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
    .content {
        @include flex(row);
        padding-bottom: 40px;
        position: relative;
        img {
            width: 50%;
        }
        p {
            position: absolute;
            top: -112px;
            right: 20px;
            font-size: 28px;
            color: #999;
            height: 112px;
            line-height: 112px;
        }
    }
}
</style>
