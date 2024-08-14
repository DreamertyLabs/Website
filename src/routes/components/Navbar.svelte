<script>
    export let darkMode = true;

    const toggleMode = () => {
        darkMode = !darkMode;
    };
</script>

<nav class={`navbar ${darkMode ? 'dark-mode' : 'light-mode'}`}>
    <a href="/">Home</a>
    <a href="#" on:click|preventDefault={() => $emit('showProjects')}>Projects</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
</nav>

<style>
    .navbar {
        position: fixed;
        bottom: 30px;
        display: flex;
        justify-content: center;
        gap: 20px;
        padding: 10px 20px;
        border-radius: 30px;
        background-color: rgba(30, 30, 30, 0.8);
        backdrop-filter: blur(10px);
        box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.3);
        transition: background-color 0.3s ease, box-shadow 0.3s ease;
    }

    .navbar:hover {
        background-color: rgba(30, 30, 30, 1);
        box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.5);
    }

    .navbar a {
        text-decoration: none;
        font-size: 1.2em;
        color: #f0f0f0;
        position: relative;
        padding: 5px 0;
        transition: color 0.3s ease;
    }
</style>
