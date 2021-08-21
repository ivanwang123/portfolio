<script lang="ts">
	import About from '$lib/About.svelte';
</script>

<svelte:head>
	<title>About | Ivan Wang</title>
</svelte:head>

<div class="max-w-3xl p-4 pb-8">
	<img src="res/profile-pic.jpg" alt="profile pic" width={200} height={200} />
	<About
		title="Hello"
		content="My name is Ivan. I'm 18 years old and grew up in New Jersey. I do full stack development."
	/>
	<About
		title="Background"
		content="I started coding back in 7th grade with the dream of making my own video games. But over
    time, I found my interests lie in web development and have been learning it ever since. I
    enjoy learning new technologies and understanding the full process, from the user interface
    all the way to the database and everything in between. You can check out what I'm working on
    right now through my github."
	/>
	<About
		title="Experience"
		content="I started coding back in 7th grade with the dream of making my own video games. But over
    time, I found my interests lie in web development and have been learning it ever since. I
    enjoy learning new technologies and understanding the full process, from the user interface
    all the way to the database and everything in between. You can check out what I'm working on
    right now through my github."
	/>
</div>
