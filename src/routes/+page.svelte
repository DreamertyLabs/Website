<script>
    import Navbar from './components/Navbar.svelte';
    import Content from './components/Content.svelte';
    import Projects from './components/Projects.svelte';

    let showProjects = false;

    const handleShowProjects = () => {
        showProjects = true;
    };
</script>

<main class="{showProjects ? 'light-mode' : 'dark-mode'}">
    <Content show={!showProjects} />
    <Projects visible={showProjects} />
    <Navbar on:showProjects={handleShowProjects} />
</main>

<style>
    main {
        transition: background-color 0.5s ease, color 0.5s ease;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 100vh;
        overflow-x: hidden;
    }

    .light-mode {
        background-color: var(--background-color-light);
        color: var(--text-color-light);
    }

    .dark-mode {
        background-color: var(--background-color-dark);
        color: var(--text-color-dark);
    }

    :root {
        --background-color-light: #1e66f5;
        --background-color-dark: #121212;
        --text-color-light: #ffffff;
        --text-color-dark: #f0f0f0;
        --accent-color: #00bcd4;
    }
</style>
