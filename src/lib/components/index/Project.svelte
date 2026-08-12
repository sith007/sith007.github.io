<script>
	import driverlicense from '$lib/images/myworks/driver license detection.png';
	import parking from '$lib/images/myworks/parking_iot.gif';
	import traffic from '$lib/images/myworks/traffic_violation_simulation.gif';
	import system from '$lib/images/myworks/system-diagram.jpg';
	import hullpoint from '$lib/images/myworks/hull point on card3 mod.png';

	const works = [
		{
			title: 'Document Intelligence',
			desc: 'Extracts text and layout from national IDs, driver\'s licenses, vaccination cards — the KYC pipeline under the hood.',
			type: 'document.ocr',
			tech: 'OpenCV',
			tick: 'KYC',
			image: driverlicense
		},
		{
			title: 'IoT Parking',
			desc: 'Camera-based occupancy for Sorya and Ratana Plaza malls, plus a mobile portal for customers.',
			type: 'iot.vision',
			tech: 'OpenCV',
			tick: 'IOT',
			image: parking
		},
		{
			title: 'Traffic Vision',
			desc: 'Speed and violation detection on a live feed, buffered through FFMPEG, simulated end-to-end in Unity.',
			type: 'speed.detection',
			tech: 'FFMPEG',
			tick: 'TRAFFIC',
			image: traffic
		},
		{
			title: 'Payment Microservices',
			desc: 'Split a payment system into services; tightened security and cut operating cost.',
			type: 'system.design',
			tech: 'payments',
			tick: 'SYS',
			image: system
		},
		{
			title: 'Custom Object Detection',
			desc: 'Hull-point detection on cards, trained for a specific client workflow.',
			type: 'object.detection',
			tech: 'OpenCV',
			tick: 'CV',
			image: hullpoint
		}
	];
</script>

<section id="projects">
	<div class="sec-head">
		<span class="cmd">//</span>
		<span class="title">objects_detected</span>
		<span class="count">[05]</span>
	</div>

	<div class="cards">
		{#each works as w (w.title)}
			<div class="card">
				<div class="media"><img src={w.image} alt={w.title} /></div>
				<div class="body">
					<h3>{w.title}</h3>
					<p class="desc">{w.desc}</p>
					<div class="meta"><span class="type">{w.type}</span> · <span class="tech">{w.tech}</span></div>
				</div>
				<span class="tick">{w.tick}</span>
			</div>
		{/each}
	</div>
</section>
