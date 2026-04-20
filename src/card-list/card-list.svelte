<script lang="ts">
  import PrimaryButton from '../button/primary-button.svelte';
  import Card from '../card/card.svelte';
</script>

<div class="flex gap-2 items-center justify-center h-96 bg-red-200">
  <div>
    <input type="checkbox" />
  </div>
  <h2>Unsubscribe</h2>
  <PrimaryButton />
</div>

<div class="flex flex-col gap-4 md:flex-row">
  <Card title="Card Title" description="This is a description of the card." />
  <Card title="Another Card" description="This is another description of a different card." />
  <Card title="Third Card" description="This is a description of the third card." />
  <Card title="Fourth Card" description="This is a description of the fourth card." />
</div>
