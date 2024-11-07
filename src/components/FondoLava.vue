<script>
</script>
<template>
    <svg preserveAspectRatio="xMidYMid slice" viewBox="0 0 100 100">
        <defs>
        </defs>
        <!-- Partículas de lava modificadas y duplicadas para un efecto con más cantidad y menor tamaño -->
        <path fill="#4a90e2" class="out-top"
            d="M37-5C25.1-14.7,5.7-19.1-9.2-10-28.5,1.8-32.7,31.1-19.8,49c15.5,21.5,52.6,22,67.2,2.3C59.4,35,53.7,8.5,37-5Z" />
        <path fill="#50a5f1" class="in-top"
            d="M20.6,4.1C11.6,1.5-1.9,2.5-8,11.2-16.3,23.1-8.2,45.6,7.4,50S42.1,38.9,41,24.5C40.2,14.1,29.4,6.6,20.6,4.1Z" />
        
        <!-- Duplicados y escalados para más partículas pequeñas -->
        <path fill="#1e90ff" class="out-bottom-small"
            d="M50,35c-6.4-4.2-15.3-2.4-20.6,0.4-10.5,6.8-16.9,27.3-8.6,39s28.8,8.1,34.2-3c3.4-8.3,0.8-19.4-1-27.2C58.8,41.3,57.3,37.6,50,35Z" />
        <path fill="#87cefa" class="in-bottom-small"
            d="M60,47c-5.6-3.5-12.7-1.7-17,1.1-8.9,6.1-11.4,21.4-4.4,27.2s20.4,2.2,25.3-7C70.6,60.3,69.8,51.6,60,47Z" />
        
        <path fill="#4a90e2" class="out-top-small"
            d="M80,20c-5.1-3.3-12.2-1.6-16.2,1.1-8.4,5.8-10.9,20.4-4.2,25.9s19,2.1,23.5-6C91.6,31.6,90.8,24.3,80,20Z" />
        <path fill="#50a5f1" class="in-top-small"
            d="M70,30c-4.6-2.9-10.6-1.4-14,0.9-7.1,4.7-9.1,16.6-3.5,21.1s15.7,1.8,19.4-5C79.4,39.2,78.8,33.5,70,30Z" />
    </svg>
</template>

<style scoped>
@keyframes rotate {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

/* Animaciones para las partículas originales */
.out-top {
    animation: rotate 20s linear infinite;
    transform-origin: 13px 25px;
}
.in-top {
    animation: rotate 55s linear infinite;
    transform-origin: 13px 25px;
}
.out-bottom {
    animation: rotate 25s linear infinite;
    transform-origin: 84px 93px;
}
.in-bottom {
    animation: rotate 15s linear infinite;
    transform-origin: 84px 93px;
}

/* Nuevas clases para partículas adicionales y más pequeñas */
.out-top-small {
    animation: rotate 30s linear infinite;
    transform-origin: 70px 80px;
    scale: 0.6;
}

.in-top-small {
    animation: rotate 45s linear infinite;
    transform-origin: 25px 15px;
    scale: 0.5;
}

.out-bottom-small {
    animation: rotate 35s linear infinite;
    transform-origin: 55px 60px;
    scale: 0.4;
}

.in-bottom-small {
    animation: rotate 25s linear infinite;
    transform-origin: 40px 70px;
    scale: 0.5;
}

svg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 95%;
    z-index: -1;
    border-radius: 5px;
}
</style>
