<script>
	import Summary from '$lib/components/index/Summary.svelte';
	import AboutMe from '$lib/components/index/AboutMe.svelte';
	import Project from '$lib/components/index/Project.svelte';
	import Skills from '$lib/components/index/Skills.svelte';
	import WorkExperience from '$lib/components/index/WorkExperience.svelte';
	import Hobbies from '$lib/components/index/Hobbies.svelte';
	import Contact from '$lib/components/index/Contact.svelte';
</script>

<svelte:head>
	<title>Oudamsith Samin — CV · MLOps · Full-Stack</title>
	<meta name="description" content="Computer vision & MLOps engineer. I build things that see." />
</svelte:head>

<Summary />
<AboutMe />
<Project />
<Skills />
<WorkExperience />
<Hobbies />
<Contact />
