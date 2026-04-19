<script>
  const { id = 'input', label, description, error, ...props } = $props();
  const descriptionId = description ? `${id}-description` : undefined;
  const errorId = error ? `${id}-error` : undefined;
</script>

<div class="space-y-1">
  <label class="block font-medium text-slate-900" for={id}>{label}</label>
  <input
    class="block
     w-full
      rounded
       bg-white
        px-2 py-1
         placeholder-slate-600 outline-1 placeholder:font-light user-invalid:outline-red-600 focus:outline-4 focus:outline-blue-600"
    {id}
    aria-describedby={descriptionId}
    aria-invalid={!!error}
    aria-errormessage={errorId}
    {...props}
  />
  {#if description}
    <p id={descriptionId}>{description}</p>
  {/if}
  {#if error}
    <p id={errorId}>{error}</p>
  {/if}
</div>
