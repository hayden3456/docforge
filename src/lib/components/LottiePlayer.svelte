<script>
  import { onMount, onDestroy } from 'svelte';
  import lottie from 'lottie-web';
  
  export let animationData;
  export let autoplay = true;
  export let loop = true;
  export let speed = 1;
  export let className = '';
  
  let containerElement;
  let animationInstance;
  
  onMount(() => {
    if (containerElement && animationData) {
      animationInstance = lottie.loadAnimation({
        container: containerElement,
        renderer: 'svg',
        loop: loop,
        autoplay: autoplay,
        animationData: animationData,
        speed: speed
      });
    }
  });
  
  onDestroy(() => {
    if (animationInstance) {
      animationInstance.destroy();
    }
  });
  
  // Reactive updates
  $: if (animationInstance) {
    animationInstance.setSpeed(speed);
    if (autoplay) {
      animationInstance.play();
    } else {
      animationInstance.pause();
    }
  }
</script>

<div bind:this={containerElement} class={className}></div>
