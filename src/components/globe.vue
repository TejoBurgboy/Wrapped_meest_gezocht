<template>
    <h3>
        Bezoekersvanuit
    </h3>
    <div class="landenAantal">108 landen</div>
    <div class="countryInfo">
        <h5>Top 3 landen</h5>
        <div class="countrySpecific" v-for="country in myJson" v-show="country.afk" :id="['land' + country.id]">
            <span class="mostCountryViews"> {{ country.id }}</span>
            <div class="bezoekers">{{ country.Bezoekers }} Bezoekers Uit</div>
            <div class="landinfo">
                <img class="vlag" :src='country.vlag'>
                <span class="landNaam">{{ country.land }}</span>
                <span id="stijgdaal" class="cstijg" v-if="country.trentPrecentage > 0"> +{{ country.trentPrecentage
                }}%
                </span>
                <span id="stijgdaal" class="cdaal" v-if="country.trentPrecentage < 0"> {{ country.trentPrecentage }}%
                </span>
            </div>
        </div>
    </div>
    <div id="myearth" class="earth-container"></div>
</template>
<style>
#myearth::after {
    background: radial-gradient(ellipse at center, rgba(5, 57, 89, 0.7) 0%, rgba(5, 57, 89, 0.55) 20%, rgba(5, 57, 89, 0.2) 40%, rgba(5, 57, 89, 0.1) 50%, rgba(5, 57, 89, 0.02) 60%, rgba(5, 57, 89, 0) 70%, rgba(5, 57, 89, 0) 100%);
}

.countryGuests {
    position: relative;
    margin: -1em 0 0 -1em;
    width: 2em;
    height: 2em;
    border: 2px #FFFFFF solid;
    border-radius: 50%;
    box-sizing: border-box;

    pointer-events: all;
    cursor: pointer;
    transition: font-size 0.2s ease, background-color 0.2s ease;
    display: flex;
}

.countryGuests:hover {
    font-size: 2em;
    margin: -1.5em 0 0 -1.5em;
    width: 3em;
    height: 3em;
    background-color: RGBA(0, 0, 0, 0.5);
}

.countryGuests span {
    position: absolute;
    top: 50%;
    left: 10%;
    width: 80%;
    transform: translateY(-50%);
    text-align: center;
    color: white;
    font-size: 0.5em;
    opacity: 0;
    transition: opacity 0.2s ease;
}

.countryGuests:hover span {
    opacity: 1;
}
</style>

<script>
import { Suspense } from 'vue'
import json from '../assets/countrydata'
//import {globe} from "../assets/miniature.earth"

export default {
    name: 'globe',
    data() {
        return {
            myJson: json,
            mapstiles: null,
            legearray: [],
            nontop3: null,
            legerearray: [],
            globestyle: null,
            countrybes: [],
            countryla: [],
            countryls: [],
            countryfor: null,
        }
    },
    mounted() {
        this.highlighting()
        this.highlight()
        this.combine()
        this.countrynav()
        
        var myearth = new Earth("myearth", {
            location: { lat: 22.5, lng: 20 },
            autoRotate: true,
            //mapLandColor: '#FFFFE2',
            mapLandColor: '#FFD074',
            //mapSeaColor: '#0E87CC',
            mapSeaColor: '#00BFBF',
            //mapStyles: this.nontop3,
            //mapStyles: this.mapstiles,
            mapStyles: this.globestyle,
            mapBorderColor: "gray",
        });

        console.log(this.myJson)
        for (let country of this.myJson) {
            var myoverlay = myearth.addOverlay({
                content: '<span>' + country.Bezoekers + " Bezoekers" + '</span>',
                location: { lat: country.Lat, lng: country.Lng },
                className: 'countryGuests',
                depthScale: 0.33,
            });
        };

        myoverlay.addEventListener('mouseover', myearth => {
            autoRotate: false
        })

        myoverlay.addEventListener('mouseout', myearth => {
            autoRotate: true
        })




        //this.addOverlay ({
        //content: country.Bezoekers,
        //location: { lat: country.Lat, lng: country.Lng },
        //className : 'my-text-overlay'

        //});
    },
    methods: {
        countrynav() {
            for (let country of this.myJson) {
                this.countrybes.push(country.Bezoekers)
            }
        },
        highlight() {
            for (let country of this.myJson) {
                this.mapstiles += country.afk
                this.legearray.push('#' + country.afk)
                console.log(country.afk)
            }
            this.mapstiles = this.legearray.join() + "{ fill: #567d46}"
        },
        highlighting() {
            for (let country of this.myJson) {
                this.nontop3 += country.non3afk
                this.legerearray.push('#' + country.non3afk)
                console.log(country.non3afk)
            }
            this.nontop3 = this.legerearray.join() + "{ fill: #F55D8C}"
        },
        combine() {
            this.globestyle = this.nontop3 + this.mapstiles
            //console.log(globestyle)
        },
    }
}
</script>

