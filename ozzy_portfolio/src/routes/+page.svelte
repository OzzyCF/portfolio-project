<script>
	import { Video } from 'flowbite-svelte';
	// If you plan to fetch repositories from GitHub API, you would include the fetching logic here
	// For the sake of this example, I'll add mock data for tech stack and experience
	const techStack = [
		'HTML',
		'CSS',
		'JavaScript',
		'React',
		'React Native',
		'Svelte',
		'Node.js',
		'Express.js'
	];
	const experiences = [
		{ year: '2023', company: 'Northcoders', role: 'Frontend Developer Bootcamp Graduate' }
		// ... other experiences
	];
	// Add the URL to your CV here
	const cvDownloadUrl = '/oswaldo_colon_freites_cv.pdf';
</script>

<div class="px-4 sm:px-6 lg:px-8 py-12 mx-auto max-w-7xl">
	<div class="bio-section">
		<div class=" w-full h-full relative flex flex-col items-center p-8 rounded-lg shadow">
			<Video
				src="/bg-video-bio.mp4"
				autoplay
				loop
				muted
				playsinline
				class="absolute w-full h-full object-cover rounded-lg shadow"
				trackSrc="bg-video-bio.mp4"
			/>

			<div class="relative z-10">
				<img
					src="/Ozzy-transparent-bg.png"
					alt="Oswaldo Colon Freites"
					class="rounded-full bg-gray-200 object-cover w-52 h-52 mb-4 shadow mt-4"
				/>
				<p class="text-center text-white font-roboto w-full drop-shadow">
					Hello! I'm Oswaldo Colon Freites, a Frontend Developer. I specialize in Design and
					implementation of web applications. I love to create and innovate with new technologies.
				</p>
			</div>
		</div>
	</div>

	<div class="tech-stack">
		<div class="mt-8 mb-6">
			<h2 class="text-xl font-semibold font-roboto text-gray-800 mb-4">
				Technologies I work with:
			</h2>
			<div class="flex justify-center flex-wrap gap-2">
				{#each techStack as tech}
					<span class="px-3 py-1 bg-blue-200 text-blue-800 rounded-full font-roboto">{tech}</span>
				{/each}
			</div>
		</div>
	</div>

	<div class="experience">
		<div class="my-6">
			<h2 class="text-xl font-semibold font-roboto text-gray-800 mb-4">Experience:</h2>
			{#each experiences as experience}
				<div class="mb-3 font-roboto text-gray-600">
					<strong class="text-gray-800">{experience.year}</strong>: {experience.role} at {experience.company}
				</div>
			{/each}
		</div>
	</div>

	<!-- Assuming you are pulling repositories from GitHub or another source -->
	<ul class="list-none mt-6 mb-8">
		{#each ['Repo 1', 'Repo 2', 'Repo 3'] as repo}
			<li class="mb-2"><a href="notLinked" class="text-blue-600 hover:text-blue-800">{repo}</a></li>
		{/each}
	</ul>

	<a
		href={cvDownloadUrl}
		download="Oswaldo-Colon-Freites-CV.pdf"
		class="mt-5 inline-block px-4 py-2 bg-green-500 text-white rounded hover:bg-green-600 transition-colors duration-300 ease-in-out"
		>Download my CV</a
	>
</div>

<style>
	/* Add your CSS here. For example: */
	.bio-section {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 20px;
	}

	.tech-stack {
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
		gap: 10px;
	}

	.experience {
		margin-top: 20px;
	}

	/* ...other styles */
</style>
