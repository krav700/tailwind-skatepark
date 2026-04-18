<script>
  const { title = 'Card Title', description = '' } = $props();
</script>

<div class="border-2 border-solid rounded-md border-slate-300 bg-slate-50 p-4 shadow-md">
  <h2 class="border-b-2 border-b-olive-500 text-lg font-semibold">{title}</h2>
  <p class="mt-1">{description}</p>
</div>
