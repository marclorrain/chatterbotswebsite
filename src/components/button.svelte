<script>
export let CTAText;
export let Link;
</script>

<a href={Link}>
{CTAText}
</a>

<style>
a{
    color: white;
    text-decoration: none;
    background-color: var(--secondary-color_light);
    margin: 2rem;
    padding: 1.5rem;
    border-radius: 10px;
    font-size: 1.5rem;
    max-width: 50%;
    filter: var(--shadow-filter)
}

a:hover{
    text-decoration: underline;
    background-color: transparent;
    border: 1px solid var(--secondary-color_light);
    color: var(--secondary-color_light);
}

@media only screen and (max-width: 441px){
    a {
        max-width: 49%;
        font-size: 1rem;
        padding: 0.75rem;
    }
}
</style>