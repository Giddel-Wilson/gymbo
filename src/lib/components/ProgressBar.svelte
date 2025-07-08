<script lang="ts">
	import { onMount } from 'svelte';
	
	export let label: string;
	export let percentage: number;
	export let delay: number = 0;
	
	let progressElement: HTMLElement;
	let isVisible = false;
	let animatedPercentage = 0;
	
	onMount(() => {
		const observer = new IntersectionObserver((entries) => {
			if (entries[0].isIntersecting && !isVisible) {
				isVisible = true;
				setTimeout(() => {
					animateProgress();
				}, delay);
			}
		});
		
		if (progressElement) {
			observer.observe(progressElement);
		}
		
		return () => observer.disconnect();
	});
	
	function animateProgress() {
		let current = 0;
		const increment = percentage / 50; // 50 frames for smooth animation
		
		const animate = () => {
			current += increment;
			if (current >= percentage) {
				animatedPercentage = percentage;
			} else {
				animatedPercentage = current;
				requestAnimationFrame(animate);
			}
		};
		
		animate();
	}
</script>

<div bind:this={progressElement} class="space-y-3">
	<div class="flex justify-between items-center">
		<span class="text-white font-medium">{label}</span>
		<span class="text-red-500 font-bold">{Math.round(animatedPercentage)}%</span>
	</div>
	<div class="w-full bg-gray-700 rounded-full h-3 overflow-hidden">
		<div 
			class="bg-gradient-to-r from-red-500 to-red-600 h-3 rounded-full transition-all duration-1000 ease-out shadow-lg"
			style="width: {animatedPercentage}%"
		></div>
	</div>
</div>
