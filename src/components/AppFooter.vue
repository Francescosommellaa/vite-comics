<script>

export default {
    name: "AppFooter",

    data() {
        return {
            topFooterItems: [
                {
                    img: "../public/img/buy-comics-digital-comics.png",
                    title: 'DIGITAL COMICS'
                },
                {
                    img: '../public/img/buy-comics-merchandise.png',
                    title: 'DC MERCHANDISE'
                },
                {
                    img: '../public/img/buy-comics-subscriptions.png',
                    title: 'SUBSCRIPTION'
                },
                {
                    img: '../public/img/buy-comics-shop-locator.png',
                    title: 'COMIC SHOP LOCATOR'
                },
                {
                    img: '../public/img/buy-dc-power-visa.svg',
                    title: 'DC POWER VISA'
                },
            ],

            DcComicsItems: [
                {
                    link: 'characters'
                    
                },
                {
                    link: 'characters'
                },
                {
                    link: 'characters'
                },
                {
                    link: 'characters'
                },
                {
                    link: 'characters'
                },
                {
                    link: 'characters'
                },
                {
                    link: 'characters'
                },
            ]
        }

    }
}

</script>

<template>
    <div class="top-nav">
        <ul class="">
            <li v-for="(item, index) in topFooterItems">
                <img :src="(item.img)" alt="Immagine" />
                <h5>{{ item.title }}</h5>
            </li>
        </ul>
    </div>

    <div class="footer">
        <div class="link-utili">
            <div>
                <h3>DC COMICS</h3>
                <ul v-for="(item, index) in DcComicsItems">
                    <li>
                        <a href="#">{{ item.link }}</a>
                    </li>
                </ul>
                <h3>SHOP</h3>
                <ul v-for="(item, index) in DcComicsItems">
                    <li>
                        <a href="#">{{ item.link }}</a>
                    </li>
                </ul>
            </div>

            <div>
                <h3>DC</h3>
                <ul v-for="(item, index) in DcComicsItems">
                    <li>
                        <a href="#">{{ item.link }}</a>
                    </li>
                </ul>
            </div>

            <div>
                <h3>DC</h3>
                <ul v-for="(item, index) in DcComicsItems">
                    <li>
                        <a href="#">{{ item.link }}</a>
                    </li>
                </ul>
            </div>
        </div>
        <div>
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
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
            gap: 0.4em;

            img {
            height: 36px;
            max-width: 36px;
            }
        }
    }

}

.footer {
    max-height: 400px;
    background-image: url(../assets/img/footer-bg.jpg);
    width: 100%;
    color: white;
    @include center(orizzontal);
    justify-content: space-around;
    overflow: hidden;

    .link-utili {
        @include center(orizzontal);

        li {
            list-style: none;
            
            a {
                color: white;
                text-decoration: none
            }
        }
    };
}

</style>