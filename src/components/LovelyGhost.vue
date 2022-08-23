<template>
    <div id="container">
        <div>
            <img class="ghost" src="../assets/ghost.svg" alt="">
        </div>
        <div class="shadowFrame">
            <img class="shadow" src="../assets/shadow.svg" alt="">
        </div>
    </div>
</template>



<style lang="scss" scoped>
#container {
    // background-color: red;
    position: relative;
    top: 50%;

}

.ghost {
    width: 300px;
    animation: float 3s ease-out infinite;
}

@keyframes float {
    50% {
        transform: translate(0, 20px);
    }
}

.shadowFrame {
    width: 260px;
    margin-top: 15px;
    display:inline-block;
}


.shadow {
    animation: shrink 3s ease-out infinite;
    transform-origin: center center;

    ellipse {
        transform-origin: center center;
    }
}

@keyframes shrink {
    0% {
        width: 90%;
        margin: 0 5%;
    }

    50% {
        width: 60%;
        margin: 0 18%;
    }

    100% {
        width: 90%;
        margin: 0 5%;
    }
}
</style>
