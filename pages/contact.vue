<template>
  <v-row justify="center" align="center">
    <v-col class="text-center">
        <h2>Interested in learning more?</h2>
        <h5>Contact us below to schedule a consultation.</h5>
        <form class="form"
            :action="'https://formspree.io/f/mjvdvelp'"
            method="POST"
            :style="{'width': isMobile ? '90%' : '60%'}"
            data-aos="fade-up"
        >
            <!-- FormSpark action: 'https://submit-form.com/AVmOTv5s', no POST method -->
            <!-- Following line is for FormSpark -->
            <!-- <input type="hidden" name="_redirect" value="https://maupinhomesco.com/contact" /> -->
            <input
                class="name-field"
                v-model="name"
                type="name"
                name="name"
                placeholder="Enter your name"
                required
            />
            <input
                class="email-field"
                v-model="email"
                type="email"
                name="email"
                placeholder="Enter your email"
                required
            />
            <textarea
                class="message-field"
                v-model="message"
                name="message"
                placeholder="Enter your message"
                rows="8"
                required
            ></textarea>
            <br>
            <v-btn class="form-btn" @click="clearForm()">
                <v-icon>mdi-close-circle</v-icon>
                <span>Clear</span>
            </v-btn>
            <v-btn class="form-btn" type="submit">
                <v-icon>mdi-send</v-icon>
                <span>Send</span>
            </v-btn>
        </form>


    </v-col>
  </v-row>
</template>

<script>
export default {
    name: 'ContactPage',
    layout: 'default2',

    mounted () {
        // Following 'if' statement is for FormSpark
        // if (this.$route.query.email != undefined) {
        //     alert('Thank you for your message! We will get back to you as soon as we can.')
        //     this.$router.push('/contact')
        // }
    },

    data () {
        return {
            name: '',
            email: '',
            message: '',
        }
    },

    methods: {
        clearForm () {
            this.name = ''
            this.email = ''
            this.message = ''
        },
    },

    computed: {
        isMobile () {
            let check = false;
            (function(a){if(/(android|bb\d+|meego).+mobile|avantgo|bada\/|blackberry|blazer|compal|elaine|fennec|hiptop|iemobile|ip(hone|od)|iris|kindle|lge |maemo|midp|mmp|mobile.+firefox|netfront|opera m(ob|in)i|palm( os)?|phone|p(ixi|re)\/|plucker|pocket|psp|series(4|6)0|symbian|treo|up\.(browser|link)|vodafone|wap|windows ce|xda|xiino/i.test(a)||/1207|6310|6590|3gso|4thp|50[1-6]i|770s|802s|a wa|abac|ac(er|oo|s\-)|ai(ko|rn)|al(av|ca|co)|amoi|an(ex|ny|yw)|aptu|ar(ch|go)|as(te|us)|attw|au(di|\-m|r |s )|avan|be(ck|ll|nq)|bi(lb|rd)|bl(ac|az)|br(e|v)w|bumb|bw\-(n|u)|c55\/|capi|ccwa|cdm\-|cell|chtm|cldc|cmd\-|co(mp|nd)|craw|da(it|ll|ng)|dbte|dc\-s|devi|dica|dmob|do(c|p)o|ds(12|\-d)|el(49|ai)|em(l2|ul)|er(ic|k0)|esl8|ez([4-7]0|os|wa|ze)|fetc|fly(\-|_)|g1 u|g560|gene|gf\-5|g\-mo|go(\.w|od)|gr(ad|un)|haie|hcit|hd\-(m|p|t)|hei\-|hi(pt|ta)|hp( i|ip)|hs\-c|ht(c(\-| |_|a|g|p|s|t)|tp)|hu(aw|tc)|i\-(20|go|ma)|i230|iac( |\-|\/)|ibro|idea|ig01|ikom|im1k|inno|ipaq|iris|ja(t|v)a|jbro|jemu|jigs|kddi|keji|kgt( |\/)|klon|kpt |kwc\-|kyo(c|k)|le(no|xi)|lg( g|\/(k|l|u)|50|54|\-[a-w])|libw|lynx|m1\-w|m3ga|m50\/|ma(te|ui|xo)|mc(01|21|ca)|m\-cr|me(rc|ri)|mi(o8|oa|ts)|mmef|mo(01|02|bi|de|do|t(\-| |o|v)|zz)|mt(50|p1|v )|mwbp|mywa|n10[0-2]|n20[2-3]|n30(0|2)|n50(0|2|5)|n7(0(0|1)|10)|ne((c|m)\-|on|tf|wf|wg|wt)|nok(6|i)|nzph|o2im|op(ti|wv)|oran|owg1|p800|pan(a|d|t)|pdxg|pg(13|\-([1-8]|c))|phil|pire|pl(ay|uc)|pn\-2|po(ck|rt|se)|prox|psio|pt\-g|qa\-a|qc(07|12|21|32|60|\-[2-7]|i\-)|qtek|r380|r750|raks|rim9|ro(ve|zo)|s55\/|sa(ge|ma|mm|ms|ny|va)|sc(01|h\-|oo|p\-)|sdk\/|se(c(\-|0|1)|47|mc|nd|ri)|sgh\-|shar|sie(\-|m)|sk\-0|sl(45|id)|sm(al|ar|b3|it|t5)|so(ft|ny)|sp(01|h\-|v\-|v )|sy(01|mb)|t2(18|50)|t6(00|10|18)|ta(gt|lk)|tcl\-|tdg\-|tel(i|m)|tim\-|t\-mo|to(pl|sh)|ts(70|m\-|m3|m5)|tx\-9|up(\.b|g1|si)|utst|v400|v750|veri|vi(rg|te)|vk(40|5[0-3]|\-v)|vm40|voda|vulc|vx(52|53|60|61|70|80|81|83|85|98)|w3c(\-| )|webc|whit|wi(g |nc|nw)|wmlb|wonu|x700|yas\-|your|zeto|zte\-/i.test(a.substr(0,4))) check = true;})(navigator.userAgent||navigator.vendor||window.opera);
            return check;
        }
    },
}
</script>

<style scoped>
@import "~/assets/styles.css";

h5 {
    font-family: Arial, Helvetica, sans-serif;
}

.form {
    margin-top: 20px;
    text-align: center;
    display: inline-block;
}

.name-field, .email-field {
    width: 49%;
    background-color: #edf0ee;
    padding: 10px;
    margin: 10px 0;
    border-radius: 15px;
    border: solid #9c8c94;
}

.message-field {
    width: 98.5%;
    background-color: #edf0ee;
    padding: 10px;
    border-radius: 15px;
    border: solid #9c8c94;
}

.form-btn {
    background-color: #9c8c94 !important;
    background: linear-gradient(to bottom right, #08a3e0, #9c8c94);
    font-size: 15px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    color: #2b2b24;
    padding: 15px !important;
    padding-top: 20px !important;
    padding-bottom: 20px !important;
}

</style>
