<script>
	import skills from '$lib/Skills';
</script>

<svelte:head>
	<title>Jani Bangiev — About</title>
</svelte:head>

<div class="container">
	<main>
		<h1>About</h1>
		<p>
			I'm a software developer who loves to turn ideas into real-world applications using code. I've been coding since I was a kid and I'm always looking for new challenges and ways to learn more. I'm currently working as a software developer at ISL Online and I also do some freelance work on the side. I'm good at using TypeScript, node.js, and Svelte, but I'm also always up for trying new things. I'm passionate about creating user-friendly, high-performance web apps that people will actually want to use.
		</p>
		<p>If you have a cool web development project in mind, let me know! I'd love to help you make it happen.</p>
		<h2>Skills</h2>
		{#each Object.entries(skills) as [section, technologies]}
			<ul>
				<li>
					<h4>
						{section}:
					</h4>
					<div class="list">
						{#each technologies as technology}
							<div>
								{technology}
							</div>
						{/each}
					</div>
				</li>
			</ul>
		{/each}
	</main>
</div>

<style>
	.container {
		max-width: 900px;
		padding: 0;
		display: flex;
		justify-content: center;
	}

	main {
		max-width: 100%;
		min-height: 500px;
		text-align: left;
		margin: 0 auto;
		box-sizing: border-box;
	}

	h1 {
		font-weight: 700;
		margin: 0 0 50px 0;
		font-size: 36px;
		text-align: start;
	}

	h2 {
		margin-top: 50px;
	}

	.list {
		display: flex;
		flex-direction: column;
		gap: 30px;
	}

	@media (min-width: 900px) {
		.list {
			flex-direction: row;
		}
		main > h1 {
			font-size: 48px;
		}
	}
</style>
