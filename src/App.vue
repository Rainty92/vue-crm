<template>
  <div id="app">
	  <component :is="layout">
		  <router-view />
	  </component>
	  <button class="btn">test</button>
    <router-view />
  </div>
</template>

<script>
import EmptyLayout from '../src/layouts/EmptyLayout'
import MainLayout from '../src/layouts/MainLayout'
export default {
	computed: {
		layout(){
			console.log()
			return (this.$route.meta.layout || 'empty') + '-layout'
		}
	},
	components: {
		EmptyLayout, MainLayout
	}
}
</script>

<style>
@import '../node_modules/materialize-css/dist/css/materialize.min.css';
@import 'assets/index.css';
</style>