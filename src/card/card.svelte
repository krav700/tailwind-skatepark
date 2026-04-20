<script>
  const { title = 'Card Title', description = '' } = $props();
</script>

<div class="text-gray-900 dark:text-slate-200 rounded-md border border-slate-300 bg-slate-50 p-4 dark:bg-slate-800 dark:border-slate-700">
  <h2 class="border-b-2 border-b-olive-500 text-lg font-semibold">{title}</h2>
  <p class="mt-1">{description}</p>
</div>
