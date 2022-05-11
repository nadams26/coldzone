<script>
    export let title = "";
    export let tagline = "";
</script>

<div class = "title">
    <h1 class = "titleHeader">
        <span class = "titleText">
            {title}
        </span>
    </h1>
    <div class = "tagline">
        <i>{tagline}</i>
    </div>
</div>

<style>
    .title {
        margin-left: 2%;
        margin-bottom: 2%;
    }
    .titleText {
        background: -webkit-linear-gradient(315deg,#af90e0 25%,#647eff);
        background-clip: text;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        font-size: 200%;
    }
    .titleHeader, .tagline {
        display: inline;
    }
    .tagline {
        margin-left: 0.5%;
    }
</style>