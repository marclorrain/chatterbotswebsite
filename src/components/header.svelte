<script>
    import Nav from '../components/Nav.svelte';
    import MobileNav from '../components/mobile-nav.svelte';
    import Logo from '../components/logo.svelte';
    export let segment;
</script>

<header>
<MobileNav/>
<div class="logo_container"> <Logo/> </div>
<Nav {segment}/>
</header>

<style>
header{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    padding: 1rem 0.5rem ;
    border-bottom: 1px solid var(--main-color_medium);
}
</style>