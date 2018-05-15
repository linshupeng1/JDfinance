<template lang="html">
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Welfare></Welfare>
        <Service></Service>
        <Footor></Footor>
        <Nav></Nav>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Slider from "./islider.vue"
import Footor from "../public/footer.vue"
import Nav from "../public/navbar.vue"
import Welfare from "./welfare.vue"
import Service from "./service.vue"
export default {
	components: {
		Heador,
		Slider,
		Service,
		Footor,
		Nav,
		Welfare,
	}
}
</script>

<style lang="scss">
</style>
