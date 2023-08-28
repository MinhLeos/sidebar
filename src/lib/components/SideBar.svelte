<script>
  import Button from "./Button.svelte";
  import { icCompass, icDownload, icPlus, icClock } from "$lib/Icons/icons";

  const listMenus = [
    {
      icon: icCompass,
      tooltip: 'Icon Compass'
    },
    {
      icon: icDownload,
      tooltip: 'Icon Download'
    },
    {
      icon: icPlus,
      tooltip: 'Icon Plus'
    },
    {
      icon: icClock,
      tooltip: 'Icon Clock'
    }
  ]
</script>

<div class="fixed top-0 bottom-0 left-0 w-28 bg-slate-600 flex flex-col items-center justify-start">
  <div class="mt-10">
    {#each listMenus as menu}
      <Button tooltip={menu.tooltip} path={menu.icon} />
    {/each}
  </div>
</div>