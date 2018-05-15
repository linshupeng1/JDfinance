<template lang="html">
  <Panel title="更多服务" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item" v-for="item in items" :key="item.img">
        <img :src="item.href" :alt="item.title">
        <p>{{ item.title }}</p>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
	components: {
		Panel,
	},
	data() {
		return {
			items: [{
				href: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
				title: "小白卡"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
				title: "白条商城"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
				title: "消费分期"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
				title: "借钱"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90",
				title: "白条提额"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90",
				title: "白条闪付"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88",
				title: "小白会玩"
			}, {
				href: "//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90",
				title: "钢镚"
			}]
		}
	}
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .content {
        @include flex(row);
        justify-content: space-around;
        .item {
            text-align: center;
            width: 25%;
            margin-bottom: 40px;
            img {
                width: 90px;
                height: 90px;
            }
            p {
                font-size: 26px;
                color: #666;
                margin-top: 10px;
            }
        }
    }
}
</style>
