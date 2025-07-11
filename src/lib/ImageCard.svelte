<!-- src/lib/ImageCard.svelte -->

<script>
    export let image; // Image URL prop
    export let title; // Title prop
    export let description; // Description prop
</script>

<div class="card bg-[#213547] dark:bg-white">
    <img src={image} alt={title} />
    <div class="card-content">
        <h2 class="card-title text-[#ddd] dark:text-[#333]">{title}</h2>
        <p class="card-description text-[#666]">{description}</p>
    </div>
</div>

<style>
    .card {
        border: 1px solid #213547;
        border-radius: 10px;
        overflow: hidden;
        width: 100%;
        box-shadow: 0 4px 8px rgba(255, 255, 255, 0.3);
        text-align: center;
    }

    .card img {
        width: 100%;
        height: auto;
    }

    .card-content {
        padding: 15px;
    }

    .card-title {
        font-size: 1.5em;
        margin: 0 0 10px 0;
    }

    .card-description {
        font-size: 1em;
        margin: 0;
    }

    @media (prefers-color-scheme: light) {
        .card {
            border: 1px solid white;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
        }
    }
</style>
