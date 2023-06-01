<script>
</script>

<main>
    <div class="flex-container">
        <img id="face" src="face.png" alt="Wunderschoenes Gesicht von Leon">
        <div id="headline" class="text-container">Happy Birthday Leon</div>
        <div id="emoji" class="text-container">(ɔ◔‿◔)ɔ ♥</div>
    </div>
</main>


<style>
    main, .flex-container {
        width: 100%;
        height: 100%;
        overflow: hidden;
    }
    .flex-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    #face {
        height: 50%;
        animation: spin 4s infinite linear;
        -webkit-animation: spin 4s infinite linear;
    }
    .text-container {
        font-size: min(5.5vw, 70px);
        font-weight: 800;
        color: white;
    }
    #headline {
        animation: flyInLeft 3s;
        -webkit-animation: flyInLeft 3s;
        -webkit-text-fill-color: transparent;
        -webkit-text-stroke: 0.5px;
    }
    #emoji {
        animation: flyInRight 3s;
        -webkit-animation: flyInRight 3s;
    }

    @-moz-keyframes spin {
    from { -moz-transform: rotate(0deg); }
    to { -moz-transform: rotate(360deg); }
    }
    @-webkit-keyframes spin {
        from { -webkit-transform: rotate(0deg); }
        to { -webkit-transform: rotate(360deg); }
    }
    @keyframes spin {
        0% {
            transform: rotate(0deg) scale(40%);
        }
        50% {
            transform: rotate(180deg) scale(100%);
        }
        100% {
            transform: rotate(360deg) scale(40%);
        }
    }

    @keyframes flyInRight {
        0% {
            transform: translateX(150%);
        }
        100% {
            transform: translateX(0%);
        }
    }
    @keyframes flyInTop {
        0% {
            transform: trnslate(150%);
        }
        100% {
            transform: translateX(0%);
        }
    }
    @keyframes flyInLeft {
        0% {
            transform: translateX(-150%);
        }
        100% {
            transform: translateX(0%);
        }
    }
</style>