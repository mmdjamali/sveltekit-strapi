<script lang="ts">
  import { cn } from '$lib/utils';

  let className = '';
  let rtl: boolean = false;

  export { className as class, rtl };
</script>

<span
  class={cn('text-lg leading-none', rtl && 'rtl:!-scale-x-100', className)}
/>
