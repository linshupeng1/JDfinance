<template lang="html">
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Ada></Ada>
        <Money></Money>
        <Adb></Adb>
        <Finance></Finance>
        <Adc></Adc>
        <Footor cname="mfooter"></Footor>
        <Nav></Nav>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Slider from "./mslider.vue"
import Footor from "../public/footer.vue"
import Nav from "../public/navbar.vue"
import Ada from "./ada.vue"
import Money from "./money.vue"
import Adb from "./adb.vue"
import Finance from "./finance.vue"
import Adc from "./adc.vue"
export default {
	components: {
		Heador,
		Slider,
		Footor,
		Nav,
		Ada,
		Money,
		Adb,
		Finance,
		Adc,
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
