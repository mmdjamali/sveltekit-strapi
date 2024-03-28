<script>
  import Icon from '$lib/components/ui/icon.svelte';
  import { Button, Input, Label, Spinner } from 'flowbite-svelte';

  let pending = false;
</script>

<main class="h-svh bg-gray-50 grid place-items-center">
  <div
    class="grid lg:grid-cols-2 sm:grid-cols-[6fr_4fr] grid-cols-1 w-full h-full"
  >
    <div class="grid place-items-center w-full h-full py-8 px-6">
      <form
        class="flex shadow bg-white rounded-lg space-y-6 flex-col max-w-md p-8 mx-auto w-full"
      >
        <h1
          class="text-xl font-bold leading-tight tracking-tight text-gray-900 md:text-2xl dark:text-white"
        >
          ورود به حساب
        </h1>

        <div>
          <Label class="mb-2">ایمیل</Label>

          <Input id="email" name="email" placeholder="your@email.com" />
        </div>

        <div>
          <Label class="mb-2">رمز</Label>

          <Input
            type="password"
            placeholder="••••••••"
            id="password"
            name="password"
          />
        </div>

        <Button
          disabled
          class="no-animation"
          on:click={() => {
            pending = true;
            setTimeout(() => {
              pending = false;
            }, 2000);
          }}
        >
          <span> بزن بریم </span>
          {#if pending}
            <Icon class="ri-loader-4-line animate-spin ms-2" />
          {:else}
            <Icon class="ri-arrow-right-line ms-2" rtl={true} />
          {/if}
        </Button>

        <p class="text-sm font-light text-gray-500 dark:text-gray-400">
          هنوز حساب کابری نداری؟
          <a
            class="font-medium text-primary-600 hover:underline dark:text-primary-500"
            href="/register"
          >
            خب بساز
          </a>
        </p>
      </form>
    </div>

    <div class="bg-primary-600 hidden sm:block w-full h-full"></div>
  </div>
</main>
