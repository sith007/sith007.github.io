<script>
	import track1 from '$lib/images/track1.jpg';
	import electric1 from '$lib/images/electric1.jpg';
	import keeb1 from '$lib/images/keeb1.jpg';
	import run1 from '$lib/images/run1.jpg';
	import sim1 from '$lib/images/sim1.jpg';

	const hobbies = [
		{ label: 'MOTORSPORT', img: track1 },
		{ label: 'DIY / 3D PRINTING', img: electric1 },
		{ label: 'MECHANICAL KEYBOARDS', img: keeb1 },
		{ label: '5K RUNNING', img: run1 },
		{ label: 'SIM RACING', img: sim1 }
	];
</script>

<section id="hobbies">
	<div class="sec-head">
		<span class="cmd">//</span>
		<span class="title">other_detections</span>
		<span class="count">[05]</span>
	</div>

	<div class="hobbies">
		{#each hobbies as h (h.label)}
			<div class="hobby">
				<div class="label">{h.label}</div>
				<div class="imgs">
					<span class="cb"><i class="c-tl"></i><i class="c-tr"></i><i class="c-bl"></i><i class="c-br"></i></span>
					<img src={h.img} alt={h.label} />
				</div>
			</div>
		{/each}
	</div>
</section>
