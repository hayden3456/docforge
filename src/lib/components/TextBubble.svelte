<script>
  export let text = "you got a minute?";
</script>

<div class="text-bubble">
  <div class="bubble-content">"{text}"</div>
  <div class="bubble-tail"></div>
  <div class="bubble-footer">
    <span class="not-equal">≠</span>
    <span class="time-text">1 Minute</span>
  </div>
</div>

<style>
/* Text bubble */
.text-bubble {
  position: relative;
  z-index: 10;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;

  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transform: scale(0.8);
  transform-origin: center;
  object-fit: contain;
}

.bubble-content {
  background: #104C35;
  color: white;
  padding: 0.4em 0.6em;
  border-radius: 0.7em;
  font-size: 2.5rem;
  font-weight: 500;
  box-shadow: 0 0.1em 0.2em rgba(0, 0, 0, 0.15);
  position: relative;
  line-height: 1.2;
  white-space: nowrap;
}

.bubble-tail {
  position: absolute;

  left: 3.2em;
  top:4.5em;
  width: 0;
  height: 0;
  border-left: 1.2em solid transparent;
  border-right: 1.2em solid transparent;
  border-top: 2.0em solid #104C35;
}

.bubble-footer {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.2em;
  margin-top: 0.4em;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

.not-equal {
  font-size: 4.5rem;
  font-weight: bold;
  color: #ef4444;
  transform: rotate(-8deg);
}

.time-text {
  font-size: 2.5rem;
  font-weight: 600;
  color: #374151;
}
</style>
