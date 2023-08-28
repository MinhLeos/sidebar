<script>
  export let path = '';
  export let tooltip = '';
</script>

<div class="btn transition">
  <svg aria-hidden="true" role="img" width="24" height="24" viewBox="0 0 24 24"><path fill="currentColor" d={path}></path></svg>
  <p class="tooltip">{tooltip}</p>
</div>
<style scoped>
  .btn {
    @apply relative flex items-center justify-center bg-slate-300 w-16 h-16 mt-4 rounded-[128px] text-[#23a559];
  }
  .btn:hover {
    @apply text-white rounded-2xl bg-green-500;
  }
  .tooltip {
    @apply invisible absolute text-white left-24 min-w-[150px] py-1.5 px-2.5 rounded-xl bg-slate-600 opacity-0;
    -webkit-transition: all 1s ease-in-out;
    transition: all 1s ease-in-out;
  }
  .btn:hover .tooltip {
    @apply visible opacity-100;
    -webkit-transition: all 0.75s ease-in-out;
    transition: all 0.75s ease-in-out;
  }
  .transition {
      /* -webkit-transition: background-color 0.75s linear, border-radius 0.75s linear;
      transition: background-color 0.75s linear, border-radius 0.75s linear; */
      -webkit-transition: all 0.5s ease-in-out;
      transition: all 0.5s ease-in-out;
  }
</style>