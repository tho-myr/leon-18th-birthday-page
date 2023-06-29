<script>
    import { onMount } from "svelte";

    onMount(() => {
        const faceContainer = document.getElementById("face-container");
        const videoContainer = document.getElementById("video-container");
        const face = document.getElementById("face");
        const rickroll = document.getElementById("rickroll");

        if (face != null && faceContainer != null && videoContainer != null && rickroll != null) {
            face.onclick = (event) => {
                // window.location.href =
                //     "https://shattereddisk.github.io/rickroll/rickroll.mp4";
                faceContainer.remove();
                videoContainer.style.visibility = 'visible';
                rickroll.play();
            };
        }
    });
</script>

<main>
    <div class="flex-container" id="face-container">
        <img
            id="chat-bubble"
            src="chat-bubble.svg"
            alt="Punch Leon to win a suprise gift!"
        />
        <img id="face" src="face.png" alt="Wunderschoenes Gesicht von Leon" />
        <div class="text-container headline">Happy Birthday Leon</div>
        <div class="text-container emoji">(ɔ◔‿◔)ɔ ♥</div>
    </div>
    <div class="flex-container" id="video-container">
        <video id="rickroll" height="50%" src="rickroll.mp4">
            <track kind="captions" />
        </video>
        <div class="text-container headline">jk u just got rickrolled</div>
        <div id="dancing-emoji" class="text-container emoji">
            ┏(-_-)┛┗(-_- )┓
        </div>
    </div>
</main>

<style>
    main,
    .flex-container {
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
    #chat-bubble {
        opacity: 0%;
        animation: blink 1s linear infinite;
        animation-delay: 1s;
    }
    #face {
        height: 50%;
        cursor: pointer;
        animation: spin 4s infinite linear;
        -webkit-animation: spin 4s infinite linear;
    }
    .text-container {
        font-size: min(5.5vw, 70px);
        font-weight: 800;
        color: white;
    }
    .headline {
        animation: flyInLeft 3s;
        -webkit-animation: flyInLeft 3s;
        -webkit-text-fill-color: transparent;
        -webkit-text-stroke: 0.5px;
    }
    .emoji {
        animation: flyInRight 3s;
        -webkit-animation: flyInRight 3s;
    }
    #video-container {
        visibility: hidden;
        width: 80%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    @-moz-keyframes spin {
        from {
            -moz-transform: rotate(0deg);
        }
        to {
            -moz-transform: rotate(360deg);
        }
    }
    @-webkit-keyframes spin {
        from {
            -webkit-transform: rotate(0deg);
        }
        to {
            -webkit-transform: rotate(360deg);
        }
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

    @keyframes blink {
        50% {
            opacity: 100%;
        }
    }
</style>
