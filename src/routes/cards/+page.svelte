<script>
    import { Card } from "$lib/components/custom/card";

    const cards = [
        {
            title: "Bonadan",
            image: "https://picsum.photos/id/11/400/300",
            description:
                "Echo Three to Echo Seven. Han, old buddy, do you read me? Loud and clear, kid. What's up? Well, I finished my circle. I don't pick up any life readings.",
        },
        {
            title: "Selonia",
            image: "https://picsum.photos/id/12/400/300",
            description:
                "Stay here and watch after the camp, Artoo. Oh, where is Artoo when I need him? Sir, I don't know where your ship learned to communicate, but it has the most peculiar dialect.",
        },
        {
            title: "Bestine IV",
            image: "https://picsum.photos/id/13/400/300",
            description:
                "What is thy bidding, my master? There is a great disturbance in the Force. I have felt it. We have a new enemy - Luke Skywalker. Yes, my master. He could destroy us.",
        },
        {
            title: "Carida",
            image: "https://picsum.photos/id/14/400/300",
            description:
                "Now matters are worse. That boy is our last hope. No. There is another. The ship is almost finished.",
        },
        {
            title: "Balmorra",
            image: "https://picsum.photos/id/15/400/300",
            description:
                "Will you join me for a little refreshment? Everyone's invited, of course. Having trouble with you droid? No. No problem.",
        },
        {
            title: "Dantooine",
            image: "https://picsum.photos/id/16/400/300",
            description:
                "I said turn her around! I'm going to put all power in the front shield. You're going to attack them?! Sir, the odds of surviving a direct assault on an Imperial Star Destroyer.",
        },
        {
            title: "Anoth",
            image: "https://picsum.photos/id/17/400/300",
            description:
                "Thank you. What did you have in mind for your next move? Well, if they follow standard Imperial procedure, they'll dump their garbage before they go to light-speed, then we just float away.",
        },
        {
            title: "Dagobah",
            image: "https://picsum.photos/id/18/400/300",
            description:
                "You look absolutely beautiful. You truly belong here with us among the clouds. Thank you. Will you join me for a little refreshment? Everyone's invited, of course.",
        },
        {
            title: "Bothawui",
            image: "https://picsum.photos/id/19/400/300",
            description:
                "What have we here? Welcome. I'm Lando Calrissian. I'm the administrator of this facility. and who might you be? Leia.",
        },
        {
            title: "Honoghr",
            image: "https://picsum.photos/id/10/400/300",
            description:
                "Reckless is he. Now matters are worse. That boy is our last hope. No. There is another. The ship is almost finished. Two or Three more things and we're in great shape.",
        },
    ];
</script>

<div class="cards-layout">
    {#each cards as card}
        <Card {...card} />
    {/each}
</div>

<style lang="postcss">
    .cards-layout {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(19rem, 1fr));
        gap: 20px;
    }
</style>
