<template>
    <div>
        <h2 class="text-center">Current Homes For Sale</h2>

        <v-dialog v-if="showDialog" v-model="showDialog"
            fullscreen
            :scrim="false"
            transition="dialog-bottom-transition"
        >
            <v-card>
                <v-toolbar class="dialog-toolbar">
                    <v-btn icon @click="showDialog = false">
                        <v-icon>mdi-close</v-icon>
                    </v-btn>
                    <v-toolbar-title
                        :style="isMobile ? {'font-size': '16px'} : null"
                    >
                        {{openHouse.address}}
                    </v-toolbar-title>
                </v-toolbar>
                <div class="carousel-wrapper justify-center">
                    <span class="image-wrapper" v-for="(image, i) in openHouse.images" :key="i">
                        <img class="images"
                            :src="require(`~/assets/images/${openHouse.imageSrc}/${image}`)"
                            style="width: 300px"
                        />
                    </span>
                </div>
                <div class="text-row-wrapper">
                    <v-row class="text-row">
                        <v-col class="text-center">
                            <span class="header">Details</span><br>
                            <list>
                                <list-item class="list-items">{{openHouse.price}}</list-item><br>
                                <list-item class="list-items">{{openHouse.numBeds}} Bed</list-item><br>
                                <list-item class="list-items">{{openHouse.numBaths}} Bath</list-item><br>
                                <list-item class="list-items">{{openHouse.totalSF}} Sq. Ft.</list-item><br>
                                <list-item class="list-items">{{openHouse.neighborhood}}</list-item><br>
                                <list-item class="list-items">{{openHouse.style}}</list-item><br>
                                <list-item class="list-items">{{openHouse.distance}}</list-item><br>
                            </list>
                        </v-col>
                        <v-col class="text-center">
                            <span class="header">Amenities</span><br>
                            <list>
                                <list-item class="list-items" v-for="(item, i) in openHouse.amenities" :key="i">{{item}}<br></list-item>
                            </list>
                        </v-col>
                    </v-row>
                </div>
            </v-card>
        </v-dialog>

        <v-row class="house-row" justify="center" align="center">
            <v-card class="house-card"
                v-for="(house, i) in houses"
                :key="i"
                data-aos="fade-up"
                data-aos-duration="500"
            >
                <v-card-title class="justify-center">
                    <span class="title-container">
                        <v-btn class="chevron" @click="decrement(house)" icon>
                            <v-icon size="50">mdi-chevron-left</v-icon>
                        </v-btn>
                        <img class="images"
                            :src="require(`~/assets/images/${house.imageSrc}/${house.images[house.index]}`)"
                            :style="isMobile ? {'width': '275px'} : null"
                        />
                        <v-btn class="chevron" @click="increment(house)" icon>
                            <v-icon size="50">mdi-chevron-right</v-icon>
                        </v-btn>
                    </span>
                    <span class="address justify-left"
                        :style="isMobile ? {'font-size': '15px'} : null"
                    >
                        {{house.address}}
                    </span>
                </v-card-title>
                <v-card-subtitle class="subtitle text-center">
                    {{house.price}} | {{house.numBeds}} Bed | {{house.numBaths}} Bath | {{house.totalSF}} Sq. Ft
                </v-card-subtitle>
                <v-card-text class="text-center">
                    <v-btn class="btn" @click="openDialog(house)" text>More Details</v-btn>
                </v-card-text>
            </v-card>
        </v-row>
    </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  name: 'HomesPage',
  layout: 'default2',
  mixins: [aosMixin],

  data () {
    return {
        openHouse: null,
        showDialog: false,
        picIndex: 0,
        houses: [
            {
                index: 0,
                price: '$1,499,900',
                address: '15611 Paintbrush St.\nBuena Vista, CO 81211',
                neighborhood: 'Westwinds Subdivision HOA',
                totalSF: 5016,
                numBeds: 5,
                numBaths: 4.5,
                style: 'Modern Rustic farmhouse style',
                distance: '3 minutes from downtown Buena Vista, CO',
                amenities: [
                    'Office',
                    'Kitchen',
                    'Great Room with fireplace',
                    'Behind-kitchen walk-through pantry',
                    'Large Master Bedroom/bathroom/walk-in closet',
                    'Large front porch entrance',
                    'Workout room',
                    '3 Car oversized garage',
                    'Utility room with washer/dryer hookups',
                    'Access to basement from main level and garage',
                    'Full kitchen in basement with pantry'
                ],
                imageSrc: '15611-Paintbrush-St',
                images: [
                    'design-1.png',
                    'design-2.png',
                    'design-3.png',
                    'design-4.png',
                    'floor-plan-1.png',
                    'floor-plan-2.png',
                    'frame-1.jpg',
                    'frame-2.jpg',
                    'frame-3.jpg'
                ]
            },
        ]
    }
  },

  methods: {
    increment(house) {
        if (house.index === house.images.length - 1) {
            house.index =0
        } else house.index++
    },

    decrement(house) {
        if (house.index === 0) {
            house.index = house.images.length - 1
        } else house.index--
    },

    openDialog(house) {
        this.openHouse = house
        this.showDialog = true
    }
  },

  computed: {
    isMobile () {
      let check = false;
      (function(a){if(/(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|mobile.+firefox|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows ce|xda|xiino/i.test(a)||/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r750|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(a.substr(0,4))) check = true;})(navigator.userAgent||navigator.vendor||window.opera);
      return check;
    }
  }
  
}
</script>

<style scoped>
@import "~/assets/styles.css";

.house-row {
    margin: 5px;
}

.house-card {
    margin: 5px;
    width: 500px;
}

.images {
    margin: 10px;
    width: 350px;
    border-radius: 10px;
}

.title-container {
    display: flex;
    align-items: center;
}

.address {
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 17px;
    color: #2c2924;
}

.subtitle {
    color: #2c2924 !important;
    font-family: Arial, Helvetica, sans-serif;
}

.btn {
    height: 50px !important;
}

.dialog-bottom-transition-enter-active,
.dialog-bottom-transition-leave-active {
    transition: transform .2s ease-in-out;
}

.dialog-toolbar {
    background-image: linear-gradient(to right, #edf0ee, rgba(8, 163, 224, 0.4), #edf0ee);
}

.carousel-wrapper {
    margin: 10px auto;
    max-width: 90%;
    overflow-x: scroll !important;
    white-space: nowrap;
}

.image-wrapper {
    display: inline-block;
}

.image-wrapper img {
  display: inline-block;
  max-width: 100%;
}

.list-items {
    list-style: none;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
}

.text-row-wrapper {
    justify-content: center;
    display: flex;
}

.text-row {
    margin: 20px;
    width: 90%;
}

.header {
    font-size: 26px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    text-decoration: underline;
}

</style>
