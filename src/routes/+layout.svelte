<script lang="ts">
    import githubLogoSvg from '$lib/images/github.svg';
    import '../app.css';

    let { children } = $props();
</script>

<div class="app">
    <main>
        {@render children()}
    </main>

    <footer>
        <p>
            Made with Svelte | Made by <a href="https://github.com/simon-b64">Simon B.<img src={githubLogoSvg} alt="GitHub" /></a>
        </p>
    </footer>
</div>

<style>
    .app {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    main {
        display: flex;
        flex-grow: 1;
        flex-direction: column;
        padding: 1rem;
        width: 100%;
        max-width: 64rem;
        margin: 0 auto;
        box-sizing: border-box;
    }

    footer {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 12px;
    }

    footer a {
        font-weight: bold;
        display: inline-flex;
        justify-content: center;
        align-items: center;
        gap: 0.2rem;
    }

    footer a img {
        height: 1.5rem;
    }

    @media (min-width: 480px) {
        footer {
            padding: 12px 0;
        }
    }
</style>
