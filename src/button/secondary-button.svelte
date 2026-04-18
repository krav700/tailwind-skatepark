<script>
  const { label = 'Button', ...props } = $props();
</script>

<button class="bg-white outline outline-slate-600 hover:bg-slate-100 px-3 py-1.5 rounded-md shadow-sm " {...props}>{label}</button>