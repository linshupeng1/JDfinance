<template lang="html">
  <Panel title="In货推荐" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item" v-for="item in items" :key="item.catory">
        <img :src="item.catory" alt="">
        <section :class="$style.list">
          <div :class="$style.product" v-for="list in item.list" :key="list.img">
            <img :src="list.img" alt="">
            <p :class="$style.title">{{list.title}}</p>
            <p :class="$style.price"><em>{{list.price}}</em>起</p>
            <article>
              <div :class="$style.wrapper">
                <div :class="$style.inner" :style="{width:list.progress+'%'}"></div>
              </div>
              <p>{{list.progress}}%</p>
            </article>
            <label v-if="list.flag">精选</label>
          </div>
        </section>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
	components: {
		Panel,
	},
	data() {
		return {
			items: [{
				catory: "//img12.360buyimg.com/jrpmobile/jfs/t17557/268/1745067789/52958/4fb44a40/5ad5bbf5N6b27ccf0.jpg?width=750&height=200",
				list: [{
					img: "//img30.360buyimg.com/cf/jfs/t5827/255/6140287884/111611/498f9693/59683808N9253369f.jpg",
					title: "GPD Win10口袋电脑",
					price: "75.00",
					progress: 100,
					flag: true,
				}, {
					img: "//img30.360buyimg.com/cf/jfs/t16507/63/2395886963/148713/e234d437/5ab49f62Nb7ddbe09.jpg",
					title: "专业级·碳纤维鱼竿Pro",
					price: "18.00",
					progress: 380,
					flag: false,
				}],
			}, {
				catory: "//img12.360buyimg.com/jrpmobile/jfs/t18631/176/1296661704/41624/f193c3f6/5ac2e521N06980907.png?width=750&height=200",
				list: [{
					img: "//img30.360buyimg.com/cf/jfs/t7480/64/3416297981/104254/df44574c/5aa87e57N52b3dd90.jpg",
					title: "褚橙之后看褚酒",
					price: "288.00",
					progress: 143,
					flag: false,
				}, {
					img: "//img30.360buyimg.com/cf/jfs/t19660/8/1460368804/125762/cb984c10/5acae308N8218b23a.jpg",
					title: "真静坊越南沉香手串",
					price: "188.00",
					progress: 512,
					flag: false,
				}],
			}, {
				catory: "//img12.360buyimg.com/jrpmobile/jfs/t19756/137/1902911799/17823/e19ffe7b/5add9511Nf6984e89.jpg?width=750&height=200",
				list: [{
					img: "//img30.360buyimg.com/cf/jfs/t8419/355/2020529518/140407/751c103f/59c3305dN9f4f5e82.jpg",
					title: "哲品π杯快客杯单人便携茶杯",
					price: "198.00",
					progress: 100,
					flag: false,
				}, {
					img: "//img30.360buyimg.com/cf/jfs/t11077/100/1285737947/152950/e31a8a11/5a0018b6N95b43b54.jpg",
					title: "OLA微信指纹锁-典藏版",
					price: "200.00",
					progress: 100,
					flag: false,
				}],
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
        @include flex;
        .item {

            > img {
                display: block;
                width: 100%;
                height: 200px;
            }
            .list {
                @include flex(row);
                justify-content: space-between;
                .product {
                    position: relative;
                    width: 48%;
                    height: 396px;
                    box-sizing: border-box;
                    background: #f1f1f1;
                    text-align: center;
                    margin-bottom: 20px;
                    img {
                        width: 180px;
                        height: 180px;
                        margin: 44px auto 20px;
                    }
                    .title {
                        font-family: PingFangSC-Regular;
                        font-size: 28px;
                        color: #444;
                        white-space: nowrap;
                        text-overflow: ellipsis;
                        overflow: hidden;
                    }
                    .price {
                        font-family: STHeitiSC-Medium;
                        font-size: 20px;
                        color: #999;
                        line-height: 48px;
                        em {
                            color: #f00;
                            font-size: 36px;
                            margin-right: 4px;
                            &:before {
                                content: "￥";
                                font-size: 28px;
                                color: #f00;
                            }
                        }
                    }
                }
                article {
                    @include flex(row);
                    align-items: center;
                    justify-content: space-around;
                    padding: 0 20px;
                    margin-top: 20px;
                    .wrapper {
                        width: 144px;
                        height: 10px;
                        background: #f3f5f7;
                        border-radius: 22px;
                        .inner {
                            width: 80%;
                            height: 10px;
                            max-width: 100%;
                            background-image: linear-gradient(270deg,#f55 1%,#ff9c31);
                            border-radius: 22px;
                        }
                    }
                    p {
                        font-size: 24px;
                        color: #999;
                        display: inline-block;
                        height: 10px;
                        line-height: 10px;
                        margin-left: 5px;
                    }
                }
                label {
                    position: absolute;
                    top: 0;
                    left: 0;
                    font-size: 20px;
                    padding: 6px 10px;
                    color: #f00;
                    background-color: #ccc;
                }
            }
        }
    }
}
</style>
