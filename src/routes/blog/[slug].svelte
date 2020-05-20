
<script context="module">
  export async function preload({ params, query }) {
    // the `slug` parameter is available because
    // this file is called [slug].svelte
    const res = await this.fetch(
      "https://api-us-east-1.graphcms.com/v2/ckaed1ly505dc01z78zp8b3t1/master",
      {
        method: "post",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          query: `query Post($slug: String) {
            post: blogPost(where: {
              slug: $slug
            }) {
              slug
              createdAt
              title
              content
              blogImg{
                url
              }
            }
          }`,
          variables: {
            slug: params.slug
          }
        })
      }
    );
    const json = await res.json();

    if (res.status === 200) {
      return json.data;
    } else {
      this.error(res.status, json && json.errors);
    }
  }
</script>

<script>
    import marked from "marked";
	export let post;
</script>

<style>
	/*
		By default, CSS is locally scoped to the component,
		and any unused styles are dead-code-eliminated.
		In this page, Svelte can't know which elements are
		going to appear inside the {{{post.html}}} block,
		so we have to use the :global(...) modifier to target
		all elements inside .content
  */
  .content :global(h1){
    font-weight: normal;
    font-family: 'Roboto Slab', serif;
    font-size: 2.5rem;
  }
	.content :global(h2) {
		font-size: 2rem;
    font-weight: 500;
    font-family: 'Roboto Slab', serif;
	}

	.content :global(pre) {
		background-color: #f9f9f9;
		box-shadow: inset 1px 1px 5px rgba(0,0,0,0.05);
		/*padding: 0.5em;*/
		border-radius: 2px;
  }
  
  .content :global(p){
    font-size: 1.5rem;
  }

	.content :global(pre) :global(code) {
    background-color: transparent;
	}

	.content :global(ul) {
		line-height: 1.5;
	}

	.content :global(li) {
		margin: 0 0 0.5em 0;
  }
  .container{
    padding: 3rem;
    margin: 5%;
    width: 80%;
    background-color: var(--bg-color_medium);
    filter: var(--shadow-filter);
  }

img {
    width: 25%;
    height: auto;
    margin: 2rem;
    filter: var(--shadow-filter);
}

.post-title{
  font-size: 3rem;
  font-weight: normal;
  text-decoration: underline;
  text-decoration-color: var(--main-color_medium);
  text-align: center;
  margin: 0 0 8rem 0;
}

.post-title::after{
  color: var(--main-color_medium);
  content: ".";
}

@media only screen and (max-width: 441px){
  img {
    width: 100%;
    height: auto;
    margin: 2rem 0;
}

.container {
  margin: 0;
  padding: 0;
  width: 100%;
}

.post-title{
  margin: 0 0 4rem 0;
}

}
</style>

<svelte:head>
	<title>{post.title}</title>
</svelte:head>
<div class="container">

<h1 class="post-title">{post.title}</h1>
<div class='content'>
  <img src={post.blogImg.url} alt="something" align="left"/>
	{@html marked(post.content)}
</div>

</div>