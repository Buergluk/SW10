<script>
    import "./styles.css";
    let { children } = $props();
</script>

<nav>
    <a href="/">Home</a>
    <a href="/contact">Contact</a>
    <a href="/mountainhuts">Mountainhuts</a>
</nav>

{@render children()}