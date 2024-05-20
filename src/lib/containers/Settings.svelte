<script lang="ts">
    import { Button } from "$lib/components/ui/button";
    import * as DropdownMenu from "$lib/components/ui/dropdown-menu";
    import { Settings } from "lucide-svelte";

    let fontSize = $state<number | undefined>(undefined);

    const sizeUp = () => {
        if (fontSize === undefined) {
            fontSize = 17;
        } else {
            fontSize += 1;
        }
    };

    const sizeDown = () => {
        if (fontSize === undefined) {
            fontSize = 15;
        } else if (fontSize > 5) {
            fontSize -= 1;
        }
    };

    const sizeReset = () => {
        fontSize = undefined;
    };

    $effect(() => {
        if (fontSize !== undefined) {
            document.documentElement.style.fontSize = `${fontSize}px`;
        } else {
            document.documentElement.style.removeProperty("font-size");
        }
    });
</script>

<DropdownMenu.Root closeOnItemClick={false}>
    <DropdownMenu.Trigger asChild let:builder>
        <Button builders={[builder]} variant="outline" size="icon">
            <Settings />
        </Button>
    </DropdownMenu.Trigger>
    <DropdownMenu.Content class="w-[16ch]">
        <DropdownMenu.Label>
            Font size: {fontSize ? `${fontSize}px` : "100%"}
        </DropdownMenu.Label>
        <DropdownMenu.Item on:click={sizeUp}>Increase</DropdownMenu.Item>
        <DropdownMenu.Item on:click={sizeDown} disabled={fontSize !== undefined && fontSize <= 5}>
            Decrease
        </DropdownMenu.Item>
        <DropdownMenu.Item on:click={sizeReset} disabled={fontSize === undefined}>
            Reset
        </DropdownMenu.Item>
    </DropdownMenu.Content>
</DropdownMenu.Root>
