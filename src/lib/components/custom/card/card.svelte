<script lang="ts">
    type CardProps = {
        title: string;
        image: string;
        description: string;
    };

    let { title, image, description }: CardProps = $props();
</script>

<div class="card-container">
    <div class="layout">
        <h4>{title}</h4>
        <img src={image} alt={title} />
        <p>{description}</p>
    </div>
</div>

<style lang="postcss">
    .card-container {
        container-type: inline-size;

        @apply rounded-lg border bg-card text-card-foreground shadow-sm;
    }

    h4 {
        grid-area: title;
        @apply text-lg font-bold;
    }

    img {
        grid-area: img;
        aspect-ratio: 2;
        width: 100%;
        object-fit: cover;
        @apply rounded-sm;

        @container (width > 25rem) {
            aspect-ratio: 1;
        }
    }

    p {
        grid-area: description;

        @apply text-sm;
    }

    .layout {
        display: grid;
        grid-template-columns: minmax(0, 1fr);
        grid-template-areas: "title" "img" "description";
        gap: 10px 16px;
        padding: 20px;

        @container (width > 25rem) {
            grid-template-columns: 8rem minmax(0, 1fr);
            grid-template-areas: "title title" "img description";
        }
    }
</style>
