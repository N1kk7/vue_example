<template>
    <!--loader start-->
    <div id="loading" class="hide">
        <div id="loading-center">
            <div id="loading-center-absolute">
                <div class="object" id="object_one"></div>
                <div class="object" id="object_two"></div>
                <div class="object" id="object_three"></div>
            </div>
        </div>
        <!--loader end-->
    </div>
</template>

<script>
export default {
    name: 'LoaderComponent'
}
</script>

<style lang="scss" scoped>
#loading {
    background-color: #374140;
    height: 100%;
    width: 100%;
    position: fixed;
    z-index: 101;
    margin-top: 0;
    top: 0;
    -webkit-transition:
        opasity 0.3s linear,
        z-index 0.1s linear 0.3s;
    -o-transition:
        opasity 0.3s linear,
        z-index 0.1s linear 0.3s;
    transition:
        opasity 0.3s linear,
        z-index 0.1s linear 0.3s;
}

#loading.hide {
    z-index: -1;
    opacity: 0;
}

#loading-center {
    width: 100%;
    height: 100%;
    position: relative;
}

#loading-center-absolute {
    position: absolute;
    left: 50%;
    top: 50%;
    height: 150px;
    width: 150px;
    margin-top: -75px;
    margin-left: -75px;
}

.object {
    width: 20px;
    height: 20px;
    background-color: #fff;
    float: left;
    margin-right: 20px;
    margin-top: 65px;
    -webkit-border-radius: 50% 50% 50% 50%;
    border-radius: 50% 50% 50% 50%;
}

#object_one {
    -webkit-animation: object_one 1.5s infinite;
    animation: object_one 1.5s infinite;
}

#object_two {
    -webkit-animation: object_two 1.5s infinite;
    animation: object_two 1.5s infinite;
    -webkit-animation-delay: 0.25s;
    animation-delay: 0.25s;
}

#object_three {
    -webkit-animation: object_three 1.5s infinite;
    animation: object_three 1.5s infinite;
    -webkit-animation-delay: 0.5s;
    animation-delay: 0.5s;
}

@-webkit-keyframes object_one {
    75% {
        -webkit-transform: scale(0);
    }
}

@keyframes object_one {
    75% {
        transform: scale(0);
        -webkit-transform: scale(0);
    }
}

@-webkit-keyframes object_two {
    75% {
        -webkit-transform: scale(0);
    }
}

@keyframes object_two {
    75% {
        transform: scale(0);
        -webkit-transform: scale(0);
    }
}

@-webkit-keyframes object_three {
    75% {
        -webkit-transform: scale(0);
    }
}

@keyframes object_three {
    75% {
        transform: scale(0);
        -webkit-transform: scale(0);
    }
}
</style>
