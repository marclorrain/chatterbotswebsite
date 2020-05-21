<script>
let TwitterIcon = '../images/twitter-icon.svg';
let LinkedinIcon = '../images/linkedin-icon.svg';

export let segment;
</script>

<footer>
<div class="footer-container">
<h4>Website</h4>
<nav>
	<ul>
		<li><a aria-current='{segment === undefined ? "page" : undefined}' href='.'>home</a></li>
		<li><a aria-current='{segment === "about" ? "page" : undefined}' href='about'>about</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li><a rel=prefetch aria-current='{segment === "blog" ? "page" : undefined}' href='blog'>blog</a></li>
	</ul>
</nav>
</div>

<div>
<h4>Follow-us on social media</h4>

<div class="social-icons">
<a href="www.twitter.com">
<img src={TwitterIcon} alt="twitter icon" class="social_icons">

</a>
<a href="www.linked.com">
<img src={LinkedinIcon} alt="linkedin icon" class="social_icons">
</a>
</div>

</div>

</footer>

<style>
footer{
    min-height: 15vh;
    color: var(--text-color_dark);
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    position: relative;
}

.footer-container{
    position: relative;
}

footer li{
    list-style: none;
    line-height: 1.5em;
}

footer a{
    color: var(--text-color_dark);
    text-decoration: none;
}

.social-icons{
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: stretch;
    flex-grow: 2;
    height: auto;
    max-width: 30%;
}
.social-icons a{
    width: 100%;
    height: auto;
}
.social_icons{
    width: 100%;
    height: auto;
}

a:hover{
    filter: opacity(0.6);
}

@media only screen and (max-width: 441px){
    footer{
        flex-direction: column;
        justify-content: space-evenly;
        align-content: flex-start;
    }
    .social-icons{
        justify-content: space-around;
        align-items: space-around;
    }
}
</style>