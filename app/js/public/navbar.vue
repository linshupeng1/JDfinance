<template lang="html">
<ul :class="$style.nav">
  <li v-for="item in items" :key="item.img">
    <router-link :to="{ name: item.href }">
      <img :src="item.img" :alt="item.title">
      <p>{{item.title}}</p>
    </router-link>
  </li>
</ul>
</template>

<script>
export default {
	data() {
		return {
			items: [{
				href: "home",
				img: "//img12.360buyimg.com/jrpmobile/jfs/t17587/158/1300523690/1908/eabacaac/5ac4850bNdf876dd8.png?width=60&height=60",
				title: "首页"
			}, {
				href: "money",
				img: "//img12.360buyimg.com/jrpmobile/jfs/t7690/252/3621724688/1715/757a3ca1/59e9d81bN27304850.png?width=60&height=60",
				title: "赚钱"
			}, {
				href: "ious",
				img: "//img12.360buyimg.com/jrpmobile/jfs/t11653/76/201131398/1192/bf1b2852/59e9d7f3N5f691137.png?width=60&height=60",
				title: "白条"
			}, {
				href: "raise",
				img: "//img12.360buyimg.com/jrpmobile/jfs/t19729/201/1027312338/1395/95cecd48/5ab85d0eN01f81011.png?width=56&height=56",
				title: "众筹"
			}, {
				href: "home",
				img: "//img12.360buyimg.com/jrpmobile/jfs/t10897/141/1894216742/2046/ad0e8dc1/59e9d7feNaa5dd2fd.png?width=60&height=60",
				title: "金融会员"
			}]
		}
	}
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.nav {
    @include list(row);
    justify-content: space-around;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100px;
    text-align: center;
    background-color: #fff;
    z-index: 1000;
    li {
        img {
            width: 44px;
            height: 44px;
            display: inline-block;
            margin: 12px auto 6px;
        }
        p {
            font-size: 22px;
            margin-bottom: 12px;
            color: #B1B4BB;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
        }
        a {
            text-decoration: none;
        }
    }
}
</style>
