<template>
    <svg v-if="menusite == false" @click="menuactive" width="34px" height="25px" viewBox="0 0 34 25" version="1.1"
        xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <title>Group 13</title>
        <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
            <g id="001a_Home_v7" transform="translate(-30.000000, -40.000000)" fill="#FFFFFF">
                <g id="Group-13" transform="translate(30.000000, 40.000000)">
                    <rect id="Rectangle-Copy-4" x="0" y="20" width="34" height="5"></rect>
                    <rect id="Rectangle-Copy-5" x="0" y="10" width="34" height="5"></rect>
                    <rect id="Rectangle-Copy-6" x="0" y="0" width="34" height="5"></rect>
                </g>
            </g>
        </g>
    </svg>
    <div v-if="menusite == true" @click="menudeactive" class="deactiveMenu">X</div>
    <div v-if="menusite == false">

    </div>
    <div v-if="menusite == true" class="menu">
        <button class="menuItem">Aantal Bezoekers</button>
        <button class="menuItem">Gebruikte Apparaten</button>
        <button class="menuItem">Meest bezochte pagina,s</button>
        <button class="menuItem">Bezoekers per land</button>
        <button class="menuItem">Browsers Gebruik</button>
        <button class="menuItem">Snelheid van jou website</button>
        <button class="menuItem">Topkanalen</button>
        <button class="menuItem">Gebeurtenissen</button>
    </div>
</template>
<style>
.deactiveMenu {
    font-size: 200%;
    color: white;
}

.menu {
    position: absolute;
    top: 200%;
    left: 10%;
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    z-index: 100;
    width: 80%;
}

.menuItem {
    border: black solid 1px;
    width: 25%;
    padding: 4% 0 4% 0;
    margin: 1% 3% 1% 3%;
    color: white;
    border-radius: 4ch;
    background-color: black;
}
</style>
<script>
export default {
    name: 'hamburgermenu',
    data() {
        return {
            menusite: false,
            blurClass: null
        }
    },
    created() {
        console.log(this.menusite)
    },
    methods: {
        menuactive() {
            this.menusite = true
            this.blurClass = 'blur'
            console.log(this.menusite)
            console.log(this.blurClass)
            this.$emit('updateBlur', this.blurClass);
        },
        menudeactive() {
            this.menusite = false
            this.blurClass = null
            console.log(this.menusite)
            console.log(this.blurClass)
            this.$emit('updateBlur', this.blurClass);
        },
    }
}
</script>
