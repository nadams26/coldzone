<script>
    let imageElement
    let interacting = false;
    let currentImage = "./AA.png";
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
            if(event.code == 'ArrowLeft'){
                let audio = document.createElement('audio');
                currentImage = "./AA.png";
                audio.src = "./AA.wav";
                audio.play();
                audio.remove();
            } else if (event.code == 'ArrowUp'){
                let audio = document.createElement('audio');
                currentImage = "./EE.png";
                audio.src = "./EE.wav";
                audio.play();
                audio.remove();
            } else if (event.code == 'ArrowRight'){
                let audio = document.createElement('audio');
                currentImage = "./OO.png";
                audio.src = "./OO.wav";
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
        alt="AAEEOO"
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
        width: 30%;
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