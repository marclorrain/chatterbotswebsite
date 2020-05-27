<script>

let cards = [
    {title: 'Meet your latest sales superstar.', text: 'Chatterbots identify, qualify, and direct potential leads, putting new customers in touch with exactly the right representative.', img: '../favicon-alt.svg'},
    {title: '24/7/365', text: 'Chatterbots are always on hand to answer questions, take orders, handle returns, and more. Show your customers you care with 24/7 service.', img: '../favicon-alt.svg'},
    {title: 'Speed up productivity', text: 'Chatterbots can take orders, log requests, book appointments, and more - freeing up your valuable time to focus on long term strategic goals.', img: '../favicon-alt.svg'}
];
</script>
<div>
<div class="flex-grid-wrap">
{#each cards as card}
<div class="flex-grid third">

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
</div>
<style>

@media only screen and (max-width: 441px){
    .card{
        position: relative;
        top: 0;
        left: 0;
        width: 100%;
    }
    .third{
    min-width: 100%;
}

}

h2{
    font-size: 2em;
    text-decoration: underline var(--main-color_medium);
    text-transform: capitalize;
    text-align: center;
}

.card{
    display: flex;
    flex-direction: column;
    justify-content:space-evenly;
    align-items: center;
    width: 70%;
    height: 50vh;
    text-align: left;
}

.card p{
    font-size: 1.25em;
    font-weight: 400;
}

.card-media{
    width: 15%;
    height: auto;
}

.third{
    width: 30%;
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