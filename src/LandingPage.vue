<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
class Member {
	constructor(name, studies, imagePath) {
		this.name = name
		this.studies = studies
		this.imagePath = imagePath
	}
}

// Taken from https://stackoverflow.com/a/12646864
// Randomize array in-place using Durstenfeld shuffle algorithm
function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
    }
}

let members = [
	new Member("Johannes Frey", "Master of Science (M.Sc.) Robotics, Cognition, Intelligence", "images/people/JohannesFrey-MA-RCI.jpg"),
	new Member("Leon Kiesgen", "Master of Science (M.Sc.) Robotics, Cognition, Intelligence", "images/people/LeonKiesgen_MA-RCI.jpg"),
	new Member("Marios Spanakakis", "Master of Science (M.Sc.) Mechatronics & Robotics", "images/people/MariosSpanakakis_MasterMechatronicsAndRobotics.png"),
	new Member("Vincent Bürgin", "Master of Science (M.Sc.) Informatics", "images/people/VincentBürgin-MasterInformatics.jpg"),
	new Member("Sonja Groß", "PhD Munich Institute of Robotics and Machine Intelligence (MIRMI)", "images/people/SonjaGroß_MSc_Biomedical_Engineering.jpg"),
	new Member("Silija Breimann", "Master of Science (M.Sc.) Mechatronics & Robotics", "images/people/SilijaBreimann_MasterMechatronicsAndRobotics.jpg"),
	new Member("Negar Shahmoradi", "Master of Science (M.Sc.) MS-Medizintechnik", "images/people/NegarShahmoradi_MS-Medizintechnik.jpg"),
]

shuffleArray(members)
</script>

<template>
<body class="leading-normal tracking-normal text-gray-900" style="font-family: 'Source Sans Pro', sans-serif;">



<div class="h-screen pb-14 bg-right bg-cover" style="background-image:url('images/hand.jpg');">
	<!--Nav-->
	<div class="w-auto mx-10 p-6">
			
		<div class="w-full flex items-center justify-between">
			<a class="flex items-center text-indigo-400 no-underline hover:no-underline font-bold text-2xl lg:text-4xl"  href="#"> 
				<img class="h-24" src="images/logos/Enhands_Full_Logo.svg">
			</a>
			
			<div class="flex w-1/2 justify-end content-center">		
				<a class="inline-block text-blue-300 no-underline hover:text-indigo-800 hover:text-underline text-center h-10 p-2 md:h-auto md:p-4" data-tippy-content="@twitter_handle" href="https://twitter.com/intent/tweet?url=#">
					<svg class="fill-current h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><path d="M30.063 7.313c-.813 1.125-1.75 2.125-2.875 2.938v.75c0 1.563-.188 3.125-.688 4.625a15.088 15.088 0 0 1-2.063 4.438c-.875 1.438-2 2.688-3.25 3.813a15.015 15.015 0 0 1-4.625 2.563c-1.813.688-3.75 1-5.75 1-3.25 0-6.188-.875-8.875-2.625.438.063.875.125 1.375.125 2.688 0 5.063-.875 7.188-2.5-1.25 0-2.375-.375-3.375-1.125s-1.688-1.688-2.063-2.875c.438.063.813.125 1.125.125.5 0 1-.063 1.5-.25-1.313-.25-2.438-.938-3.313-1.938a5.673 5.673 0 0 1-1.313-3.688v-.063c.813.438 1.688.688 2.625.688a5.228 5.228 0 0 1-1.875-2c-.5-.875-.688-1.813-.688-2.75 0-1.063.25-2.063.75-2.938 1.438 1.75 3.188 3.188 5.25 4.25s4.313 1.688 6.688 1.813a5.579 5.579 0 0 1 1.5-5.438c1.125-1.125 2.5-1.688 4.125-1.688s3.063.625 4.188 1.813a11.48 11.48 0 0 0 3.688-1.375c-.438 1.375-1.313 2.438-2.563 3.188 1.125-.125 2.188-.438 3.313-.875z"></path></svg>
				</a>
				<a class="inline-block text-blue-300 no-underline hover:text-indigo-800 hover:text-underline text-center h-10 p-2 md:h-auto md:p-4 " data-tippy-content="#facebook_id" href="https://www.facebook.com/sharer/sharer.php?u=#">
					<svg class="fill-current h-6" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><path d="M19 6h5V0h-5c-3.86 0-7 3.14-7 7v3H8v6h4v16h6V16h5l1-6h-6V7c0-.542.458-1 1-1z"></path></svg>
				</a>
			</div>
			
		</div>

	</div>

	<!--Main-->
	<div class=" pt-24 md:pt-48 px-6 mx-10 flex flex-wrap flex-col md:flex-row items-center">
		
		<!--Left Col-->
		<div class="flex flex-col w-full xl:w-2/5 justify-center lg:items-start overflow-y-hidden">
			<h1 class="slide-in-bottom mb-4 text-4xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-6xl dark:text-white">Enabling <span class="underline underline-offset-3 decoration-8 decoration-blue-400 hover:text-indigo-600 dark:decoration-blue-600">accessible</span> prosthetic hands</h1>
			<p class="leading-normal text-base md:text-2xl mb-8 text-center md:text-left slide-in-bottom-subtitle">Helping others, regardless of location or circumstance, one hand at a time.</p>
	
			<button type="button" class="fade-in text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-base px-5 py-2.5 text-center inline-flex items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
				Join us!
				<svg aria-hidden="true" class="ml-2 -mr-1 w-5 h-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
			</button>

		</div>
		
		<!--Right Col-->
		<div class="w-full xl:w-3/5 py-6 overflow-y-hidden">
			<img class="w-5/6 hidden sm:block mx-auto lg:mr-0 slide-in-bottom" src="devices.svg">
		</div>
	</div>

		<!-- This example requires Tailwind CSS v2.0+ -->
		<div class="bg-white">
			<div class="max-w-2xl mx-auto py-24 px-4 grid items-center grid-cols-1 gap-y-16 gap-x-8 sm:px-6 sm:py-32 lg:max-w-7xl lg:px-8 lg:grid-cols-2">
			<div>
				<h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:tracking-tight sm:text-4xl">Technical Specifications</h2>
				<p class="mt-4 text-gray-500">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum.</p>
		
				<dl class="mt-16 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 sm:gap-y-16 lg:gap-x-8">
				<div class="border-t border-gray-200 pt-4">
					<dt class="font-medium text-gray-900">Origin</dt>
					<dd class="mt-2 text-sm text-gray-500">Designed by Lorem ipsum, Inc.</dd>
				</div>
		
				<div class="border-t border-gray-200 pt-4">
					<dt class="font-medium text-gray-900">Material</dt>
					<dd class="mt-2 text-sm text-gray-500">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed</dd>
				</div>
		
				<div class="border-t border-gray-200 pt-4">
					<dt class="font-medium text-gray-900">Dimensions</dt>
					<dd class="mt-2 text-sm text-gray-500">6.25&quot; x 3.55&quot; x 1.15&quot;</dd>
				</div>
		
				<div class="border-t border-gray-200 pt-4">
					<dt class="font-medium text-gray-900">Finish</dt>
					<dd class="mt-2 text-sm text-gray-500">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed</dd>
				</div>
		
				<div class="border-t border-gray-200 pt-4">
					<dt class="font-medium text-gray-900">Includes</dt>
					<dd class="mt-2 text-sm text-gray-500">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed</dd>
				</div>
		
				<div class="border-t border-gray-200 pt-4">
					<dt class="font-medium text-gray-900">Considerations</dt>
					<dd class="mt-2 text-sm text-gray-500">Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed</dd>
				</div>
				</dl>
			</div>
			<div class="grid grid-cols-2 grid-rows-2 gap-4 sm:gap-6 lg:gap-8">
				<img src="images/prototyp/devHand1.png" alt="Walnut card tray with white powder coated steel divider and 3 punchout holes." class="bg-gray-100 rounded-lg">
				<img src="images/prototyp/devHand2.png" alt="Top down view of walnut card tray with embedded magnets and card groove." class="bg-gray-100 rounded-lg">
				<img src="images/prototyp/devHand5.png" alt="Side of walnut card tray with card groove and recessed card area." class="bg-gray-100 rounded-lg">
				<img src="images/prototyp/devHand1.png" alt="Walnut card tray filled with cards and card angled in dedicated groove." class="bg-gray-100 rounded-lg">
			</div>
			</div>
		</div>




		<!--About Us-->
		<div class="max-w-2xl mx-auto py-24 px-4 grid items-center grid-cols-1 gap-y-16 gap-x-8 sm:px-6 sm:py-32 lg:max-w-7xl lg:px-8 ">
			<h2 class="text-center text-3xl font-bold tracking-tight text-gray-900 sm:tracking-tight sm:text-4xl">Meet our Team 👨‍👩‍👧‍👧</h2>
			<div class="flex gap-6 flex-wrap justify-center "  >
				<div v-for="member in members" v-bind:key="member.name" class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" :src=member.imagePath alt="Team member profile picture">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">{{member.name}}</div>
					<p class="text-gray-700 text-base">
						{{member.studies}}
					</p>
					</div>
				</div>


				<!-- Card 1
				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/JohannesFrey-MA-RCI.jpg" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Johannes Frey</div>
					<p class="text-gray-700 text-base">
						Master of Science (M.Sc.) Robotics, Cognition, Intelligence
					</p>
					</div>
				</div>
				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/LeonKiesgen_MA-RCI.jpg" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Leon Kiesgen</div>
					<p class="text-gray-700 text-base">
						Master of Science (M.Sc.) Robotics, Cognition, Intelligence
					</p>
					</div>
				</div>
				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/MariosSpanakakis_MasterMechatronicsAndRobotics.png" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Marios Spanakakis</div>
					<p class="text-gray-700 text-base">
						Master of Science (M.Sc.) Mechatronics & Robotics
					</p>
					</div>
				</div>

				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/VincentBürgin-MasterInformatics.jpg" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Vincent Bürgin</div>
					<p class="text-gray-700 text-base">
						Master of Science (M.Sc.) Informatics
					</p>
					</div>
				</div>

				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/SonjaGroß_MSc_Biomedical_Engineering.jpg" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Sonja Groß</div>
					<p class="text-gray-700 text-base">
						PhD Munich Institute of Robotics and Machine Intelligence (MIRMI)
					</p>
					</div>
				</div>

				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/SilijaBreimann_MasterMechatronicsAndRobotics.jpg" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Silija Breimann</div>
					<p class="text-gray-700 text-base">
						Master of Science (M.Sc.) Mechatronics & Robotics
					</p>
					</div>
				</div>
				
				<div class="w-60 rounded overflow-hidden shadow-lg">
					<img class="w-full" src="images/people/NegarShahmoradi_MS-Medizintechnik.jpg" alt="Mountain">
					<div class="px-6 py-4">
					<div class="font-bold text-xl mb-2">Negar Shahmoradi</div>
					<p class="text-gray-700 text-base">
						Master of Science (M.Sc.) MS-Medizintechnik
					</p>
					</div>
				</div> -->
				

		</div>
		</div>
		
		<!--Footer-->
		
		<footer class="p-4 bg-white rounded-lg shadow md:flex md:items-center md:justify-between md:p-6 dark:bg-gray-800">
			<span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2022 <a href="http://enhands.de" class="hover:underline">EnHands</a>. All Rights Reserved.
			</span>
			<ul class="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
				<li>
					<a href="#" class="mr-4 hover:underline md:mr-6 ">About</a>
				</li>
				<li>
					<a href="#" class="mr-4 hover:underline md:mr-6">Privacy Policy</a>
				</li>
				<li>
					<a href="#" class="mr-4 hover:underline md:mr-6">Licensing</a>
				</li>
				<li>
					<a href="#" class="hover:underline">Contact</a>
				</li>
			</ul>
		</footer>

		
	
	

</div>


  <!-- jQuery if you need it
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  -->

</body>



  <!-- <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
/* ----------------------------------------------
* Generated by Animista
* w: http://animista.net, t: @cssanimista
* ---------------------------------------------- */

.slide-in-bottom{-webkit-animation:slide-in-bottom .5s cubic-bezier(.25,.46,.45,.94) both;animation:slide-in-bottom .5s cubic-bezier(.25,.46,.45,.94) both}
.slide-in-bottom-h1{-webkit-animation:slide-in-bottom .5s cubic-bezier(.25,.46,.45,.94) .5s both;animation:slide-in-bottom .5s cubic-bezier(.25,.46,.45,.94) .5s both}
.slide-in-bottom-subtitle{-webkit-animation:slide-in-bottom .5s cubic-bezier(.25,.46,.45,.94) .75s both;animation:slide-in-bottom .5s cubic-bezier(.25,.46,.45,.94) .75s both}
.fade-in{-webkit-animation:fade-in 1.2s cubic-bezier(.39,.575,.565,1.000) 1s both;animation:fade-in 1.2s cubic-bezier(.39,.575,.565,1.000) 1s both}
.bounce-top-icons{-webkit-animation:bounce-top .9s 1s both;animation:bounce-top .9s 1s both}

@-webkit-keyframes slide-in-bottom{0%{-webkit-transform:translateY(1000px);transform:translateY(1000px);opacity:0}100%{-webkit-transform:translateY(0);transform:translateY(0);opacity:1}}@keyframes slide-in-bottom{0%{-webkit-transform:translateY(1000px);transform:translateY(1000px);opacity:0}100%{-webkit-transform:translateY(0);transform:translateY(0);opacity:1}}
@-webkit-keyframes bounce-top{0%{-webkit-transform:translateY(-45px);transform:translateY(-45px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in;opacity:1}24%{opacity:1}40%{-webkit-transform:translateY(-24px);transform:translateY(-24px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}65%{-webkit-transform:translateY(-12px);transform:translateY(-12px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}82%{-webkit-transform:translateY(-6px);transform:translateY(-6px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}93%{-webkit-transform:translateY(-4px);transform:translateY(-4px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}25%,55%,75%,87%{-webkit-transform:translateY(0);transform:translateY(0);-webkit-animation-timing-function:ease-out;animation-timing-function:ease-out}100%{-webkit-transform:translateY(0);transform:translateY(0);-webkit-animation-timing-function:ease-out;animation-timing-function:ease-out;opacity:1}}@keyframes bounce-top{0%{-webkit-transform:translateY(-45px);transform:translateY(-45px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in;opacity:1}24%{opacity:1}40%{-webkit-transform:translateY(-24px);transform:translateY(-24px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}65%{-webkit-transform:translateY(-12px);transform:translateY(-12px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}82%{-webkit-transform:translateY(-6px);transform:translateY(-6px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}93%{-webkit-transform:translateY(-4px);transform:translateY(-4px);-webkit-animation-timing-function:ease-in;animation-timing-function:ease-in}25%,55%,75%,87%{-webkit-transform:translateY(0);transform:translateY(0);-webkit-animation-timing-function:ease-out;animation-timing-function:ease-out}100%{-webkit-transform:translateY(0);transform:translateY(0);-webkit-animation-timing-function:ease-out;animation-timing-function:ease-out;opacity:1}}
@-webkit-keyframes fade-in{0%{opacity:0}100%{opacity:1}}@keyframes fade-in{0%{opacity:0}100%{opacity:1}}
				

/* .logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
} */
</style>
