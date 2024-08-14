<script>
    export let visible = false;
</script>

<div class="projects-section" style="display: {visible ? 'block' : 'none'}">
    <div class="section-title">
        <h1>Projects</h1>
    </div>
    <p>Here is a list of all of our projects!</p>
    <br />
    <div class="project">
        <h2>Shaytris</h2>
        <p>
            Our flagship game, a FOSS Tetris client, with multiplayer, chat, friends
            list and more!
        </p>
        <div class="language-tags">
            <div class="language-tag">TypeScript</div>
            <div class="language-tag">Ruby</div>
            <div class="language-tag">Swift</div>
            <div class="language-tag">Java</div>
        </div>
    </div>
</div>

<style>
    .projects-section {
        width: 100%;
        max-width: 1000px;
        padding: 50px 20px;
        margin-top: 50px;
        opacity: 0;
        transform: translateY(30px);
        display: none;
        transition: opacity 0.5s ease, transform 0.5s ease;
    }
</style>
