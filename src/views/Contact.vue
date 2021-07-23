/* eslint-disable prettier/prettier */
<template>
  <transition
    :duration="{ enter: 500, leave: 0 }"
    name="fade"
    mode="out-in"
    appear
  >
    <div v-if="show">
      <b-container>
        <b-row>
          <!-- Contact Information -->
          <b-col>
            <div class="text-side">
              <p>
                <span class="highlight">Primary Email: </span>
                prodijvy@gmail.com
              </p>
              <p>
                <span class="highlight">Music Submissions: </span>
                demmiigod@gmail.com or contact my
                <span class="line">discord: jjvy#2477</span>
              </p>
              <p class="highlight">*CONTACT FORM IS CURRENTLY UNAVAILABLE*</p>
            </div>
          </b-col>
          <!-- Contact Information -->

          <!-- Contact Form -->
          <b-col>
            <b-form novalidate @submit="onSubmit" @reset="onReset" v-if="show">
              <b-form-group
                id="input-group-1"
                label="Email address:"
                label-for="input-1"
                description="We'll never share your email with anyone else."
              >
                <b-form-input
                  disabled
                  id="input-1"
                  v-model="form.email"
                  type="email"
                  placeholder="Disabled Email"
                  required
                ></b-form-input>
              </b-form-group>

              <b-form-group
                id="input-group-2"
                label="Your Name:"
                label-for="input-2"
              >
                <b-form-input
                  disabled
                  id="input-2"
                  v-model="form.name"
                  placeholder="Disabled Name"
                  required
                ></b-form-input>
              </b-form-group>

              <b-form-group
                id="input-group-3"
                label="Your Message:"
                label-for="input-3"
              >
                <b-form-textarea
                  disabled
                  id="textarea"
                  v-model="form.text"
                  placeholder="Disabled Textarea"
                  rows="3"
                  max-rows="6"
                ></b-form-textarea>
              </b-form-group>

              <button type="submit">Submit</button>
            </b-form>
          </b-col>
          <!-- Contact Form -->
        </b-row>
      </b-container>
      <Footer />
    </div>
  </transition>
</template>

<script>
// Components
import Footer from "../components/Footer.vue";

export default {
  name: "Contact",
  components: {
    Footer,
  },
  data() {
    return {
      show: true,
      form: {
        email: "",
        name: "",
        text: "",
      },
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(event) {
      event.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.text = "";
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    },
  },
};
</script>

<style scoped>
.container {
  margin-top: 100px;
  margin-bottom: 100px;
}

.text-side {
  text-align: left;
}

.highlight {
  color: #b94242;
  font-weight: bold;
}

form {
  background-color: #000;
  padding: 50px;
}

button {
  padding: 10px;
  border: none;
  border-radius: none;
  background-color: #942e2e;
  color: #fff;
  text-transform: uppercase;
  cursor: pointer;
}
</style>
