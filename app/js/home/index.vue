<template lang="html">
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Novice></Novice>
        <Borrow></Borrow>
        <Money></Money>
        <Product></Product>
        <Life></Life>
        <Footor></Footor>
        <Nav></Nav>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Slider from "./hslider.vue"
import Novice from "./novice.vue"
import Borrow from "./borrow.vue"
import Money from "./money.vue"
import Product from "./product.vue"
import Life from "./life.vue"
import Footor from "../public/footer.vue"
import Nav from "../public/navbar.vue"
export default {
	components: {
		Heador,
		Slider,
		Novice,
		Borrow,
		Money,
		Product,
		Life,
		Footor,
		Nav,
	}
}
</script>

<style lang="scss" module>

</style>
