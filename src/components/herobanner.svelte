<script>
import Btn from '../components/button.svelte';
let src = '../images/chatterbots-automation.svg';
</script>

<div class="flex-grid-wrap">
<div class="flex-grid">
<img src={src} alt="automate all the things!" class="hide-mobile">
</div>

  <div class="flex-grid">
      <p>
      Our experts will design, set up, and maintain your chatbot, ensuring peak productivity and performance. We’ll integrate conversational marketing into your workflow, allowing your team to focus on what they do best. <br> <br>

But don’t take our word for it. Stay and chat a while with Cassia, the spiciest chatterbot of them all.

     </p>
  <Btn CTAText={'Chat with Cassia'} Link={'#hello'}/>
  </div>

</div>

<style>

@media only screen and (max-width: 441px){

  p{
  min-width: 95% !important;
  padding: 0 !important;
  font-size: 1em;
} 
.hide-mobile{
  display: none;
}
}

p{
  font-size: 1.75em;
  max-width: 60%;
  height: auto;
}

img{
  width: 100%;
  height: auto;
  filter: var(--shadow-filter)
}
</style>