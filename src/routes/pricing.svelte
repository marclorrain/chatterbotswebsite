<svelte:head>
	<title>Pricing</title>
</svelte:head>

<style>
.flex{
	display: flex;
	justify-content: space-evenly;
	align-content: space-around;
}
.row{
	flex-direction: row;
}
.column{
	flex-direction: column;
	justify-content: space-evenly;
}

.container{
	padding: 5% 30% 10% 30%;
	line-height: 1.5em;
}

.container p{
	font-size: 1.25em;
}

.page-title{
	font-size: 4em;
	margin: 1em 0 0 2em;
}

@media only screen and (max-width: 441px){
	.container{
	padding: 10% 5%;
    line-height: 1.5em;
}
    .section_title{
		font-size: 2.35em;
		line-height: 2em;
	}
	.page-title{
	font-size: 4em;
	margin: 0 0.5em;
}
}

</style>
<h1 class="page-title">Pricing</h1>
<section class="flex row container">
<div class="flex column">
<h2 class="section_title"> Time for "the talk"</h2>
<p>We don't like having this conversation either, it's awkward, it sucks but it is very much necessary as 2/3 of our team members are but humble "meat bags" (as Cassia likes to remind us).</p>
<p>We need to talk about how much it costs for us to give birth to your new team mate! We typically charge about $75USD/hour for a minimum of 4 hours per job. That's about $300USD per outing.</p>
<p>Now we understand all projects do not have the same requirements and we are willing to be flexible depending on what the project needs!</p>
<p>If you'd like more details, feel free to check in with Cassia and tell her the projects requirement and she'll be happy to give you a quote!</p>
</div>
</section>