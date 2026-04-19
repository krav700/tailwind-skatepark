<script>
  const { label = 'A Very Important Checkbox', id = 'checkbox', ...props } = $props();
</script>

<div class="border bg-slate-200 p-4 rounded focus-within:bg-sky-200 outline-sky-400 outline-offset-2">
  <input class="accent-purple-400" {id} {...props} type="checkbox" />
  <label for={id}>{label}</label>
</div>
