<script>
    import Navbar from "../components/Navbar.svelte";
    import Footer from "../components/Footer.svelte";
    import Title from "../components/Title.svelte";
</script>

<div class = "body">
    <Navbar/>
    <Title title = "ColdZone" tagline = "sorta-portfolio, sorta-sandbox"/>
    <Footer/>
</div>

<style>
    :global(*) {
        font-family: Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Fira Sans", "Droid Sans", "Helvetica Neue", sans-serif;
    }
</style>
