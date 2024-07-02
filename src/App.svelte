<script>
  import Slider from './Slider.svelte';
  let greenColor = 0;
  let blueColor = 0;
  let yellowColor = 0;
</script>

<div class="row">
  <div class="col">
    <h1>Color Picker</h1>
 </div>
</div>
<div class="row">
  <div class="column">
   <form>
      <Slider colorName ="Green" bind:colorValue={greenColor}/>
      <Slider colorName ="Blue" bind:colorValue={blueColor}/> 
      <Slider colorName ="Yellow" bind:colorValue={yellowColor}/>
   </form>
  </div>
</div>
<div class="row">
  <div class="column">
   <div id="color" style="background-color: rgb({greenColor}, {blueColor}, {yellowColor})"/>
  </div>
</div>
<div class="row">
  <div class="column">
    <h2>rgb({greenColor}, {blueColor}, {yellowColor})</h2>
  </div>
</div>
<style>
    #color {
      height: 300px;
      border: dashed 5px;
    }
    h2 {
      text-align: center;
      margin-top: 20px;
    }
</style>

