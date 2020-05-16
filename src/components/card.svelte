<script>

let cards = [
    {title: 'card 1', text: 'lorem ispum lorem blablablablablabla', img: '../favicon-alt.svg'},
    {title: 'card 2', text: 'lorem ispum lorem blablablablablabla', img: '../favicon-alt.svg'},
    {title: 'card 3', text: 'lorem ispum lorem blablablablablabla', img: '../favicon-alt.svg'}
];
</script>

<div class="flex-grid-wrap">
{#each cards as card}
<div class="flex-grid">

<div class="card">
<figure class="card-media">
<img src={card.img} alt="alt-text bozo" width="100%"/>
</figure>
<div class="card-title">
<h2>{card.title}</h2>
</div>
<div class="card-content">
    <p>{card.text}</p>
</div>

</div>

</div>
{/each}
</div>

<style>

@media only screen and (max-width: 441px){
    .card{
        position: relative;
        top: 0;
        left: 0;
        max-width: 100% ;
    }
}

h2{
    font-size: 2em;
    text-decoration: underline var(--main-color_medium);
    text-transform: capitalize;
}

.card{
    display: flex;
    flex-direction: column;
    justify-content:space-evenly;
    align-items: baseline;
    width: 100%;
    height: 50vh;
}

.card-media{
    width: 15%;
    height: auto;
}

</style>

<!-- testing section

<script>
export let cardTitle;
export let cardText;
export let cardImg

let cards = [
    {title: 'card 1', text: 'lorem ispum lorem blablablablablabla'},
    {title: 'card 2', text: 'lorem ispum lorem blablablablablabla'},
    {title: 'card 3', text: 'lorem ispum lorem blablablablablabla'}
];
</script>

<div style="display: flex; flex-direction: row; margin-top: 6.25%;">

<div class="col third">
<div class="card">
<figure class="card-media">
<img src={cardImg}/>
</figure>
<div class="card-title">
<h2>{cardTitle}</h2>
</div>
<div class="card-content">
    <p>{cardText}</p>
</div>
</div>
</div>

</div>

<style>

h2{
    font-size: 2em;
    text-decoration: underline var(--main-color_medium);
    text-transform: capitalize;
}

.card{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #343434;
    width: 100%;
    height: 50vh;
}

.col{
    display: flex;
    flex-direction: column;
    margin: 0 2.5em;
}

.third{
    width: 33%;
}
</style>

-->