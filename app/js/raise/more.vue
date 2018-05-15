<template lang="html">
<Panel title="更多福利" :class="$style.panel">
  <section :class="$style.content">
    <img src="//img12.360buyimg.com/jrpmobile/jfs/t12355/171/849656870/29064/92c9bc12/5a153643N04efba6e.jpg?width=210&height=260" alt="">
    <img src="//img12.360buyimg.com/jrpmobile/jfs/t9697/338/291348712/12737/27e1204/59cb6304Naef85042.jpg?width=210&height=260" alt="">
    <img src="//img12.360buyimg.com/jrpmobile/jfs/t10360/347/311063647/10881/14a5cd40/59cb632fNcac82571.jpg?width=210&height=260" alt="">
    <span>专享福利 ></span>
  </section>
</Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
	components: {
		Panel,
	},
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .content {
        position: relative;
        @include flex(row);
        padding-bottom: 40px;
        img {
            width: 33.3333%;
        }
        span {
            position: absolute;
            right: 20px;
            top: -110px;
            font-size: 28px;
            color: #999;
            height: 112px;
            line-height: 112px;
        }
    }
}
</style>
