<script>
	import '../app.css';
</script>

<div class="grid-bg"></div>

<div class="hud">
	<span class="h-tl"></span>
	<span class="h-tr"></span>
	<span class="h-bl"></span>
	<span class="h-br"></span>
</div>
<span class="global-scan"></span>

<nav>
	<div class="brand"><b>sith</b>@cv<span class="cursor">█</span></div>
	<div class="right">
		<div class="links">
			<a href="#about"><span>//</span>about</a>
			<a href="#projects"><span>//</span>work</a>
			<a href="#skills"><span>//</span>skills</a>
			<a href="#experience"><span>//</span>log</a>
			<a href="#hobbies"><span>//</span>other</a>
			<a href="#contact"><span>//</span>ping</a>
		</div>
		<div class="rec"><span class="dot"></span><span class="rec-txt">REC</span></div>
	</div>
</nav>

<main>
	<slot />
</main>

<footer><b>sith</b>@cv ~ <span style="color: var(--cyan)">$</span> made with sveltekit + a lot of object detection</footer>
