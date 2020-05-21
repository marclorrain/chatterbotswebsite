<script>
    export let segment;
    export let visible = false;
    function handleClick(){
       if (visible == true) {
       visible = false
       } else {
           visible = true
       }
    }

</script>

<div class="menu_button mobile-nav">

<button on:click={handleClick} >
  <hr>
  <hr>
  <hr>
</button>

</div>

{#if visible}

<nav id="nav-menu" class="mobile-nav">
	<ul>
		<li><a aria-current='{segment === undefined ? "page" : undefined}' href='.'>home</a></li>
		<li><a aria-current='{segment === "about" ? "page" : undefined}' href='about'>about</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li><a rel=prefetch aria-current='{segment === "blog" ? "page" : undefined}' href='blog'>blog</a></li>
	</ul>
</nav>

<style>
hr{
    background-color: #F5537B !important;
}
</style>

{/if}

<style>
#nav-menu{
    background-color: #343434;
    display: flex;
    flex-direction: column;
    width: 20%;
    padding: 10% 0;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    text-align: left;
    z-index: 10;
}

a{
    color:  #EF003C;
    text-decoration: none;
    margin: 0 1em;
    font-size: 1.5em;
}

button{
    background-color: transparent;
    border: none;
    width: 100%;
    padding: 0;
    outline: none;
}

hr{
    background-color: #EF003C;
    border: none;
    border-radius: 10px;
    height: 3px;
    margin: 0.45em 0;
}

hr:nth-of-type(2){
    width: 1.75em;
}

.menu_button{
    width: 2.25em;
    margin: 0.5em;
    z-index: 15;
    position: absolute;
}

.menu_button:hover hr{
    background-color: #a40a32;
}

.menu_button:active hr{
    background-color:white;
}

a:hover{
    color: #a40a32;
}

li {
    list-style: none;
}

    .mobile-nav{
        display: none;
    }

@media only screen and (max-width: 441px){
    nav { 
        width: 50% !important;
        padding-top: 5em;
    }

    .mobile-nav{
        display: block;
    }
}
</style>
