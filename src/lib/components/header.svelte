<script lang="ts">
  import { Button } from 'flowbite-svelte';
</script>

<header class="sticky top-0 z-[50] shadow">
  <nav
    class="bg-white max-w-screen-xl mx-auto flex items-center justify-between px-4 lg:px-6 h-16"
  >
    <div class="flex lg:flex-1">
      <a href="/" class="flex items-center">
        <div class="size-8 inline-grid rounded-full bg-primary-50 me-3"></div>

        <span
          class="self-center text-xl font-semibold whitespace-nowrap dark:text-white"
        >
          اسم برند
        </span>
      </a>
    </div>

    <div class="flex-grow-[2] hidden lg:flex justify-center">
      <ul class="flex items-center lg:space-x-8 rtl:lg:space-x-reverse">
        <li>
          <a
            href="/"
            class="text-gray-900 hover:text-primary-700"
            aria-current="page">صفحه اصلی</a
          >
        </li>
        <li>
          <a
            href="/"
            class="text-gray-900 hover:text-primary-700"
            aria-current="page">درباره ما</a
          >
        </li>
        <li>
          <a
            href="/"
            class="text-gray-900 hover:text-primary-700"
            aria-current="page">تماس با ما</a
          >
        </li>
      </ul>
    </div>

    <div class="flex shrink-0 items-center lg:flex-1">
      <a href="/login" class="me-2">
        <Button class="border-none whitespace-nowrap" color="alternative"
          >ورود به حساب</Button
        >
      </a>

      <a href="/register">
        <Button class="whitespace-nowrap">شروع کن</Button>
      </a>
    </div>
  </nav>
</header>
