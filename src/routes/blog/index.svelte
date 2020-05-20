<!-- <script context="module">
	export function preload({ params, query }) {
		return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
			return { posts };
		});
	}
</script> -->

<script context="module">
  export async function preload(page, session) {
    const res = await this.fetch(
      "https://api-us-east-1.graphcms.com/v2/ckaed1ly505dc01z78zp8b3t1/master",
      {
        method: "post",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({
          query: `{
          posts: blogPosts(stage: PUBLISHED){
            slug
            title
			summary
			blogImg {
                    url
			}
			publicationDate
          }
        }`
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
	export let posts;
</script>

<style>
	@media only screen and (max-width: 441px){
    .card{
        position: relative;
        top: 0;
        left: 0;
        max-width: 100%;
	}
	.blog-card{
		flex-direction: column;
	}
	aside{
	min-width: 100%;
}

	.card-media{
		display: none;
	}

}

.blog-title{
    font-size: 2em;
    text-decoration: underline var(--main-color_medium);
	text-transform: capitalize;
	color: white;
}

.blog-card{
	display: flex; 
	flex-direction: row; 
	justify-content: space-around;
}

.card{
    display: flex;
    flex-direction: column;
    justify-content:space-evenly;
    align-items: center;
    width: 100%;
    height: 50vh;
	text-align: left;
	border: 1px white solid;
	border-radius: 5px;
}

.card-media{
    width: 35%;
    height: auto;
}

.card p{
	font-size: 1.25rem;
}

aside{
	width: 50%;
}

</style>

<svelte:head>
	<title>Blog</title>
</svelte:head>

<h1>Recent posts</h1>
<div class="flex-grid-wrap">
	{#each posts as post}
		<!-- we're using the non-standard `rel=prefetch` attribute to
				tell Sapper to load the data for the page as soon as
				the user hovers over the link or taps it, instead of
				waiting for the 'click' event -->

<div class="flex-grid">
<div class="card">

<div class="blog-card">
<figure class="card-media">
<img src={post.blogImg.url} alt="alt-text bozo" width="100%"/>
</figure>

<aside>
<div class="card-title">
<a rel='prefetch' href='blog/{post.slug}' class="blog-title">{post.title}</a>
</div>
<div class="card-content">
    <p>{post.summary}</p>
	<p> <i>Published on:{post.publicationDate} </i></p>
</div>
</aside>
</div>

</div>
</div>
	{/each}
	</div>