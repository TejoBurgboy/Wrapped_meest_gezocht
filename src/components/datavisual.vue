<template>
    <div class="bestbekekenfotos">
        <img class="sitescreenshot" @mouseover="hover(foto)" @mouseleave="unhover" v-for="foto in myJson"
            :id="['pic' + foto.id]" :src='foto.image' :alt="foto.title">
    </div>
    <p id="nummer" v-if="currentfoto">
        {{ currentfoto.id }}</p>
    <div class="fotoinfo" v-if="currentfoto">
        <h4 id="fototitel"> {{ currentfoto.title }} </h4>
        <a :href="currentfoto.url" class="sitelink"> {{ currentfoto.url }} </a>
        <div class="weergaven">
            <div id="peoplesvg">
                <svg width="17px" height="25px" viewBox="0 0 16 21" version="1.1" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink">
                    <title>Group 18 Copy</title>
                    <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                        <g id="004a_Meest_Bezochte_Pagina's_v7" transform="translate(-926.000000, -870.000000)"
                            stroke="#3C3D46" stroke-width="1.5">
                            <g id="Group-17" transform="translate(926.000000, 858.000000)">
                                <g id="Group-18-Copy" transform="translate(0.000000, 12.000000)">
                                    <path
                                        d="M10,12.75 C11.4497475,12.75 12.7622475,13.3376263 13.7123106,14.2876894 C14.6623737,15.2377525 15.25,16.5502525 15.25,18 L15.25,20.25 L0.75,20.25 L0.75,18 C0.75,16.5502525 1.33762627,15.2377525 2.2876894,14.2876894 C3.23775253,13.3376263 4.55025253,12.75 6,12.75 Z"
                                        id="Rectangle"></path>
                                    <ellipse id="Oval" cx="8" cy="5.25" rx="4.58333333" ry="4.5"></ellipse>
                                </g>
                            </g>
                        </g>
                    </g>
                </svg>
            </div>
            <div class="aantalWeergaven">{{ currentfoto.visitors }} </div>
            <div id="stijgdaal" class="stijg" v-if="currentfoto.trentPrecentage > 0"> +{{ currentfoto.trentPrecentage }}%
            </div>
            <div id="stijgdaal" class="daal" v-if="currentfoto.trentPrecentage < 0"> {{ currentfoto.trentPrecentage }}%
            </div>
        </div>
    </div>
</template>

<script>
import { gsap } from "gsap";
import json from '../assets/data.json'
export default {
    name: 'datavisual',
    data() {
        return {
            myJson: json,
            currentfoto: null
        }
    },
    created() {
        console.log(this.myJson)
    },
    methods: {
        hover(foto) {
            gsap.to(event.currentTarget, 1, { y: -150 });
            this.currentfoto = foto
            console.log(foto)
        },
        unhover() {
            gsap.to(event.currentTarget, 1, { y: 0 });
            currentfoto = null
        }
    }
}
</script>