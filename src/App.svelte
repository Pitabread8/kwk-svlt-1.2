<script>
    let name = "sita vemuri";
    let favoriteNumber = "🎱";
    let bio = "i'm an incoming college freshman and i love to code. you can find out more about me below!";
    let facts = ["i've never lost a fight against a hippopotamus. 🦛", "i play the violin. 🎻", "i was once TIME's person of the year (2006). 📰", "i have two dogs. 🐶"]; // List some facts
</script>

<div class="container">
    <h1>About Me</h1>
    <p>Hello, my name is <strong>{name}</strong>!</p>
    <p>{bio}</p>
    <p>My favorite number is <strong>{favoriteNumber}</strong>.</p>

    <h2>My facts</h2>
    <div class="facts">
        {#each facts as fact}
            <div class="fact">{fact}</div>
        {/each}
    </div>
</div>

<style>
    h1 {
        color: #2c3e50;
        font-family: Arial, sans-serif;
    }
    .container {
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
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
</style>
