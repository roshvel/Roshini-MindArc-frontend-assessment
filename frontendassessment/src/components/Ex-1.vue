<template>
    <div id="wrapper" class="w-100">
        <div id="hello-developer" class="w-100 d-flex flex-column justify-content-center text-white mb-5">
            <h1 class="text-bold">Hello Developer!</h1>
            <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit</h3>
        </div>
        <div id="cards-wrapper" class="px-5 d-flex flex-column flex-sm-row justify-content-center">
            <div class="card mx-4 mb-3" style="width: 18rem;" v-for="(c, i) in cards" :key="`card-${i + 1}`">
                <img class="card-img-top" :src="require(`@/assets/${c.src}`)" alt="Card image cap">
                <div class="card-body">
                    <p class="card-text">{{ c.text }}</p>
                </div>
                <div class="card-footer">
                    <button type="button" style="width: 8rem; margin: 0px auto;  background-color: Transparent; color: black; border-radius: 25px; font-weight:bold; border-width: medium; "
                        class="btn btn-primary btn-sm btn-block text-bold  border-dark cursor-pointer"
                        onclick="location.href = '';">READ MORE
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            cards: [
                {
                    name: 'card 1',
                    src:"` https://via.placeholder.com/400x300`",
                    // src: '400x300.png',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
                },
                {
                    name: 'card 2',
                    src: "` https://via.placeholder.com/400x300`",
                    // src: '400x300.png',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
                },
                {
                    name: 'card 3',
                    src:"` https://via.placeholder.com/400x300`",
                    // src: '400x300.png',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.'
                }
            ]
        }
    }
}
</script>

<style scoped>
#hello-developer {
    background-repeat: no-repeat;
}

@media only screen and (max-width: 1920px) {
    #hello-developer {
        height: 650px;
        justify-items: center;
        align-items: center;
        background-image: url("https://via.placeholder.com/1920x650")
        /* background-image: url('../assets/1920x650.png') */
    }
}

@media only screen and (max-width: 600px) {
    #hello-developer {
        height: 600px;
        justify-items: center;
        align-items: center;
        background-image: url("https://via.placeholder.com/600x600")
        /* background-image: url('../assets/600x600.png') */
    }
}
</style>