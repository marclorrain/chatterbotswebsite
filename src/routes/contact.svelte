<svelte:head>
	<title>Contact</title>
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
<h1 class="page-title">Contact Us</h1>
<section class="flex row container">
<div class="flex column">
<h2 class="section_title"> Need to reach us?</h2>
<p>Let’s stay in touch! Leave your info with Cassia, and our people will talk to your people. We promise we’ll never ghost you. </p>

</section>