<script setup>
import chatbuddy from './chatbuddy.vue'
import searchbar from './searchbar.vue'
import hamburgermenu from './menu.vue'
import globe from './globe.vue'
</script>

<template>
      <header>
        <hamburgermenu @update-blur="updateBlurFunction" />
        <searchbar />
        <div class="rightTop">
          <div class="smgBackground">
            <svg width="15px" height="21px" viewBox="0 0 15 21" version="1.1" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink">
              <title>?</title>
              <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <g id="001a_Home_v7" transform="translate(-1162.000000, -42.000000)" fill="#FFFFFF" fill-rule="nonzero">
                  <g id="Group-15" transform="translate(1147.000000, 30.000000)">
                    <g id="?" transform="translate(15.240000, 12.360000)">
                      <path
                        d="M3.75,14.07 C3.75,14.7 3.99,14.94 4.62,14.94 L7.86,14.94 C8.49,14.94 8.7,14.7 8.7,14.07 L8.7,13.41 C8.7,12.54 8.91,12.33 9.84,11.91 L11.61,11.13 C12.96,10.53 14.52,9.24 14.52,6.15 L14.52,5.13 C14.49,2.55 12.6,0 7.2,0 C1.8,0 0,2.55 0,5.13 L0,6.99 C0,7.62 0.24,7.89 0.87,7.89 L3.96,7.89 C4.59,7.89 4.8,7.62 4.8,6.99 L4.8,5.91 C4.8,4.53 5.79,3.96 7.2,3.96 C8.61,3.96 9.63,4.53 9.63,5.91 L9.63,6.33 C9.63,7.32 9.15,7.68 8.67,7.92 L5.58,9.48 C4.56,9.99 3.75,10.5 3.75,12.12 L3.75,14.07 Z M8.7,17.28 C8.7,16.65 8.49,16.38 7.86,16.38 L4.62,16.38 C3.99,16.38 3.75,16.65 3.75,17.28 L3.75,19.77 C3.75,20.4 3.99,20.64 4.62,20.64 L7.86,20.64 C8.49,20.64 8.7,20.4 8.7,19.77 L8.7,17.28 Z"
                        id="Shape"></path>
                    </g>
                  </g>
                </g>
              </g>
            </svg>
          </div>
          <div class="smgBackground">
            <svg width="21px" height="24px" viewBox="0 0 21 24" version="1.1" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink">
              <title>Group 7</title>
              <defs>
                <polygon id="path-1" points="0 0 5.2448625 0 5.2448625 2.50052101 0 2.50052101"></polygon>
                <polygon id="path-3" points="0 0 21 0 21 20.5978714 0 20.5978714"></polygon>
              </defs>
              <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <g id="001a_Home_v7" transform="translate(-1208.000000, -41.000000)">
                  <g id="Group-9" transform="translate(1197.000000, 30.000000)">
                    <g id="Group-13-Copy-2" transform="translate(11.000000, 5.000000)">
                      <g id="Group-7" transform="translate(0.000000, 6.000000)">
                        <g id="Group-3" transform="translate(7.873258, 21.499479)">
                          <mask id="mask-2" fill="white">
                            <use xlink:href="#path-1"></use>
                          </mask>
                          <g id="Clip-2"></g>
                          <path
                            d="M0.76940555,1.76575566 C1.24438741,2.21907596 1.89992745,2.50057324 2.62216014,2.50057324 L2.62216014,2.50057324 C3.34710392,2.50057324 4.00264395,2.21907596 4.4770836,1.76575566 C4.95152324,1.31243537 5.2448625,0.687292059 5.2448625,0 L0,0 C0,0.687292059 0.294423688,1.31243537 0.76940555,1.76575566"
                            id="Fill-1" fill="#FFFFFF" mask="url(#mask-2)"></path>
                        </g>
                        <g id="Group-6">
                          <mask id="mask-4" fill="white">
                            <use xlink:href="#path-3"></use>
                          </mask>
                          <g id="Clip-5"></g>
                          <path
                            d="M18.3816896,16.8485783 L18.3811474,16.8480561 L18.3811474,10.6122908 C18.3811474,6.76324632 16.2231248,3.56702489 12.4709849,2.72618887 L12.4709849,1.87490767 C12.4709849,0.840836029 11.5925938,0 10.5027382,0 C10.5016538,0 10.5011115,0 10.5000271,0 C10.4989427,0 10.4984005,0 10.497316,0 C9.40746039,0 8.52906927,0.840836029 8.52906927,1.87490767 L8.52906927,2.72618887 C4.77692945,3.56702489 2.61890684,6.76324632 2.61890684,10.6122908 L2.61890684,16.8480561 L2.61836462,16.8485783 C0.000542216737,16.967131 0,19.3444513 0,19.3444513 L0,20.5978714 L21.0000542,20.5978714 L21.0000542,19.3444513 C21.0000542,19.3444513 20.999512,16.967131 18.3816896,16.8485783"
                            id="Fill-4" fill="#FFFFFF" mask="url(#mask-4)"></path>
                        </g>
                      </g>
                    </g>
                  </g>
                </g>
              </g>
            </svg>
          </div>
          <figure>
            <img src="../assets/Images/jettje.jpg" alt="Juliette Groot">
            <figcaption>Juliette Groot</figcaption>
          </figure>
        </div>
      </header>
      <main :class="blurClass">
        <h1> Bezoekers per Land </h1>
        <p>Landen met de meeste bezoekers</p>
        <chatbuddy />
        <globe/>
        <div class="landen">
            <div id="myearth"></div>
        </div>
      </main>
      <footer class="cfooter" :class="blurClass"><img src="../assets/Images/gi-logo-wit.png" alt="Get Interactive logo"><svg id="driePijl"
          width="16px" height="20px" viewBox="0 0 16 20" version="1.1" xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink">
          <title>Group</title>
          <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
            <g id="001a_Home_v7" transform="translate(-712.000000, -969.000000)" fill="#FFFFFF">
              <g id="Group" transform="translate(712.000000, 969.000000)">
                <polygon id="Fill-1-Copy"
                  transform="translate(8.000000, 10.000000) scale(1, -1) translate(-8.000000, -10.000000) "
                  points="8 6.07718019 0 13.9228198 2.6274206 13.9228198 8 8.65390459 13.3731991 13.9228198 16 13.9228198">
                </polygon>
                <polygon id="Fill-1-Copy-3" opacity="0.6"
                  transform="translate(8.000000, 16.077180) scale(1, -1) translate(-8.000000, -16.077180) "
                  points="8 12.1543604 0 20 2.6274206 20 8 14.7310848 13.3731991 20 16 20"></polygon>
                <polygon id="Fill-1-Copy-2" opacity="0.4"
                  transform="translate(8.000000, 3.922820) scale(1, -1) translate(-8.000000, -3.922820) "
                  points="8 0 0 7.84563962 2.6274206 7.84563962 8 2.5767244 13.3731991 7.84563962 16 7.84563962">
                </polygon>
              </g>
            </g>
          </g>
        </svg>
        <div class="terugvolgende"><svg width="21px" height="11px" viewBox="0 0 21 11" version="1.1"
            xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
            <title>Fill 1</title>
            <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
              <g id="001a_Home_v7" transform="translate(-1380.000000, -903.000000)" fill="#FFFFFF">
                <polygon id="Fill-1"
                  points="1390.5 903 1380 914 1383.44849 914 1390.5 906.612703 1397.55232 914 1401 914">
                </polygon>
              </g>
            </g>
          </svg>
          <p id="pagina">5/10</p><svg width="21px" height="11px" viewBox="0 0 21 11" version="1.1"
            xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" id="beneden">
            <title>Fill 1 Copy</title>
            <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
              <g id="001a_Home_v7" transform="translate(-1380.000000, -964.000000)" fill="#FFFFFF">
                <polygon id="Fill-1-Copy"
                  transform="translate(1390.500000, 969.500000) scale(1, -1) translate(-1390.500000, -969.500000) "
                  points="1390.5 964 1380 975 1383.44849 975 1390.5 967.612703 1397.55232 975 1401 975">
                </polygon>
              </g>
            </g>
          </svg>
        </div>
      </footer>
</template>
<script>

export default {

  data() {
    return {
      blurClass: null,
    };
  },
  components: { hamburgermenu },
  methods: {
    updateBlurFunction(value) {
      this.blurClass = value
      console.log(this.updateBlurFunction)
    },
  }
}
</script>
<style>
@import '../assets/main.css';
@import 'swiper/css';
@import'../assets/countries.css';


body {
  overflow-x: hidden;
}

.blur {
  filter: blur(1.5rem);
}
</style>

