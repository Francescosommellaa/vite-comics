<script>

export default {
    name: "AppHeader",
}

</script>

<template>
    <div id="app" class="container">
        <img src="..//assets/img/dc-logo.png" alt="logo DC Header">
        <ul>
            <li v-for="(item, index) in menuItems" :key="index" @click="toggleActive(index)">
                {{ item.label }}
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>

</style>