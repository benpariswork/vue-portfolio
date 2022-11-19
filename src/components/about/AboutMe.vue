<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'Growing up in Seattle gave me the opportunity to build a seemingly endless toolkit, perfectly tailored for web development and security. I have formal training from University of Oregon Continuin Education, in the form of a Certificate in Cybersecurity. I have also been learning full stack web development for close to two years. My mentor for web development has guided me through the process of understanding front end and back end and all that lies in between.',
				},
				{
					id: 2,
					bio:
						' “Prior Planning Prevents Poor Performance”, George Paris',
				},
			],
		};
	},
};
</script>

<template>
	<div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
		<!-- About profile image -->
		<div class="w-full sm:w-1/4 mb-7 sm:mb-0">
			<img
				src="@/assets/images/security2.svg"
				class="rounded-xl w-96"
				alt=""
			/>
		</div>

		<!-- About details -->
		<div class="w-full sm:w-3/4 text-left">
			<p
				v-for="bio in bios"
				:key="bio.id"
				class="font-general-regular mb-4 text-ternary-dark dark:text-ternary-light text-lg"
			>
				{{ bio.bio }}
			</p>
		</div>
	</div>
</template>
