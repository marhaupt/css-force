<script lang="ts">
    import NavigationSlider from "$lib/containers/NavigationSlider.svelte";
    import Settings from "$lib/containers/Settings.svelte";
    import "../app.css";

    let { children } = $props();
</script>

<header
    class="bg sticky top-0 z-50 flex items-center justify-between border-b bg-background/50 px-[16px] py-[10px] backdrop-blur-sm"
>
    <div class="whitespace-nowrap text-2xl">CSS FORCE</div>
    <div class="flex gap-[10px]">
        <div>
            <Settings />
        </div>
        <div>
            <NavigationSlider />
        </div>
    </div>
</header>

<main class="p-[16px]">
    {@render children()}
</main>
