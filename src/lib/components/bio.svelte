<script>
	import me from '$lib/assets/avatar.webp';
</script>

<div class="card">
	<div class="me">
		<img src={me} alt="me smiling" />
		<p>@Jorge</p>
	</div>
	<p>
		I’m a hands-on builder who loves blending technical skill with creative curiosity. I tinker with
		self hosting servers, web development, make music, and even sew when the mood strikes.
		Originally from Miami, I joined the Navy in 2004, traveled the world as a cook — now I live in
		San Diego, cooking up cleaner code instead of chow. If you’ve made it this far, feel free to say
		hi: <a href="mailto:hello@codingMustache.dev">hello@codingMustache.dev</a>.
	</p>
</div>

<style>
	.card {
		margin: 10% auto;
		max-width: 500px;
		border-radius: 3px;
		padding: 10px;
		background-color: var(--sec);
		display: flex;
		flex-direction: column;
		gap: 10px;
		padding: 50px 100px;
		p {
			line-height: 1.5;
		}
		.me {
			display: flex;
			align-items: end;
			justify-content: start;
			gap: 5px;
			p {
				font-weight: 600;
			}
			img {
				height: 50px;
				width: 50px;
				border-radius: 100%;
				box-shadow: 0px 0px 10px black;
			}
		}
	}
</style>
