<template>
	<div class="informer-container">
		<Temperature v-bind:temperatureReal='weather.temperatureReal' v-bind:temperatureFeel='weather.temperatureFeel'/>
		<FlexBreak/>
		<Humidity v-bind:humidity='weather.humidity'/>
		<VerticalDivider/>
		<Wind v-bind:wind='weather.wind'/>
	</div>
</template>


<script>
import Temperature from './Temperature.vue'
import Humidity from './Humidity.vue'
import Wind from './Wind.vue'
import FlexBreak from './FlexBreak.vue'
import VerticalDivider from './VerticalDivider.vue'

export default {
	name: 'Container',
	props: ['weather'],
	components : {
		Temperature,
		Humidity,
		Wind,
		FlexBreak,
		VerticalDivider
	},
};
</script>


<style>
.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  padding: 30px;
  background-image: url('/img/forest.png');
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}
</style>
