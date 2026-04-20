{#snippet link(title)}
  <li class="group border-b-4 hover:bg-red-50 px-4 py-2">
    <a href="#" >{title}</a>
  </li>
{/snippet}

<nav class="flex justify-between border-b-4 border-red-200">
  <a class="text-xl font-extrabold flex items-center " href="/">Unicorn Corp</a>
  <ul class="flex gap-8">
    {@render link('Home')}
    {@render link('About')}
    {@render link('Services')}
    {@render link('Contact')}
  </ul>
</nav>
