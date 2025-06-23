<script lang="ts">
  type Link = {
    title: string;
    href: string;
  };

  const LinkList: Link[] = [
    {
      title: "privacy-policy-psde",
      href: "privacy-policy-psde",
    },
  ];
</script>

<div class="p-2 w-1/2">
  <h1 class="text-6xl pb-5 select-none">document</h1>
  <ul class="list-disc list-inside">
    {#each LinkList as link}
      <li>
        <a
          class="underline text-gray-300 hover:text-gray-400"
          href="/document/{link.href}">{link.title}</a
        >
      </li>
    {/each}
  </ul>
</div>
