<script>
  import StackedContainer from './StackedContainer.svelte';
  import TextBubble from './TextBubble.svelte';

  export let title = "";
  export let description = "";
  export let hasCodeExample = false;
  export let hasTextBubble = false;
  export let bubbleText = "you got a minute?";
  export let imageSrc = "";
</script>

<div class="problem-card-container">
  <div class="card-content">
    <div class="rounded-xl bg-amber-50 p-6 ">
      {#if hasCodeExample}
        {#if imageSrc}
          <div class="image-wrapper">
            <img src={imageSrc} alt={title} class="problem-image" />
          </div>
        {:else}
          <StackedContainer />
        {/if}
      {:else if hasTextBubble}
        <div class="text-bubble-wrapper">
          <TextBubble text={bubbleText} />
        </div>
      {/if}
    </div>
    
    <div class="text-content">
      <h3 class="font-semibold text-slate-900 mt-4 text-2xl md:text-2xl sm:text-xl">{title}</h3>
      <p class="mt-2 text-slate-600 text-xl md:text-xl sm:text-lg">{description}</p>
    </div>
  </div>
</div>

<style>
/* ProblemCard container for positioning */
.problem-card-container {
  position: relative;
  height: 100%; /* Take full height of parent */
  display: flex;
  flex-direction: column;
}

/* Card content wrapper with flexbox */
.card-content {
  flex: 1; /* Take remaining space */
  display: flex;
  flex-direction: column;
  justify-content: center; /* Center the graphics vertically */
}

/* Text content pushed to bottom */
.text-content {
  margin-top: auto; /* Push to bottom */
}

/* Text bubble wrapper - takes up space in layout */
.text-bubble-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
  width: 100%;
  position: relative;
  margin-top: 20px;
}

/* Image wrapper for problem cards */
.image-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
  width: 100%;
  position: relative;
  margin-top: 20px;
}

/* Mobile responsive adjustments */
@media (max-width: 768px) {
  .text-bubble-wrapper,
  .image-wrapper {
    height: 150px;
    margin-top: 15px;
  }
}

.problem-image {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  border-radius: 8px;
}
</style>
