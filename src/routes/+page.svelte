

<svelte:head>
	<title>Recipe App</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<script>
	
	import { recipes } from './data.js';
	
	</script>
	
	<header class="text-gray-400 bg-gray-900 body-font">
		<div class="container mx-auto mt-10 flex flex-wrap p-5 flex-col md:flex-row items-left">
		  <a href="/" class="flex title-font font-medium items-center text-white mb-4 md:mb-0">
			
			<span class="ml-1 text-2xl">Recipe App</span>
		  </a>
		  <nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
			
		  </nav>
		  
		</div>
	  </header>
	
	  <section class="text-gray-400 bg-gray-900 body-font">
		<div class="container px-5 py-16 mx-auto">
	
		  <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4">
	
			{#each recipes as recipe}
			<div class="p-4 md:w-1/3 sm:mb-0 mb-6">
				<div class="rounded-lg h-64 overflow-hidden">
				<img alt="content" class="object-cover object-center h-full w-full" src="{recipe.image}">
				</div>
				<h2 class="text-xl font-medium title-font text-white mt-5">{recipe.name}</h2>
				<p class="text-base leading-relaxed mt-2">{recipe.tagline}</p>
				<a href="/{recipe.id}" class="text-indigo-400 inline-flex items-center mt-3">View Recipe
				<svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-2" viewBox="0 0 24 24">
					<path d="M5 12h14M12 5l7 7-7 7"></path>
				</svg>
				</a>
			</div>   
			{/each}
	
	
		  </div>
		</div>
	  </section>  
