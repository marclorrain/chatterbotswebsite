
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
	.content :global(h2) {
		font-size: 1.4em;
		font-weight: 500;
	}

	.content :global(pre) {
		background-color: #f9f9f9;
		box-shadow: inset 1px 1px 5px rgba(0,0,0,0.05);
		/*padding: 0.5em;*/
		border-radius: 2px;
    overflow-x: auto;
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
  .content p{
    /*display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-content: space-around;*/
  }
  .container{
    padding: 2rem;
    width: 80%;
  }

img {
    width: 25%;
    height: auto;
    margin: 2rem;
}
</style>

<svelte:head>
	<title>{post.title}</title>
</svelte:head>
<div class="container">

<h1>{post.title}</h1>
<div class='content'>
  <img src={post.blogImg.url} alt="something" align="left"/>
	{@html marked(post.content)}
</div>

</div>