<template>
  <v-row justify="center" align="center">
    <div class="main-text">
      <h2 data-aos="fade-up">Our History</h2>
      <p data-aos="fade-up">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. In a dictum elit. Praesent laoreet lacus in laoreet ornare. Pellentesque vel varius nisi. In eleifend neque sed ultrices hendrerit. Praesent eu orci a quam accumsan gravida. Mauris ultrices nunc at odio imperdiet varius. Aenean iaculis augue at congue iaculis. Etiam vel nisl dolor. Vestibulum imperdiet nisl eu convallis molestie.
      </p>
      <p data-aos="fade-up">
        In dictum, massa ut dapibus pretium, ante nibh volutpat nisi, quis fermentum quam mi id nulla. Aliquam ut gravida sem. Nam sit amet faucibus ex. Integer scelerisque accumsan tellus interdum venenatis. Aenean ex tortor, malesuada in varius sed, dapibus molestie sapien. Nam vestibulum sem ut bibendum ultrices. Quisque dapibus sed nunc eu viverra. Praesent augue diam, pellentesque vitae imperdiet vulputate, sodales id nibh. Praesent id nunc ac quam interdum venenatis.
      </p>
      <p data-aos="fade-up">
        In egestas orci ac posuere lacinia. Proin ac porta odio. Suspendisse vel justo malesuada enim venenatis dignissim. Aliquam at tempor magna. Donec vel lorem nec ligula condimentum feugiat. Pellentesque commodo finibus nisl, non aliquam ante facilisis vel. Maecenas consequat auctor sem, a dapibus massa faucibus nec. Donec tortor turpis, accumsan in quam at, finibus accumsan odio. Nam consectetur tincidunt eros eu cursus. Duis imperdiet tincidunt turpis ut dapibus. Suspendisse posuere erat sapien, pellentesque gravida lacus elementum egestas. Pellentesque velit dui, dignissim non tortor quis, blandit pharetra magna. In at dui sapien. Phasellus id turpis a lectus rhoncus condimentum. Aenean euismod diam at tellus cursus, eget feugiat nulla tristique.
      </p>
    </div>
  </v-row>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  name: 'IndexPage',
  mixins: [aosMixin],

  data () {
    return {
    }
  },


  methods: {
  },
}
</script>

<style scoped>
@import "~/assets/styles.css";

.main-text {

}

h2 {
  color: #2c2924;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

</style>