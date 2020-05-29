<script>

let TwitterIcon = '../images/twitter-icon.svg';
let LinkedinIcon = '../images/linkedin-icon.svg';

export let segment;

import {goto} from '@sapper/app';
import NavList from '../components/navlist.svelte'
</script>

<footer>
<div class="footer-container">
<h4>Website</h4>
<nav>
	<ul>
		<NavList/>
	</ul>
</nav>
</div>

<div>
<h4>Follow-us on social media</h4>

<div class="social-icons">
<a href="https://twitter.com/cassia_chtrbots">
<img src={TwitterIcon} alt="twitter icon" class="social_icons">

</a>
<a href="https://www.linkedin.com/company/chatterbots-agency">
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