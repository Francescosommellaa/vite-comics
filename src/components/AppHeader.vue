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
                    active: false },
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
                    tive: false 
                },
                { 
                    label: 'NEWS', 
                    url: '#',
                    tive: false 
                },
                { 
                    label: 'SHOP', 
                    url: '#',
                    tive: false 
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
                {{ item.label }}
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>

ul {
    @include center(orizzontal);

    li {
    list-style: none;
}
}
</style>