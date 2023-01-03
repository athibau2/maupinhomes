<template>
  <v-row class="gallery" justify="center" align="center">
    <v-col>
      <span v-for="i in numPics / 2" :key="i" data-aos="fade-up">
        <figure>
          <a target="_blank" :href="`https://maupinhomesco.com/pic${i}.jpg`">
            <img class="gallery__img"
              :src="require(`~/assets/images/projects/pic${i}.jpg`)"
            />
          </a>
        </figure>
      </span>
    </v-col>
    <v-col>
      <span v-for="i in numPics / 2" :key="i" data-aos="fade-up">
        <figure>
          <a target="_blank" :href="`https://maupinhomesco.com/pic${i + (numPics / 2)}.jpg`">
            <img class="gallery__img"
            :src="require(`~/assets/images/projects/pic${i + (numPics / 2)}.jpg`)"
            />
          </a>
        </figure>
      </span>
    </v-col>
  </v-row>
  <!-- <div class="gallery">
    <span v-for="i in numPics" :key="i" data-aos="fade-up">
      <figure>
        <img class="gallery__img"
          :src="require(`~/assets/images/projects/pic${i}.jpg`)"
        />
      </figure>
    </span>
  </div> -->
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  name: 'GalleryPage',
  layout: 'default2',
  mixins: [aosMixin],

  data () {
    return {
      numPics: 22,
    }
  },


}
</script>

<style scoped>
@import "~/assets/styles.css";

.gallery {
  max-width: 80%;
  margin-left: 10%;
}

.gallery__img {
  max-width: 100%;
  border-radius: 8px;
}

/* .gallery {
  margin-left: 7.5%;
  max-width: 85%;
  display: inline-grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: auto;
  align-content: flex-start;
  column-gap: 10px;
  row-gap: 10px;
}

.gallery__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

img {
  width: 25%;
  margin: 2px;
  border-radius: 8px;
} */


</style>
