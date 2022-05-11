<script>
    let imageElement
    let interacting = false;
    let currentImage = "./normal-nathan-component.png";
    let imageClass = "imgInactive";
    function handleClick(event) {
        if(event.target == imageElement) {
            interacting = true;
            imageClass = "imgActive";
        }
        else {
            interacting = false;
            imageClass = "imgInactive";
        }
    }

    function handleKeypress(event){
        if(interacting){
            if(event.code == 'ArrowUp'){
                let audio = document.createElement('audio');
                currentImage = "./normal-nathan-component.png";
                audio.src = "./metal-clap.wav";
                audio.play();
                audio.remove();
            } else if (event.code == 'ArrowDown'){
                let audio = document.createElement('audio');
                currentImage = "./compressed-nathan-component.png";
                audio.src = "./crunch.wav";
                audio.play();
                audio.remove();
            }
        }
    }
</script>

<svelte:window on:click={handleClick} on:keydown={handleKeypress}/>

<div class = "container">
    <img 
    bind:this={imageElement}
    alt="CRUNCH HIM!"
    src= {currentImage}
    class= {imageClass}
/>
</div>

<style>
    .imgInactive {
        width: 20%;
        height: auto;
        outline: 4px solid rgb(89, 101, 114);
        outline-offset: -4px;
        filter: drop-shadow(15px 15px 4px rgb(167, 192, 216));
    }
    .imgActive {
        width: 20%;
        height: auto;
        outline: 4px solid rgb(114, 89, 89);
        outline-offset: -12px;
        filter: drop-shadow(10px 10px 2px rgb(216, 167, 167));
    }
    .container {
        margin: 2%;
        display: flex;
    }
</style>