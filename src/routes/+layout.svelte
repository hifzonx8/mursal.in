<script lang="ts">
  import "../app.css";

  let { children } = $props();

  type HeaderLink = {
    title: string;
    href: string;
  };

  const HeaderLinkList: HeaderLink[] = [
    {
      title: "main",
      href: "/",
    },
    {
      title: "document",
      href: "/document",
    },
    {
      title: "links",
      href: "/links",
    },
  ];

  console.log();
</script>

<div class="min-h-screen w-full bg-neutral-900 text-white">
  <header class="bg-neutral-800 py-4 flex justify-center">
    <nav class="flex space-x-4 text-xl">
      {#each HeaderLinkList as link, i}
        <a class="hover:underline" href={link.href}>{link.title}</a>
      {/each}
    </nav>
  </header>
  {@render children()}
</div>
