<script>
    import Logo from "./logo.svelte";
    import Link from "./link.svelte";
    import lupa from "../lupa.svelte";
</script>

<header>
    <Logo />
    <nav>
        <strong><Link text="Inici" /> </strong>
        <strong><Link text="Pel·lícules" /></strong>
        <strong><Link text="Sèries" /></strong>
        <strong><Link text="Col·leccions" /></strong>
        <strong><Link text="Festivals" /></strong>
        <strong><Link text="Kids" /></strong>
        <strong><Link text="Més" /></strong>
    </nav>

    <img src={lupa} alt="imagen de lupa" />
</header>

<style>
    header {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        margin: 20px 40px;
        gap: 20px;
    }
p{
    color: white;
}
</style>
