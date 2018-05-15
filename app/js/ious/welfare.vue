<template lang="html">
  <Panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t18103/37/490404196/5076/dfe2d74f/5a8440f1Nbda4f02a.png?width=90&height=90" alt="">
        <div>
          <h4>开通白条</h4>
          <p>送188元礼包</p>
        </div>
        <em>立即开通 > </em>
      </div>
      <div :class="$style.item">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t18073/271/483133084/5159/f8133cd6/5a844103N02f95449.png?width=90&height=90" alt="">
        <div>
          <h4>白条闪付</h4>
          <p>新手享158元礼包</p>
        </div>
        <em>随机立减 > </em>
      </div>
      <div :class="$style.item">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t17563/145/489151866/3943/bed46aef/5a8440cfN4a1fabc3.png?width=90&height=90" alt="">
        <div>
          <h4>白条提额</h4>
          <p>金融app专享提额礼包</p>
        </div>
        <em>去提额 > </em>
      </div>
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
    > h4 {
        border-bottom: 1px solid #ddd;
    }
    .content {
        @include list;
        .item {
            @include list(row);
            align-items: center;
            height: 140px;
            &:after {
                content: " ";
                display: block;
                width: 100%;
                height: 0;
                box-sizing: border-box;
                border-bottom: 1px solid #ddd;
                margin-left: 150px;
            }
            &:last-child:after {
                border-color: #fff;
            }
            > img {
                width: 90px;
                height: 90px;
                display: inline-block;
                margin: 0 32px;
            }
            div {
                font-size: 32px;
                color: #333;
                line-height: 1.8;
                width: 304px;
                p {
                    color: #999;
                    font-size: 24px;
                    line-height: 1.1;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    overflow: hidden;
                }
            }
            > em {
                color: #ff801a;
                font-size: 28px;
            }
        }
    }
}
</style>
