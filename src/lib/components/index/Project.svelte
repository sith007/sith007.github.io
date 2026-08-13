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
			conf: '99.1%',
			image: driverlicense
		},
		{
			title: 'IoT Parking',
			desc: 'Camera-based occupancy for Sorya and Ratana Plaza malls, plus a mobile portal for customers.',
			type: 'iot.vision',
			tech: 'OpenCV',
			tick: 'IOT',
			conf: '97.8%',
			image: parking
		},
		{
			title: 'Traffic Vision',
			desc: 'Speed and violation detection on a live feed, buffered through FFMPEG, simulated end-to-end in Unity.',
			type: 'speed.detection',
			tech: 'FFMPEG',
			tick: 'TRAFFIC',
			conf: '96.4%',
			image: traffic
		},
		{
			title: 'Payment Microservices',
			desc: 'Split a payment system into services; tightened security and cut operating cost.',
			type: 'system.design',
			tech: 'payments',
			tick: 'SYS',
			conf: '95.9%',
			image: system
		},
		{
			title: 'Custom Object Detection',
			desc: 'Hull-point detection on cards, trained for a specific client workflow.',
			type: 'object.detection',
			tech: 'OpenCV',
			tick: 'CV',
			conf: '98.7%',
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
				<div class="media">
					<span class="cb"><i class="c-tl"></i><i class="c-tr"></i><i class="c-bl"></i><i class="c-br"></i></span>
					<span class="cls">{w.conf}</span>
					<span class="scanbar"></span>
					<img src={w.image} alt={w.title} />
				</div>
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
