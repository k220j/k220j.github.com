<template>
    <div>
        <Navbar></Navbar>
        <div class="container">
            <Header></Header>
            <About></About>
            <Experience></Experience>
            <Project></Project>
            <Skill></Skill>
            <Footer></Footer>
        </div>
    </div>
</template>

<script>
	import Navbar from '../components/Common/Navbar'
	import Experience from '../components/Common/Experience'
	import Header from '../components/Common/Header'
	import About from '../components/Common/About'
	import Project from '../components/Common/Project'
	import Skill from '../components/Common/Skill'
	import Footer from "../components/Common/Footer";

	export default {
		name: "index.vue",
		components: {
			'Navbar': Navbar,
			'Header': Header,
			'Experience': Experience,
			'About': About,
			'Project': Project,
			'Skill': Skill,
			'Footer': Footer
		}
	}
</script>

<style scoped>

</style>
