<script>
export let segment;
</script>

<nav class="desk-nav">
		<a aria-current='{segment === undefined ? "page" : undefined}' href='.'>home</a>
		<a aria-current='{segment === "about" ? "page" : undefined}' href='about'>about</a>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<a rel=prefetch aria-current='{segment === "blog" ? "page" : undefined}' href='blog'>blog</a>
</nav>

<style>


a{
    color:  #EF003C;
    text-decoration: none;
    margin: 0 1em;
    font-size: 1.5em;
}



a:hover{
    color: #a40a32;
}


    .desk-nav{
        display: inline;
    }

@media only screen and (max-width: 441px){
    .desk-nav{
        display: none;
    }
}
</style>
