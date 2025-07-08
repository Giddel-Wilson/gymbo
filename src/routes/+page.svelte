<script lang="ts">
	import { onMount } from 'svelte';
    import gymBro from '$lib/assets/image1.png';
    import gymBro2 from '$lib/assets/image2.png';
    import gymBro3 from '$lib/assets/image3.png';
	import ProgressBar from '$lib/components/ProgressBar.svelte';
	
	let mobileMenuOpen = false;
	
	const toggleMobileMenu = () => {
		mobileMenuOpen = !mobileMenuOpen;
	};
</script>

<!-- Navigation -->
<nav class="bg-black border-b border-gray-800 sticky top-0 z-50">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex justify-between items-center h-16">
			<div class="flex items-center">
				<div class="text-red-500 font-bold text-xl">
					<span class="text-white">GYMBO</span><span class="text-red-500">.</span>
				</div>
			</div>
			<div class="hidden lg:block">
				<div class="ml-10 flex items-baseline space-x-8">
					<a href="./" class="text-white hover:text-red-500 px-3 py-2 text-sm font-medium transition-colors">HOME</a>
					<a href="#about" class="text-gray-300 hover:text-red-500 px-3 py-2 text-sm font-medium transition-colors">ABOUT US</a>
					<a href="#services" class="text-gray-300 hover:text-red-500 px-3 py-2 text-sm font-medium transition-colors">SERVICES</a>
					<a href="#training" class="text-gray-300 hover:text-red-500 px-3 py-2 text-sm font-medium transition-colors">TRAINING</a>
					<a href="#blog" class="text-gray-300 hover:text-red-500 px-3 py-2 text-sm font-medium transition-colors">BLOG</a>
					<a href="./" class="text-gray-300 hover:text-red-500 px-3 py-2 text-sm font-medium transition-colors">CONTACT</a>
				</div>
			</div>
			<div class="hidden lg:block">
				<button class="bg-red-500 hover:bg-red-600 text-white px-6 py-2 text-sm font-medium transition-all duration-300 transform hover:scale-105">
					GET STARTED
				</button>
			</div>
			<div class="lg:hidden">
				<button on:click={toggleMobileMenu} class="text-white hover:text-red-500 p-2">
					<svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
					</svg>
				</button>
			</div>
		</div>
		
		<!-- Mobile menu -->
		{#if mobileMenuOpen}
			<div class="lg:hidden bg-gray-900 border-t border-gray-800">
				<div class="px-2 pt-2 pb-3 space-y-1">
					<a href="./" class="text-white hover:text-red-500 block px-3 py-2 text-base font-medium">HOME</a>
					<a href="#about" class="text-gray-300 hover:text-red-500 block px-3 py-2 text-base font-medium">ABOUT US</a>
					<a href="#services" class="text-gray-300 hover:text-red-500 block px-3 py-2 text-base font-medium">SERVICES</a>
					<a href="#training" class="text-gray-300 hover:text-red-500 block px-3 py-2 text-base font-medium">TRAINING</a>
					<a href="#blog" class="text-gray-300 hover:text-red-500 block px-3 py-2 text-base font-medium">BLOG</a>
					<a href="./" class="text-gray-300 hover:text-red-500 block px-3 py-2 text-base font-medium">CONTACT</a>
					<button class="bg-red-500 hover:bg-red-600 text-white px-6 py-2 text-sm font-medium transition-colors w-full mt-4">
						GET STARTED
					</button>
				</div>
			</div>
		{/if}
	</div>
</nav>

<!-- Hero Section -->
<section class="bg-black text-white relative overflow-hidden min-h-screen flex items-center">
	<!-- Background with Fighter Image -->
	<div class="absolute inset-0">
		<!-- Fighter silhouette background - positioned on the right side -->
		<div class="absolute right-0 top-0 w-full lg:w-3/5 h-full">
			<!-- Create a realistic fighter silhouette using CSS -->
			<div class="w-full h-full relative">
				<!-- Fighter body silhouette -->
				<div class="absolute lg:right-40 bottom-0 w-full h-full bg-gradient-to-t from-gray-600/30 via-gray-700/20 to-transparent">
					<img src={gymBro} alt="gym bro lifting" class="w-full h-full object-cover">
				</div>
			</div>
		</div>
		<!-- Dark gradient overlay from left -->
		<div class="absolute inset-0 bg-gradient-to-r from-black via-black/95 to-black/30"></div>
		<div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"></div>
	</div>
	
	<!-- Decorative corner elements -->
	<div class="absolute top-8 left-8 w-16 lg:w-20 h-16 lg:h-20 border-4 border-red-500 border-b-transparent border-r-transparent"></div>
	<div class="absolute bottom-8 right-8 w-16 lg:w-20 h-16 lg:h-20 border-4 border-red-500 border-t-transparent border-l-transparent"></div>
	
	<!-- Content -->
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
		<div class="w-full md:w-screen">
			<h1 class="text-4xl sm:text-5xl lg:text-6xl xl:text-7xl font-bold leading-tight mb-6 lg:mb-8">
				THE BEST <span class="text-red-500">BOXING</span><br>
				SCHOOL AND MARTIAL<br>
				ARTS IN THE WORLD
			</h1>
			<p class="text-gray-400 text-lg lg:text-xl max-w-2xl mb-8 lg:mb-12 leading-relaxed">
				Transform your body and mind with our world-class boxing and martial arts training. Join thousands of students who have achieved their fitness goals with our expert instructors.
			</p>
			<button class="bg-red-500 hover:bg-red-600 text-white px-8 lg:px-10 py-4 lg:py-5 text-base lg:text-lg font-medium transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl uppercase tracking-wide">
				GET STARTED
			</button>
		</div>
	</div>
</section>

<!-- Stats Section -->
<section class="bg-gray-900 border-t border-gray-800">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
		<div class="grid grid-cols-2 md:grid-cols-4 gap-8">
			<div class="text-center group">
				<div class="text-4xl lg:text-5xl font-bold text-red-500 transition-all duration-300 group-hover:scale-110">15</div>
				<div class="text-gray-400 text-sm mt-2 font-medium">YEARS OF<br>EXPERIENCE</div>
			</div>
			<div class="text-center group">
				<div class="text-4xl lg:text-5xl font-bold text-red-500 transition-all duration-300 group-hover:scale-110">480</div>
				<div class="text-gray-400 text-sm mt-2 font-medium">MEMBERS<br>JOINED</div>
			</div>
			<div class="text-center group">
				<div class="text-4xl lg:text-5xl font-bold text-red-500 transition-all duration-300 group-hover:scale-110">30</div>
				<div class="text-gray-400 text-sm mt-2 font-medium">EXPERT<br>TRAINERS</div>
			</div>
			<div class="text-center group">
				<div class="text-4xl lg:text-5xl font-bold text-red-500 transition-all duration-300 group-hover:scale-110">360</div>
				<div class="text-gray-400 text-sm mt-2 font-medium">AWARDS<br>WON</div>
			</div>
		</div>
	</div>
</section>

<!-- About Section -->
<section id="about" class="bg-black text-white py-20">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
			<div class="relative group">
				<div class="w-full h-96 lg:h-[500px] bg-gray-800 rounded-lg overflow-hidden relative transition-all duration-500 group-hover:scale-105">
					<div class="w-full h-full bg-gradient-to-br from-gray-700 via-gray-800 to-gray-900 flex items-center justify-center relative">
						<!-- Boxing gloves placeholder -->
						<div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent">
                            <img src={gymBro2} alt="gym bro lifting" class="w-full h-full object-cover">
                        </div>
						<div class="relative z-10 flex space-x-4">
							<div class="w-20 h-20 bg-red-500/30 rounded-full flex items-center justify-center">
								<div class="w-12 h-12 bg-red-500 rounded-full"></div>
							</div>
							<div class="w-20 h-20 bg-red-500/30 rounded-full flex items-center justify-center">
								<div class="w-12 h-12 bg-red-500 rounded-full"></div>
							</div>
						</div>
						<div class="absolute top-4 left-4 w-16 h-16 border-4 border-red-500 border-b-transparent border-r-transparent transition-all duration-500 group-hover:rotate-90"></div>
						<div class="absolute bottom-4 right-4 w-16 h-16 border-4 border-red-500 border-t-transparent border-l-transparent transition-all duration-500 group-hover:-rotate-90"></div>
					</div>
				</div>
			</div>
			<div class="space-y-6">
				<div class="text-red-500 text-sm font-bold tracking-wide uppercase">About Us</div>
				<h2 class="text-4xl lg:text-5xl font-bold leading-tight">
					BEST BOXING SCHOOL AND<br>
					MARTIAL ARTS SINCE <span class="text-red-500">2005</span>
				</h2>
				<p class="text-gray-400 text-lg leading-relaxed">
					At Gymbo, we've been transforming lives through the art of boxing and martial arts for over 18 years. Our world-class facility and expert trainers provide an unmatched training experience that builds strength, discipline, and confidence.
				</p>
				<div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
					<div class="flex items-center space-x-3 group">
						<div class="w-3 h-3 bg-red-500 rounded-full transition-all duration-300 group-hover:w-4 group-hover:h-4"></div>
						<span class="text-white font-medium">Best Training</span>
					</div>
					<div class="flex items-center space-x-3 group">
						<div class="w-3 h-3 bg-red-500 rounded-full transition-all duration-300 group-hover:w-4 group-hover:h-4"></div>
						<span class="text-white font-medium">Best Pricing</span>
					</div>
					<div class="flex items-center space-x-3 group">
						<div class="w-3 h-3 bg-red-500 rounded-full transition-all duration-300 group-hover:w-4 group-hover:h-4"></div>
						<span class="text-white font-medium">Quality Equipment</span>
					</div>
					<div class="flex items-center space-x-3 group">
						<div class="w-3 h-3 bg-red-500 rounded-full transition-all duration-300 group-hover:w-4 group-hover:h-4"></div>
						<span class="text-white font-medium">Best Trainers</span>
					</div>
				</div>
				<button class="bg-red-500 hover:bg-red-600 text-white px-8 py-4 font-medium transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
					GET STARTED
				</button>
			</div>
		</div>
	</div>
</section>

<!-- Services Section -->
<section id="services" class="bg-gray-900 text-white py-20">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<div class="text-red-500 text-sm font-bold tracking-wide uppercase mb-4">Services</div>
			<h2 class="text-4xl lg:text-5xl font-bold">OUR TRAINING PROGRAMS</h2>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<!-- Service 1 -->
			<div class="bg-black p-8 rounded-lg transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="w-16 h-16 bg-gradient-to-br from-red-500 to-red-600 rounded-lg flex items-center justify-center mb-6 transition-all duration-300 group-hover:scale-110">
					<svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
						<path d="M12 2L13.5 8.5L20 7L14.5 12L20 17L13.5 15.5L12 22L10.5 15.5L4 17L9.5 12L4 7L10.5 8.5L12 2Z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold mb-4 group-hover:text-red-500 transition-colors">Personal Training</h3>
				<p class="text-gray-400 mb-6 leading-relaxed">
					One-on-one sessions with our expert trainers to achieve your specific fitness goals with personalized attention and custom workout plans.
				</p>
				<a href="#" class="text-red-500 hover:text-red-400 font-medium transition-colors flex items-center">
					Learn More 
					<svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
					</svg>
				</a>
			</div>
			
			<!-- Service 2 -->
			<div class="bg-black p-8 rounded-lg transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="w-16 h-16 bg-gradient-to-br from-red-500 to-red-600 rounded-lg flex items-center justify-center mb-6 transition-all duration-300 group-hover:scale-110">
					<svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
						<path d="M16 4C16 2.9 15.1 2 14 2H10C8.9 2 8 2.9 8 4H6C4.9 4 4 4.9 4 6V18C4 19.1 4.9 20 6 20H18C19.1 20 20 19.1 20 18V6C20 4.9 19.1 4 18 4H16M10 4H14V6H10V4Z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold mb-4 group-hover:text-red-500 transition-colors">Group Classes</h3>
				<p class="text-gray-400 mb-6 leading-relaxed">
					Join our energetic group sessions and train alongside like-minded individuals in a motivating and supportive environment.
				</p>
				<a href="#" class="text-red-500 hover:text-red-400 font-medium transition-colors flex items-center">
					Learn More 
					<svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
					</svg>
				</a>
			</div>
			
			<!-- Service 3 -->
			<div class="bg-black p-8 rounded-lg transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="w-16 h-16 bg-gradient-to-br from-red-500 to-red-600 rounded-lg flex items-center justify-center mb-6 transition-all duration-300 group-hover:scale-110">
					<svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
						<path d="M12 2C13.1 2 14 2.9 14 4C14 5.1 13.1 6 12 6C10.9 6 10 5.1 10 4C10 2.9 10.9 2 12 2M21 9V7L15 7.5V9C15 10.1 15.9 11 17 11S19 10.1 19 11V9M3 9V7L9 7.5V9C9 10.1 8.1 11 7 11S5 10.1 5 11V9Z"/>
					</svg>
				</div>
				<h3 class="text-xl font-bold mb-4 group-hover:text-red-500 transition-colors">Kickboxing</h3>
				<p class="text-gray-400 mb-6 leading-relaxed">
					High-intensity kickboxing classes that combine cardio, strength training, and martial arts techniques for total body conditioning.
				</p>
				<a href="#" class="text-red-500 hover:text-red-400 font-medium transition-colors flex items-center">
					Learn More 
					<svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
					</svg>
				</a>
			</div>
		</div>
	</div>
</section>

<!-- Training Programs Section -->
<section id="training" class="bg-black text-white py-20">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<div class="text-red-500 text-sm font-medium tracking-wide mb-4">TRAINING</div>
			<h2 class="text-4xl lg:text-5xl font-bold">PREMIUM PACKAGES</h2>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<!-- Basic Package -->
			<div class="bg-gray-900 p-8 rounded-lg">
				<h3 class="text-2xl font-bold mb-2">Premium Packages</h3>
				<div class="text-red-500 text-4xl font-bold mb-6">$89<span class="text-lg text-gray-400">/month</span></div>
				<ul class="space-y-3 mb-8">
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Free Riding</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Unlimited Equipment</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Personal Training</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Weight Lifting</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>No Time Restriction</span>
					</li>
				</ul>
				<button class="w-full bg-red-500 hover:bg-red-600 text-white py-3 font-medium transition-colors">
					GET STARTED
				</button>
			</div>
			
			<!-- Standard Package -->
			<div class="bg-gray-900 p-8 rounded-lg">
				<h3 class="text-2xl font-bold mb-2">Basic Packages</h3>
				<div class="text-red-500 text-4xl font-bold mb-6">$59<span class="text-lg text-gray-400">/month</span></div>
				<ul class="space-y-3 mb-8">
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Free Riding</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Unlimited Equipment</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Personal Training</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Weight Lifting</span>
					</li>
					<li class="flex items-center text-gray-500">
						<span class="text-gray-500 mr-3">✗</span>
						<span>No Time Restriction</span>
					</li>
				</ul>
				<button class="w-full bg-red-500 hover:bg-red-600 text-white py-3 font-medium transition-colors">
					GET STARTED
				</button>
			</div>
			
			<!-- Premium Package -->
			<div class="bg-gray-900 p-8 rounded-lg">
				<h3 class="text-2xl font-bold mb-2">Standard Packages</h3>
				<div class="text-red-500 text-4xl font-bold mb-6">$79<span class="text-lg text-gray-400">/month</span></div>
				<ul class="space-y-3 mb-8">
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Free Riding</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Unlimited Equipment</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Personal Training</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>Weight Lifting</span>
					</li>
					<li class="flex items-center">
						<span class="text-red-500 mr-3">✓</span>
						<span>No Time Restriction</span>
					</li>
				</ul>
				<button class="w-full bg-red-500 hover:bg-red-600 text-white py-3 font-medium transition-colors">
					GET STARTED
				</button>
			</div>
		</div>
	</div>
</section>

<!-- Courses Section -->
<section id="courses" class="bg-gray-900 text-white py-20">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
			<div class="space-y-8">
				<div class="text-red-500 text-sm font-bold tracking-wide uppercase">Courses</div>
				<h2 class="text-4xl lg:text-5xl font-bold leading-tight">
					WE PROVIDE THE <span class="text-red-500">BEST</span><br>
					COURSES FOR OUR MEMBERS
				</h2>
				
				<div class="space-y-6">
					<ProgressBar label="Cardio/HIIT" percentage={80} delay={0} />
					<ProgressBar label="Professional Boxing" percentage={90} delay={200} />
					<ProgressBar label="Body Building" percentage={75} delay={400} />
					<ProgressBar label="Affordable Price" percentage={95} delay={600} />
				</div>
			</div>
			<div class="relative group">
				<div class="w-full h-96 lg:h-[500px] bg-gray-800 rounded-lg overflow-hidden relative transition-all duration-500 group-hover:scale-105">
					<div class="w-full h-full bg-gradient-to-br from-gray-700 via-gray-800 to-gray-900 flex items-center justify-center relative">
						<!-- Training equipment placeholder -->
						<div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent">
                            <img src={gymBro3} alt="gym bro lifting">
                        </div>
						<div class="relative z-10 grid grid-cols-2 gap-4">
							<div class="w-16 h-16 bg-red-500/30 rounded-lg flex items-center justify-center">
								<div class="w-8 h-8 bg-red-500 rounded"></div>
							</div>
							<div class="w-16 h-16 bg-red-500/30 rounded-lg flex items-center justify-center">
								<div class="w-8 h-8 bg-red-500 rounded-full"></div>
							</div>
							<div class="w-16 h-16 bg-red-500/30 rounded-lg flex items-center justify-center">
								<div class="w-8 h-8 bg-red-500 rounded"></div>
							</div>
							<div class="w-16 h-16 bg-red-500/30 rounded-lg flex items-center justify-center">
								<div class="w-8 h-8 bg-red-500 rounded-full"></div>
							</div>
						</div>
					</div>
				</div>
				<div class="absolute -bottom-4 -right-4 bg-red-500 text-white p-6 rounded-lg shadow-2xl transform transition-all duration-500 group-hover:scale-110">
					<div class="text-center">
						<div class="text-3xl font-bold">50</div>
						<div class="text-sm font-medium">Premium Training</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Testimonials Section -->
<section id="testimonials" class="bg-black text-white py-20">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<div class="text-red-500 text-sm font-bold tracking-wide uppercase mb-4">Testimonials</div>
			<h2 class="text-4xl lg:text-5xl font-bold">OUR CLIENTS <span class="text-red-500">REVIEWS</span></h2>
			<p class="text-gray-400 mt-4 max-w-2xl mx-auto">
				Don't just take our word for it. Here's what our members have to say about their transformation journey with Gymbo.
			</p>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<!-- Testimonial 1 -->
			<div class="bg-gray-900 p-8 rounded-lg relative transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-red-600"></div>
				<div class="flex items-center mb-6">
					<div class="w-12 h-12 bg-gradient-to-br from-red-500 to-red-600 rounded-full mr-4 flex items-center justify-center">
						<span class="text-white font-bold text-lg">E</span>
					</div>
					<div>
						<div class="font-bold text-lg">Emily Williams</div>
						<div class="text-gray-400 text-sm">Boxing Student</div>
					</div>
				</div>
				<div class="text-red-500 text-4xl mb-4 leading-none">"</div>
				<p class="text-gray-400 leading-relaxed mb-4">
					"Gymbo has completely transformed my fitness journey. The trainers are incredibly knowledgeable and the community is so supportive. I've never felt stronger!"
				</p>
				<div class="flex text-red-500">
					{#each Array(5) as _}
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
							<path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
						</svg>
					{/each}
				</div>
			</div>
			
			<!-- Testimonial 2 -->
			<div class="bg-gray-900 p-8 rounded-lg relative transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-red-600"></div>
				<div class="flex items-center mb-6">
					<div class="w-12 h-12 bg-gradient-to-br from-red-500 to-red-600 rounded-full mr-4 flex items-center justify-center">
						<span class="text-white font-bold text-lg">D</span>
					</div>
					<div>
						<div class="font-bold text-lg">David Rodriguez</div>
						<div class="text-gray-400 text-sm">Gym Member</div>
					</div>
				</div>
				<div class="text-red-500 text-4xl mb-4 leading-none">"</div>
				<p class="text-gray-400 leading-relaxed mb-4">
					"The equipment is top-notch and the atmosphere is electric. I've been training here for 2 years and it never gets old. Best decision I ever made!"
				</p>
				<div class="flex text-red-500">
					{#each Array(5) as _}
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
							<path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
						</svg>
					{/each}
				</div>
			</div>
			
			<!-- Testimonial 3 -->
			<div class="bg-gray-900 p-8 rounded-lg relative transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-500 to-red-600"></div>
				<div class="flex items-center mb-6">
					<div class="w-12 h-12 bg-gradient-to-br from-red-500 to-red-600 rounded-full mr-4 flex items-center justify-center">
						<span class="text-white font-bold text-lg">M</span>
					</div>
					<div>
						<div class="font-bold text-lg">Maria Garcia</div>
						<div class="text-gray-400 text-sm">Fitness Enthusiast</div>
					</div>
				</div>
				<div class="text-red-500 text-4xl mb-4 leading-none">"</div>
				<p class="text-gray-400 leading-relaxed mb-4">
					"As a beginner, I was nervous about joining a boxing gym. But the staff made me feel welcome from day one. I'm now competing in amateur fights!"
				</p>
				<div class="flex text-red-500">
					{#each Array(5) as _}
						<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
							<path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
						</svg>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Blog Section -->
<section id="blog" class="bg-gray-900 text-white py-20">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="text-center mb-16">
			<div class="text-red-500 text-sm font-bold tracking-wide uppercase mb-4">Blog Post</div>
			<h2 class="text-4xl lg:text-5xl font-bold">LATEST BLOG & <span class="text-red-500">ARTICLES</span></h2>
			<p class="text-gray-400 mt-4 max-w-2xl mx-auto">
				Stay updated with the latest training tips, nutrition advice, and boxing techniques from our expert trainers.
			</p>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<!-- Blog Post 1 -->
			<article class="bg-black rounded-lg overflow-hidden transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="h-48 bg-gray-800 relative overflow-hidden">
					<div class="w-full h-full bg-gradient-to-br from-red-500/20 via-gray-700 to-gray-900 flex items-center justify-center relative">
						<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
						<svg class="w-16 h-16 text-red-500 relative z-10" fill="currentColor" viewBox="0 0 24 24">
							<path d="M12 2L13.5 8.5L20 7L14.5 12L20 17L13.5 15.5L12 22L10.5 15.5L4 17L9.5 12L4 7L10.5 8.5L12 2Z"/>
						</svg>
					</div>
					<div class="absolute top-4 left-4 bg-red-500 text-white px-3 py-1 rounded-full text-xs font-bold">
						BOXING
					</div>
				</div>
				<div class="p-6">
					<div class="text-red-500 text-sm mb-2 font-medium">December 15, 2023</div>
					<h3 class="text-xl font-bold mb-3 group-hover:text-red-500 transition-colors">Which Boxing Event Organized Last Month</h3>
					<p class="text-gray-400 text-sm mb-4 leading-relaxed">
						Discover the highlights from our recent boxing championship event and see our fighters in action.
					</p>
					<a href="#" class="text-red-500 hover:text-red-400 font-medium transition-colors flex items-center">
						Read More 
						<svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
						</svg>
					</a>
				</div>
			</article>
			
			<!-- Blog Post 2 -->
			<article class="bg-black rounded-lg overflow-hidden transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="h-48 bg-gray-800 relative overflow-hidden">
					<div class="w-full h-full bg-gradient-to-br from-red-500/20 via-gray-700 to-gray-900 flex items-center justify-center relative">
						<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
						<svg class="w-16 h-16 text-red-500 relative z-10" fill="currentColor" viewBox="0 0 24 24">
							<path d="M16 4C16 2.9 15.1 2 14 2H10C8.9 2 8 2.9 8 4H6C4.9 4 4 4.9 4 6V18C4 19.1 4.9 20 6 20H18C19.1 20 20 19.1 20 18V6C20 4.9 19.1 4 18 4H16M10 4H14V6H10V4Z"/>
						</svg>
					</div>
					<div class="absolute top-4 left-4 bg-red-500 text-white px-3 py-1 rounded-full text-xs font-bold">
						TRAINING
					</div>
				</div>
				<div class="p-6">
					<div class="text-red-500 text-sm mb-2 font-medium">December 12, 2023</div>
					<h3 class="text-xl font-bold mb-3 group-hover:text-red-500 transition-colors">Martial Boxing Event Organized Last Month</h3>
					<p class="text-gray-400 text-sm mb-4 leading-relaxed">
						Learn about the fundamentals of martial arts and how they integrate with modern boxing techniques.
					</p>
					<a href="#" class="text-red-500 hover:text-red-400 font-medium transition-colors flex items-center">
						Read More 
						<svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
						</svg>
					</a>
				</div>
			</article>
			
			<!-- Blog Post 3 -->
			<article class="bg-black rounded-lg overflow-hidden transition-all duration-300 hover:transform hover:scale-105 hover:shadow-2xl group">
				<div class="h-48 bg-gray-800 relative overflow-hidden">
					<div class="w-full h-full bg-gradient-to-br from-red-500/20 via-gray-700 to-gray-900 flex items-center justify-center relative">
						<div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
						<svg class="w-16 h-16 text-red-500 relative z-10" fill="currentColor" viewBox="0 0 24 24">
							<path d="M12 2C13.1 2 14 2.9 14 4C14 5.1 13.1 6 12 6C10.9 6 10 5.1 10 4C10 2.9 10.9 2 12 2M21 9V7L15 7.5V9C15 10.1 15.9 11 17 11S19 10.1 19 11V9M3 9V7L9 7.5V9C9 10.1 8.1 11 7 11S5 10.1 5 11V9Z"/>
						</svg>
					</div>
					<div class="absolute top-4 left-4 bg-red-500 text-white px-3 py-1 rounded-full text-xs font-bold">
						LIFESTYLE
					</div>
				</div>
				<div class="p-6">
					<div class="text-red-500 text-sm mb-2 font-medium">December 10, 2023</div>
					<h3 class="text-xl font-bold mb-3 group-hover:text-red-500 transition-colors">Learn Martial Arts That Are Best For Learning</h3>
					<p class="text-gray-400 text-sm mb-4 leading-relaxed">
						Explore the various martial arts disciplines and find the perfect style that matches your fitness goals.
					</p>
					<a href="#" class="text-red-500 hover:text-red-400 font-medium transition-colors flex items-center">
						Read More 
						<svg class="w-4 h-4 ml-2 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
						</svg>
					</a>
				</div>
			</article>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="bg-black text-white py-20 relative overflow-hidden">
	<div class="absolute inset-0 bg-gradient-to-r from-red-500/10 via-transparent to-red-500/10"></div>
	<div class="absolute inset-0">
		<div class="w-full h-full bg-gradient-to-br from-gray-900/50 via-black/80 to-gray-900/50"></div>
	</div>
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
		<div class="text-center">
			<h2 class="text-5xl lg:text-6xl font-bold mb-6">
				GET <span class="text-red-500">30%</span> DISCOUNT
			</h2>
			<p class="text-gray-400 mb-8 max-w-2xl mx-auto text-lg leading-relaxed">
				Join Gymbo today and transform your life with our world-class training programs. Limited time offer for new members only.
			</p>
			<div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
				<button class="bg-red-500 hover:bg-red-600 text-white px-10 py-4 font-bold text-lg transition-all duration-300 transform hover:scale-105 shadow-lg hover:shadow-xl">
					JOIN NOW
				</button>
				<button class="border-2 border-red-500 text-red-500 hover:bg-red-500 hover:text-white px-10 py-4 font-bold text-lg transition-all duration-300 transform hover:scale-105">
					LEARN MORE
				</button>
			</div>
		</div>
	</div>
</section>

<!-- Footer -->
<footer class="bg-black text-white border-t border-gray-800">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
		<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
			<!-- Brand Section -->
			<div class="md:col-span-1">
				<div class="text-red-500 font-bold text-2xl mb-6">
					<span class="text-white">GYMBO</span><span class="text-red-500">.</span>
				</div>
				<p class="text-gray-400 mb-6 leading-relaxed">
					Transform your body and mind with our world-class boxing and martial arts training. Join the best gym in the city.
				</p>
				<div class="flex space-x-4">
					<a href="#" class="w-10 h-10 bg-red-500 hover:bg-red-600 rounded-lg flex items-center justify-center transition-all duration-300 transform hover:scale-110">
						<svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 24 24">
							<path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
						</svg>
					</a>
					<a href="#" class="w-10 h-10 bg-red-500 hover:bg-red-600 rounded-lg flex items-center justify-center transition-all duration-300 transform hover:scale-110">
						<svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 24 24">
							<path d="M22.46 6c-.77.35-1.6.58-2.46.69.88-.53 1.56-1.37 1.88-2.38-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29 0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15 0 1.49.75 2.81 1.91 3.56-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07 4.28 4.28 0 0 0 4 2.98 8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21 16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56.84-.6 1.56-1.36 2.14-2.23z"/>
						</svg>
					</a>
					<a href="#" class="w-10 h-10 bg-red-500 hover:bg-red-600 rounded-lg flex items-center justify-center transition-all duration-300 transform hover:scale-110">
						<svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 24 24">
							<path d="M12.017 0C5.396 0 .029 5.367.029 11.987c0 5.079 3.158 9.417 7.618 11.174-.105-.949-.199-2.403.041-3.439.219-.937 1.219-5.175 1.219-5.175s-.31-.62-.31-1.538c0-1.442.833-2.518 1.871-2.518.883 0 1.309.662 1.309 1.455 0 .887-.565 2.212-.857 3.434-.244 1.03.516 1.871 1.532 1.871 1.84 0 3.255-1.943 3.255-4.75 0-2.484-1.786-4.221-4.34-4.221-2.957 0-4.691 2.218-4.691 4.51 0 .893.344 1.85.772 2.372.085.103.097.194.072.299-.079.33-.254 1.037-.289 1.183-.045.186-.145.226-.334.137-1.249-.581-2.03-2.407-2.03-3.874 0-3.154 2.292-6.052 6.608-6.052 3.469 0 6.165 2.473 6.165 5.776 0 3.447-2.173 6.22-5.19 6.22-1.013 0-1.968-.527-2.292-1.155l-.623 2.378c-.226.869-.835 1.958-1.244 2.621.937.29 1.931.446 2.962.446 6.624 0 11.99-5.367 11.99-11.987C24.007 5.367 18.641.001 12.017.001z"/>
						</svg>
					</a>
					<a href="#" class="w-10 h-10 bg-red-500 hover:bg-red-600 rounded-lg flex items-center justify-center transition-all duration-300 transform hover:scale-110">
						<svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 24 24">
							<path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
						</svg>
					</a>
				</div>
			</div>
			
			<!-- Quick Links -->
			<div>
				<h3 class="font-bold mb-6 text-lg">Quick Links</h3>
				<ul class="space-y-3">
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">About Us</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Our Services</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Training Programs</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Gallery</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Contact Us</a></li>
				</ul>
			</div>
			
			<!-- Services -->
			<div>
				<h3 class="font-bold mb-6 text-lg">Training Services</h3>
				<ul class="space-y-3">
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Personal Training</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Group Classes</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Kickboxing</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Professional Boxing</a></li>
					<li><a href="#" class="text-gray-400 hover:text-red-500 transition-colors">Cardio/HIIT</a></li>
				</ul>
			</div>
			
			<!-- Contact Info -->
			<div>
				<h3 class="font-bold mb-6 text-lg">Get In Touch</h3>
				<div class="space-y-4">
					<div class="flex items-start space-x-3">
						<div class="w-5 h-5 text-red-500 mt-1">
							<svg fill="currentColor" viewBox="0 0 24 24">
								<path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
							</svg>
						</div>
						<p class="text-gray-400">123 Gym Street, Fitness City, FC 12345</p>
					</div>
					<div class="flex items-center space-x-3">
						<div class="w-5 h-5 text-red-500">
							<svg fill="currentColor" viewBox="0 0 24 24">
								<path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/>
							</svg>
						</div>
						<p class="text-gray-400">+1 (555) 123-4567</p>
					</div>
					<div class="flex items-center space-x-3">
						<div class="w-5 h-5 text-red-500">
							<svg fill="currentColor" viewBox="0 0 24 24">
								<path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
							</svg>
						</div>
						<p class="text-gray-400">info@gymbo.com</p>
					</div>
					<div class="flex items-center space-x-3">
						<div class="w-5 h-5 text-red-500">
							<svg fill="currentColor" viewBox="0 0 24 24">
								<path d="M11.99 2C6.47 2 2 6.48 2 12s4.47 10 9.99 10C17.52 22 22 17.52 22 12S17.52 2 11.99 2zM12 20c-4.42 0-8-3.58-8-8s3.58-8 8-8 8 3.58 8 8-3.58 8-8 8z"/>
								<path d="M12.5 7H11v6l5.25 3.15.75-1.23-4.5-2.67z"/>
							</svg>
						</div>
						<p class="text-gray-400">Mon-Fri: 6AM-10PM<br>Sat-Sun: 8AM-8PM</p>
					</div>
				</div>
			</div>
		</div>
		
		<div class="border-t border-gray-800 mt-12 pt-8">
			<div class="flex flex-col md:flex-row justify-between items-center">
				<p class="text-gray-400 text-center md:text-left">
					&copy; 2023 Gymbo. All rights reserved. | Privacy Policy | Terms of Service
				</p>
				<p class="text-gray-400 text-center md:text-right mt-4 md:mt-0">
					Designed by <a href="https://giddelwilson.vercel.app" class="text-red-500 hover:text-red-400 transition-colors">Giddel Wilson</a>
				</p>
			</div>
		</div>
	</div>
</footer>
