<template>
	<div class="author">

		<g-image alt="Author image" class="author__image" src="~/assets/images/Picture1.jpg" width="180" height="180" blur="5" />

		<h1 v-if="showTitle" class="author__site-title">
			SEOULCHA RATMUMAD
		</h1>

		<p class="author__intro">
			Studying in the 4th year of Computer Engineering, Faculty of Engineering, Prince of Songkla University.
		</p>

		<p class="author__links">
			<a href="https://web.facebook.com/SeoulSR/">Follow on Facebook</a>
			<a href="https://github.com/6110110108">GitHub</a>
			
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author__site-title {
	text-decoration: underline;
}
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding: calc(var(--space) / 2) 0;

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		font-size: 1.5em;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>
