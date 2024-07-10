<script>

export default {
    name: "AppFooter",

    data() {
        return {
            topFooteritems: [
                {
                    img: "../assets/img/buy-comics-digital-comics.png",
                    title: 'DIGITAL COMICS'
                },
                {
                    img: '../assets/img/buy-comics-merchandise.png',
                    title: 'DIGITAL COMICS'
                },
                {
                    img: '../assets/img/buy-comics-subscriptions.png',
                    title: 'DIGITAL COMICS'
                },
                {
                    img: '../assets/img/buy-comics-shop-locator.png',
                    title: 'DIGITAL COMICS'
                },
                {
                    img: '../assets/img/buy-dc-power-visa.svg',
                    title: 'DIGITAL COMICS'
                },
            ]
        }

    }
}

</script>

<template>
    <div class="top-nav">
        <ul class="">
            <li v-for="(item, index) in topFooteritems">
                <img :src="(item.img)" alt="Immagine" />
                <h5>{{ item.title }}</h5>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as * ;
@use '../styles/partials/variables' as * ;

.top-nav{
    @include center(vertical);
    height: 100px;
    background-color: #0582F9;
    color: rgba(255, 255, 255, 0.692);

    ul {
    @include center();
    gap: 20px;

    li {
        @include center();

        img {
            height: 40px;
        }
    }
}

}

</style>