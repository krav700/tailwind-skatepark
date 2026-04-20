<script>
  import PrimaryButton from "../button/primary-button.svelte";

  const { label = 'A Very Important Checkbox', id = 'checkbox', ...props } = $props();
</script>

<div
  class="group flex flex-col gap-2 rounded border bg-slate-200 p-4 outline-offset-2 outline-sky-400 has-[input:checked]:bg-purple-200"
>
  <div>
    <input class="peer accent-purple-400" {id} {...props} type="checkbox" />
    <label class="group-has-checked:line-through peer-checked:text-purple-500" for={id}
      >{label}</label
    >
  </div>
  <div class="hidden flex-col group-has-checked:flex gap-2">
    <label>What is your reason?</label>
    <input
      class="block
  w-full
  rounded
  bg-white
  px-2 py-1 placeholder-slate-600 outline-1 placeholder:font-light user-invalid:outline-red-600 focus:outline-4 focus:outline-blue-600"
      placeholder="Enter your reason here"
      required
    />
    <button class="group-has-[input:invalid]:hidden">Submit</button>
  </div>
</div>
