<script>
  const { id = 'input', label, description, error, ...props } = $props();
  const descriptionId = description ? `${id}-description` : undefined;
  const errorId = error ? `${id}-error` : undefined;
</script>

<div class="group space-y-1">
<form class="has-[input:user-invalid]:bg-red-400 has-[input:valid]:bg-green-200 bg-blue-300 p-2 rounded-md">

  <label
    class="flex font-medium
   text-slate-900 after:ml-2 after:block after:h-2 after:w-2 after:rounded-full
   group-has-[input:required]:after:text-red-600 group-has-[input:required]:after:content-['*']"
    for={id}>{label}</label
  >
  <input
  class="block
  w-full
  rounded
  bg-white
  px-2 py-1 placeholder-slate-600 outline-1 placeholder:font-light user-invalid:outline-red-600 focus:outline-4 focus:outline-blue-600"
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
</form>
</div>
