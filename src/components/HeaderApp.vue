<script>

export default {
    data() {
        return {
            title: "Yu-Gi-Oh Cards Shop",
            url: "https://toppng.com/uploads/preview/yugioh-logo-yu-gi-oh-11562857421zchdpnt0xu.png"
        }
    }
}
</script>

<template>
    <header class="position-fixed w-100">
        <nav class="navbar bg-white">
            <div class="container-fluid">
                <a class="navbar-brand" href="#">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS5GwPdSWoaAOh53IugMPunkI197X24s8DQiiBka8rHGw&s" alt="Logo"
                        class="d-inline-block align-text-top">
                    {{ title }}
                </a>
            </div>
        </nav>
    </header>
</template>

<style>
header {
    z-index: 99999;
}
img {
    width: 100%;
}
a {
    width: 5rem;
}
</style>
