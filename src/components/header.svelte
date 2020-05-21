<script>
    import Nav from '../components/Nav.svelte';
    import MobileNav from '../components/mobile-nav.svelte';
    import Logo from '../components/logo.svelte';
    export let segment;
</script>

<div style="background-color: var(--bg-color_dark);">
<MobileNav/>
<header>
<div class="logo_container"> <Logo/> </div>
<Nav {segment}/>
</header>
</div>
<style>
header{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    padding: 1rem 0.5rem ;
    /* border-bottom: 1px solid var(--main-color_medium); */
    background-color: var(--bg-color_dark);
    height: 15vh;
}
</style>