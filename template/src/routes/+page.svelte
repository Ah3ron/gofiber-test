<script>
	// You can add your own details or logic here
	const name = "John Doe";
	const description = "Web Developer | Designer | Creative Thinker";
	const links = [
	  { label: "About", href: "#about" },
	  { label: "Projects", href: "#projects" },
	  { label: "Contact", href: "#contact" },
	];
  </script>
  
  <main class="min-h-screen bg-base-200 flex flex-col items-center justify-center text-center">
	<div class="container mx-auto px-4">
	  <!-- Header -->
	  <header class="mb-8">
		<h1 class="text-5xl font-bold text-primary">{name}</h1>
		<p class="mt-4 text-lg text-content">{description}</p>
	  </header>
  
	  <!-- Navigation Links -->
	  <nav class="mb-8">
		<ul class="flex justify-center gap-4">
		  {#each links as { label, href }}
			<li>
			  <a
				href="{href}"
				class="btn btn-outline btn-primary transition-all duration-300 hover:scale-105"
				>{label}</a
			  >
			</li>
		  {/each}
		</ul>
	  </nav>
  
	  <!-- Call-to Action Section -->
	  <section class="mt-8">
		<p class="mb-4 text-md text-content">Check out my latest projects and see what I’m working on!</p>
		<a href="#projects" class="btn btn-wide btn-secondary">
		  Explore Projects
		</a>
	  </section>
  
	  <!-- Footer -->
	  <footer class="mt-16">
		<p class="text-sm text-neutral-content">
		  &copy; {new Date().getFullYear()} {name}. All rights reserved.
		</p>
	  </footer>
	</div>
  </main>
  
  <style>
	/* Additional styling if needed */
	main {
	  scroll-behavior: smooth;
	}
  </style>
  