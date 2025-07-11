<script>
    let name = "sita vemuri";
    let favoriteNumber = "🎱";
    let bio = "i'm an incoming college freshman and i love to code. you can find out more about me below!";
    let facts = ["i've never lost a fight against a hippopotamus. 🦛", "i play the violin. 🎻", "i was once TIME's person of the year (2006). 📰", "i have two dogs. 🐶"];

    import ImageCard from "./lib/ImageCard.svelte";

    let cardData = [
        {
            image: "/images/pic-1.jpeg",
            title: "film photography",
            description: "shooting, developing, and printing film. the process is soo rewarding!",
        },
        {
            image: "/images/pic-2.jpeg",
            title: "travel",
            description: "learning more about the world and the different places and cultures within it.",
        },
        {
            image: "/images/pic-3.jpeg",
            title: "crochet",
            description: "a relaxing, satisfying hobby. still trying to get better at it!",
        },
        {
            image: "/images/pic-4.jpeg",
            title: "coco",
            description: "my first dog. she's really shy and a bit grumpy!",
        },
        {
            image: "/images/pic-5.jpeg",
            title: "digital photography",
            description: "taking photos, capturing the stories around me.",
        },
        {
            image: "/images/pic-6.jpeg",
            title: "maple",
            description: "my second dog. she's really brave but thinks she's still a tiny puppy!",
        },
    ];
</script>

<div class="container">
    <h1>about me</h1>
    <p>hii, my name is <strong>{name}</strong>!</p>
    <p>{bio}</p>
    <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>
</div>

<div class="container">
    <h2>some fun facts</h2>
    <div class="facts">
        {#each facts as fact}
            <div class="fact">{fact}</div>
        {/each}
    </div>
</div>

<div class="container">
    <h2>some of my favorite things</h2>
    <div class="card-container grid grid-cols-3 gap-8">
        {#each cardData as { image, title, description }}
            <ImageCard {image} {title} {description} />
        {/each}
    </div>
</div>

<style>
    h1 {
        font-family: Arial, sans-serif;
    }
    .container {
        margin: 0 auto;
        padding: 15px;
        text-align: center;
    }
    .facts {
        display: flex;
        justify-content: center;
        gap: 15px;
        flex-wrap: wrap;
    }
    .fact {
        background-color: #3498db;
        color: white;
        padding: 10px 15px;
        border-radius: 5px;
    }
    .card-container {
        grid-template-rows: auto 1fr;
    }
</style>
