<script>
import Btn from '../components/button.svelte';
let src = '../images/chatterbots-automation.svg';
</script>

<div class="flex-grid-wrap">
<div class="flex-grid">
<img src={src} alt="automate all the things!">
</div>

  <div class="flex-grid">
      <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent faucibus lacus id turpis ornare, at tempor sapien pharetra. Mauris id libero luctus diam rutrum ornare in eu odio. Quisque a lorem id libero dictum venenatis vel et tellus. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aliquam eleifend dolor ligula, ac scelerisque eros vehicula eget. Donec ex risus, viverra scelerisque luctus ac, consectetur id lorem. In a lacinia purus. Nunc accumsan egestas nulla in dapibus. Sed molestie eleifend purus, eget finibus ante scelerisque a. Nulla vitae interdum quam. Mauris rhoncus velit quam, non ultricies ipsum egestas eu. Praesent aliquam elit eu ligula ultricies, sit amet posuere urna sollicitudin. Proin id erat a nisi suscipit rutrum eu in mi. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Donec rutrum quam est, sit amet faucibus turpis pretium ac. Aenean mauris libero, volutpat ut mauris in, tincidunt ultrices purus.</p>
  <Btn CTAText={'Chat with Cassia'} Link={'#hello'}/>
  </div>

</div>

<style>
@media only screen and (max-width: 441px){

  p{
  width: 95% !important;
  padding: 0 !important;
  font-size: 1em;
} 
}

p{
  font-size: 1.25em;
  width: 100%;
  height: auto;
}

img{
  width: 100%;
  height: auto;
  filter: var(--shadow-filter)
}
</style>