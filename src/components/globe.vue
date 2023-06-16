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


<script>
import json from '../assets/countrydata'
//import {globe} from "../assets/miniature.earth"

export default {
    name: 'globe',
    data() {
        return {
            myJson: json,
            landenAfkorting: null
        }
    },
    mounted() {
        var myearth = new Earth("myearth", {
            location: { lat: 22.5, lng: 20 },
            mapLandColor: '#333333',
            mapSeaColor: '#DDDDDD',
            mapStyles : "#NL, #BE, #DE { fill: blue; stroke: blue; }",
            mapStyles : "#NL, #BE, #DE { fill: blue; stroke: blue; }",
            mapStyles : "#NL, #BE, #DE { fill: blue; stroke: blue; }",
        });
    },
    methods:{
        show(country){
            this.landenAfkorting = country.afk
            console.log(country.afk)
        }
    }
}
</script>