<script>
    import "./styles.css";
    let { children } = $props();
</script>

<nav>
    <img src="/src/routes/Logo.png" alt="Logo" class="logo">
    <a href="/">Home</a>
    <a href="/contact">Contact</a>
    <a href="/mountainhuts">Mountainhuts</a>
</nav>

{@render children()}