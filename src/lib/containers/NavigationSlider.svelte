<script lang="ts">
    import { Button } from "$lib/components/ui/button";
    import * as Sheet from "$lib/components/ui/sheet";
    import { Menu } from "lucide-svelte";

    let open = $state(false);

    const close = () => (open = false);
</script>

<Sheet.Root {open}>
    <Sheet.Trigger>
        <Button variant="outline" size="icon" on:click={() => (open = true)}>
            <Menu />
        </Button>
    </Sheet.Trigger>
    <Sheet.Content>
        <nav class="flex flex-col gap-[10px]">
            <a href="/" onclick={close}>Home</a>
            <a href="/cards" onclick={close}>Cards grid</a>
        </nav>
    </Sheet.Content>
</Sheet.Root>
