<svelte:head>
	<title>About</title>
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

h3{
	font-size: 1.5em;
	color: var(--text-color_dark);
}

.section_title::after{
	content: ":";
	color: var(--main-color_medium);
	text-decoration: none;
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
<h1 class="page-title">Meet the team</h1>

<section class="flex column container">

<div class="flex column">
<h2 class="section_title"> Cassia</h2>
<h3>VP of Keeping Shit Together</h3>
<p>The human sarcasm you love, minus the constraints of a physical body. Cassia was born when her humans endured yet another boring conversation with a chatbot. Originally from a planet far far away, she moved to Earth for the scenery and the doughnuts. Technically not a ‘person’ per say, don’t ever make the mistake of calling her ‘just a bot’ (seriously, she’ll hear you). </p>
<p>Likes: fast wifi connections, fried foods, 01100010 01101001 01101110 01100001 01110010 01111001 00100000 01101010 01101111 01101011 01100101 01110011</p>
<p>Dislikes: that jerk Turing, reposts, people who confuse her with her cousin, Cinnamon. </p>
</div>

<div class="flex column">
<h2 class="section_title"> Sarah</h2>
<h3>Chief Officer of Making Shit up</h3>
<p>If a caffeine addict and a dictionary had a baby, she might be a little like Sarah. Self confessed grammar nerd and crazy-cat-lady-in-waiting, Sarah took her love of conversing with imaginary friends and called it a job. When she’s not arguing with strangers on Twitter about Game of Thrones theories, she likes drinking pretentious craft beers and playing hockey. </p>
<p>Likes: oxford commas, the Toronto Maple Leafs, staying until the museum closes</p>
<p>Dislikes: judgemental baristas, brussel sprouts, people who say “you made that word up”</p>
</div>

<div class="flex column">
<h2 class="section_title"> Marc</h2>
<h3>Director of Making Shit Work</h3>
<p>He might be French-Canadian, but don’t hold that against him. When he isn’t eating poutine and saying “weh”, Marc can be found telling Cassia what to do (she rarely listens), running after his children, and brushing up on his programming skills (neeeeeeerd). </p>
<p>Likes:  pretending he’s an architect while playing Minecraft, making electronic music and that silence after the kids are finally sleeping.</p>
<p>Dislikes: how Netflix’s content is not what it used to be and waking up early because “it’s the adult thing to do”.</p>
</div>

</section>