<script>
    export let show = true;
</script>

<div class="content" style="display: {show ? 'block' : 'none'}">
    <h1>Welcome to Your Game Development Company</h1>
    <p>Crafting immersive experiences for gamers worldwide.</p>
</div>

<style>
    .content {
        text-align: center;
        max-width: 800px;
        opacity: 0;
        transform: translateY(20px);
        animation: fadeInUp 1s ease forwards;
        transition: opacity 0.5s ease, transform 0.5s ease;
    }

    @keyframes fadeInUp {
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
</style>
