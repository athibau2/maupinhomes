<template>
  <v-row class="index" justify="center" align="center">
    <div class="main-text">
      <h2 data-aos="fade-up">About Us</h2>
      <p data-aos="fade-up">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur cursus eget orci in vestibulum. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nullam egestas turpis facilisis, mollis mauris id, molestie elit. Maecenas ultricies vel massa eget aliquam. Aliquam suscipit vestibulum varius. Duis euismod, sapien at pulvinar blandit, arcu sem aliquam metus, bibendum dignissim elit diam eget lorem. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
      </p>
      <p data-aos="fade-up">
        Sed dictum sem ut pharetra cursus. Quisque porttitor venenatis orci. Pellentesque pharetra venenatis leo, non egestas ipsum porttitor quis. Nullam congue odio tellus, nec lobortis odio dapibus vitae. Ut eget orci in ante lobortis luctus in lacinia mauris. Aliquam faucibus ornare dolor, vitae congue ligula vestibulum lacinia. Sed efficitur pellentesque lorem, nec feugiat ante aliquam sit amet. Phasellus commodo consectetur lacus ut venenatis. Fusce facilisis molestie pellentesque. Mauris leo justo, convallis et blandit ut, dignissim quis diam. Mauris suscipit tortor eros, quis sagittis leo feugiat id. Mauris mauris nisi, venenatis laoreet efficitur ornare, pretium eu ante.
      </p>

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
  margin: 10px 20px;  
}

h2 {
  color: #2c2924;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

</style>