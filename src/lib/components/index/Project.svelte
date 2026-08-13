<script>
	import driverlicense from '$lib/images/myworks/driver license detection.png';
	import parking from '$lib/images/myworks/parking_iot.gif';
	import traffic from '$lib/images/myworks/traffic_violation_simulation.gif';
	import system from '$lib/images/myworks/system-diagram.jpg';
	import hullpoint from '$lib/images/myworks/hull point on card3 mod.png';

	const featured = {
		title: 'Document Intelligence',
		desc: 'Extracts text and layout from national IDs, driver\'s licenses, and vaccination cards — the KYC pipeline that runs under the hood of everything I do with OCR.',
		type: 'document.ocr',
		tech: 'OpenCV',
		conf: '99.1%',
		image: driverlicense
	};

	const works = [
		{
			title: 'IoT Parking',
			desc: 'Camera-based occupancy for Sorya and Ratana Plaza malls, plus a mobile portal for customers.',
			type: 'iot.vision',
			tech: 'OpenCV',
			image: parking
		},
		{
			title: 'Traffic Vision',
			desc: 'Speed and violation detection on a live feed, buffered through FFMPEG, simulated end-to-end in Unity.',
			type: 'speed.detection',
			tech: 'FFMPEG',
			image: traffic
		},
		{
			title: 'Payment Microservices',
			desc: 'Split a payment system into services; tightened security and cut operating cost.',
			type: 'system.design',
			tech: 'payments',
			image: system
		},
		{
			title: 'Custom Object Detection',
			desc: 'Hull-point detection on cards, trained for a specific client workflow.',
			type: 'object.detection',
			tech: 'OpenCV',
			image: hullpoint
		}
	];
</script>

<section id="projects">
	<div class="sec-head" data-reveal>
		<span class="cmd">//</span>
		<span class="title">objects_detected</span>
		<span class="count">[05]</span>
	</div>

	<article class="featured" data-reveal>
		<div class="f-media">
			<span class="cb"><i class="c-tl"></i><i class="c-tr"></i><i class="c-bl"></i><i class="c-br"></i></span>
			<span class="cls">{featured.conf}</span>
			<img src={featured.image} alt={featured.title} />
		</div>
		<div class="f-body">
			<span class="f-tag">featured · {featured.tech}</span>
			<h3>{featured.title}</h3>
			<p class="desc">{featured.desc}</p>
			<div class="meta"><span class="type">{featured.type}</span> · <span class="tech">{featured.tech}</span></div>
		</div>
	</article>

	<div class="cards">
		{#each works as w (w.title)}
			<div class="card" data-reveal>
				<div class="media"><img src={w.image} alt={w.title} /></div>
				<div class="body">
					<h3>{w.title}</h3>
					<p class="desc">{w.desc}</p>
					<div class="meta"><span class="type">{w.type}</span> · <span class="tech">{w.tech}</span></div>
				</div>
			</div>
		{/each}
	</div>
</section>
