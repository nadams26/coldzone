<script>
    import AAEEOO from '../components/AAEEOO.svelte';
    import CRUNCH_HIM from '../components/CRUNCH_HIM.svelte';
    import Navbar from "../components/Navbar.svelte";
    import Footer from "../components/Footer.svelte";
    import Title from "../components/Title.svelte";
</script>

<div class = "body">
    <Navbar/>
    <Title title = "The Hall of Components" tagline = "Cerne simiam illam, ridiculam est"/>
    <div class = "content">
        <AAEEOO/>
        <CRUNCH_HIM/>
    </div>
    <Footer/>
</div>

<style>
</style>
