<script>
  import "../app.postcss";
  import { AppShell } from "@skeletonlabs/skeleton";
  import { AppBar } from "@skeletonlabs/skeleton";
  import { Avatar } from "@skeletonlabs/skeleton";
</script>

<AppShell slotSidebarLeft="bg-surface-500 w-48 p-2">
  <svelte:fragment slot="pageHeader">
  <AppBar>
        <svelte:fragment slot="lead">
          <button class="md:hidden btn btn-sm mr-4" on:click={drawerOpen}>
            <span>
              <svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
                <rect width="100" height="20" />
                <rect y="30" width="100" height="20" />
                <rect y="60" width="100" height="20" />
              </svg>
            </span>
          </button>
          <strong class="text-xl">Memo</strong>
        </svelte:fragment>
        <svelte:fragment slot="trail">
          <Avatar initials="JD" width="w-10" background="bg-primary-500" />
        </svelte:fragment>
      </AppBar>
  </svelte:fragment>

  <svelte:fragment slot="sidebarLeft">
    <nav class="list-nav">
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
      </ul>
    </nav>
  </svelte:fragment>
  <slot />
</AppShell>
