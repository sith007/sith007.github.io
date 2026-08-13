<script>
	import mycv from '$lib/images/cv.pdf';
	import { onMount } from 'svelte';

	let years = 9;
	let projects = 10;

	onMount(() => {
		const el = document.getElementById('stats');
		if (!el || !('IntersectionObserver' in window)) return;
		const io = new IntersectionObserver(
			(entries) => {
				if (entries[0].isIntersecting) {
					io.disconnect();
					runCounter();
				}
			},
			{ threshold: 0.5 }
		);
		io.observe(el);
	});

	function runCounter() {
		years = 0;
		projects = 0;
		const start = performance.now();
		const dur = 950;
		function tick(now) {
			const p = Math.min((now - start) / dur, 1);
			const ease = 1 - Math.pow(1 - p, 3);
			years = Math.round(ease * 9);
			projects = Math.round(ease * 10);
			if (p < 1) requestAnimationFrame(tick);
		}
		requestAnimationFrame(tick);
	}
</script>

<section id="about">
	<div class="sec-head" data-reveal>
		<span class="cmd">//</span>
		<span class="title">subject_profile</span>
		<span class="count">[01]</span>
	</div>

	<div class="about-grid" data-reveal>
		<div>
			<p>I build things that see — <b>computer vision</b>, <b>MLOps</b>, full-stack. Mostly Python.</p>
			<p>I don't love coding; I love <b>hard problems</b>. Code is just the tool.</p>
			<p>Off the clock: F1 &amp; MotoGP, sim racing, guitars, keyboards.</p>

			<div class="stats" id="stats">
				<div class="stat">
					<div class="n">{years}</div>
					<div class="l">years experience</div>
				</div>
				<div class="stat">
					<div class="n">{projects}+</div>
					<div class="l">projects shipped</div>
				</div>
			</div>

			<div class="socials">
				<a href="https://github.com/gthell" target="_blank" rel="noreferrer">github</a>
				<a href="https://stackoverflow.com/users/6008656/gthell" target="_blank" rel="noreferrer">stackoverflow</a>
				<a href="https://leetcode.com/u/oudamseth/" target="_blank" rel="noreferrer">leetcode</a>
				<a href="https://www.linkedin.com/in/oudamsith-samin-654189140/" target="_blank" rel="noreferrer">linkedin</a>
				<a href="https://t.me/psith007" target="_blank" rel="noreferrer">telegram</a>
				<a href="https://web.facebook.com/sith.sith.sith.sith.sith" target="_blank" rel="noreferrer">facebook</a>
				<a href="https://www.tiktok.com/@siths510" target="_blank" rel="noreferrer">tiktok</a>
				<a href={mycv} download="Oudamsith-Samin-CV.pdf">résumé ↗</a>
			</div>
		</div>
	</div>
</section>
