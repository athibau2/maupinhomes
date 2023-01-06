<template>
  <v-row class="" justify="center" align="center">
    <v-col class="reviews-col">
      <h2 class="text-center">Hear what our customers have to say!</h2>
      <v-divider class="divider" />
      
      <div class="review" data-aos="fade-up">
        <p>
          <i class="fas fa-quote-left fa-lg" id="left-quote"></i>
          <span class="review-text">
            When I finally decided to add a standalone garage to my vacation home, I began asking trusted friends and neighbors for recommendations and Andy Maupin was a name that consistently came up.  Andy, who has been in the area for a long time is well-connected and trusted.  Ultimately, the project was completed as designed on time, and on budget.  Andy was a proactive and effective communicator and we enjoyed designing and building with him.  If you are looking for a trusted, hardworking, honest builder, I would recommend Andy.
          </span>
          <i class="fas fa-quote-right fa-lg" id="right-quote"></i>
          <v-subheader class="name">&#126;Jim Smith, Ph.D.</v-subheader>
        </p>
      </div>

      <div class="review" data-aos="fade-up">
        <p>
          <i class="fas fa-quote-left fa-lg" id="left-quote"></i>
          <span class="review-text">
            Andy was on time, and always communicated without us having to press. He was very responsive to our questions. His work was impeccable and never in question. The contract was honored perfectly. We really like his help and subcontractors as well. Basically, he’s an honorable, professional, and knowledgeable person. If we ever build again, no line would be too long for us to wait to use him.
          </span>
          <i class="fas fa-quote-right fa-lg" id="right-quote"></i>
          <v-subheader class="name">&#126;Joe B.</v-subheader>
        </p>
      </div>
      
      <div class="review" data-aos="fade-up">
        <p>
          <i class="fas fa-quote-left fa-lg" id="left-quote"></i>
          <span class="review-text">
            My wife and I worked with Andy on multiple projects, including the complete construction of our mountain home. We cannot express enough the trust and faith we had in Andy to operate in our best interest throughout the entire project.  Being over a hundred miles away for us was stressful, but the communication, updates, and pride in his work that Andy exhibits made the process easy and exciting from beginning to end. We will be starting a new home build soon and will not trust the project with anyone but Andy Maupin for the entirety of the build.
          </span>
          <i class="fas fa-quote-right fa-lg" id="right-quote"></i>
          <v-subheader class="name">&#126;Greg B.</v-subheader>
        </p>
      </div>

      <br>
    </v-col>
  </v-row>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  name: 'ReviewsPage',
  layout: 'default2',
  mixins: [aosMixin],
  
}
</script>

<style scoped>
@import "~/assets/styles.css";

.divider {
  margin-top: 10px;
  margin-bottom: 30px;
}

.reviews-col {
  max-width: 75% !important;
}

.review {
  margin-bottom: 30px;
}

.review-text {
  margin: 10px;
  color: #2c2924;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 17px;
}

.fas {
  color: #2c2924;
}

#left-quote {
  vertical-align: top;
}

#right-quote {
  vertical-align: bottom;
}

.name {
  text-align: center;
  display: grid;
}

</style>
