<script>
  import { onMount } from 'svelte';
  let visible = false;
  let el;
  onMount(() => {
    if (!el) return;
    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting) {
          visible = true;
          observer.disconnect();
        }
      },
      { threshold: 0.15 }
    );
    observer.observe(el);
    return () => observer.disconnect();
  });
</script>

<div bind:this={el} class:visible={visible}>
  <slot />
</div>

<style>
div {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.7s cubic-bezier(.4,0,.2,1), transform 0.7s cubic-bezier(.4,0,.2,1);
}
.visible {
  opacity: 1;
  transform: none;
}
</style>
