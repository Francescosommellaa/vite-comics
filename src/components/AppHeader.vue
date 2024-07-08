<script>

export default {
    name: "AppHeader",

    data() {
        return {
            menuItems: [
                { 
                    label: 'CHARACTERS', 
                    url: '#',
                    active: false 
                },
                { 
                    label: 'COMICS',
                    url: '#',
                    active: true 
                },
                { 
                    label: 'MOVIES',
                    url: '#',
                    active: false 
                },
                { 
                    label: 'TV', 
                    url: '#',
                    active: false 
                },
                {  
                    label: 'GAMES', 
                    url: '#',
                    active: false 
                },
                { 
                    label: 'COLLECTIBLES', 
                    url: '#',
                    active: false 
                },
                { 
                    label: 'VIDEOS',
                    url: '#',
                    active: false 
                },
                { 
                    label: 'FANS', 
                    url: '#',
                    active: false 
                },
                { 
                    label: 'NEWS', 
                    url: '#',
                    active: false 
                },
                { 
                    label: 'SHOP', 
                    url: '#',
                    active: false 
                },
            ],
        };
    },
};

</script>

<template>
    <div class="container">
        <img src="..//assets/img/dc-logo.png" alt="logo DC Header">
        <ul>
            <li v-for="(item, index) in menuItems" :key="index" @click="toggleActive(index)">
                <a>{{ item.label }}</a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as * ;
@use '../styles/partials/variables' as * ;

.container {
    @include center(orizzontal);
    justify-content: space-between;

    ul {
        @include center(orizzontal);
        height: 100px;

        li {
            list-style: none;
            height: 100%;

            &:active {
                padding: 1em 0;
                border-bottom: 3px solid $prymary;
            }
            &:hover {
                background-color: #f2f2f2;
            }

            a {
                @include center();
                font-weight: 700;
                font-size: 14px;
                height: 100%;
                padding: 0 1em;
            }
        }
    }

    img {
        margin: 2em 0.5em;
        height: 88px;
    }
}
</style>