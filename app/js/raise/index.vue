<template lang="html">
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Daily></Daily>
        <In></In>
        <More></More>
        <Footor cname="mfooter"></Footor>
        <Nav></Nav>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Slider from "./rslider.vue"
import Footor from "../public/footer.vue"
import Nav from "../public/navbar.vue"
import Daily from "./daily.vue"
import In from "./in.vue"
import More from "./more.vue"
export default {
	components: {
		Heador,
		Slider,
		Daily,
		In,
		More,
		Footor,
		Nav,
	}
}
</script>

<style lang="scss">
.mfooter {
    margin-top: 0!important;
    ul {
        > li:first-child {
            display: none;
        }
    }
}
</style>
