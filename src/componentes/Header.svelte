<script>
    import Logo from "./logo.svelte";
    import Link from "./link.svelte";
</script>

<header>
    <Logo />
    <nav>
        <Link text="Inici" />           
        <Link text="Pel·lícules" />
        <Link text="Sèries" />
        <Link text="Col·leccions" />
        <Link text="Festivals" />
        <Link text="Kids" />
        <Link text="Més" />
    </nav>
</header>

<style>
header{
    display: flex;
    justify-content: flex-start;
    align-items: center;
    margin: 20px 40px;
    gap: 20px; 
}
</style>