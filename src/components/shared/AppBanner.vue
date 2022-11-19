<script>
import feather from 'feather-icons';

export default {
	name: 'Home',
	data: () => {
		return {
			theme: '',
		};
	},
	created() {
		this.theme = localStorage.getItem('theme') || 'light';
	},
	mounted() {
		feather.replace();
		this.theme = localStorage.getItem('theme') || 'light';
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>

<template>
	<section
		class="flex flex-col sm:justify-between items-center sm:flex-row mt-12 sm:mt-10 intro-row"
	>
		<!-- Banner left contents -->
		<div class="w-full md:w-1/3 text-left">
			<h1
				class="font-general-semibold text-3xl md:text-3xl xl:text-4xl text-center sm:text-left text-ternary-dark dark:text-primary-light "
			>
				Hi, my name is Ben :)
			</h1>
			<p
				class="font-general-medium mt-2 text-lg sm:text-xl  xl:text-2xl text-center sm:text-left leading-none text-gray-400"
			>
			Born and raised in Seattle, living in San Diego. Currently working as a freelance web developer and co founder of an online marketplace. In my day to day i have a lot of priorities, code and security are right up at the top.			</p>
			<div class="flex justify-center sm:block">
				<a
					download="Benjamin-Paris-Resume.pdf"
					href="/files/Benjamin-Paris-Resume.pdf"
					class="flex justify-center items-center w-36 sm:w-48 mt-12 mb-6 sm:mb-0 text-lg border-indigo-200 dark:border-ternary-dark py-2.5 sm:py-3 shadow-lg rounded-lg bg-indigo-50 focus:ring-1 focus:ring-indigo-900 hover:bg-emerald-600 text-gray-500 hover:text-white duration-500"
					aria-label="Download Resume"
				>
					<i
						data-feather="arrow-down-circle"
						class="ml-0 sm:ml-1 mr-2 sm:mr-3 w-5 sm:w-6 duration-100"
					></i>
					<span
						class="text-sm sm:text-lg font-general-medium duration-100"
						>Resume</span
					></a
				>
			</div>
		</div>

		<!-- Banner right illustration -->
		<div class="w-full md:w-2/3 banner-illustration">
			<img
				v-if="theme === 'light'"
				src="@/assets/images/code2.svg"
				alt="Developer"
			/>
			<img
				v-else
				src="@/assets/images/code2.svg"
				alt="Developer"
			/>
		</div>
	</section>
</template>

<!-- <style scoped>
.intro-row {
	display: flex;
	flex-direction: row;

}
.banner-illustration {
	padding: 0px;
	display: flex;
	flex-direction: row;
	justify-content: flex-end;
}
</style> -->
