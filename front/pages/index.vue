<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-flex
      xs12
      sm8
      md6
    >
      <div class="text-center">
        <logo />
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications.</p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat repellat maiores, architecto a impedit ut provident deserunt cum sunt debitis nemo beatae modi voluptas. Illum vero quos fugiat nihil vitae.
            Doloribus, explicabo nemo? Officia, natus explicabo illum tempore nihil nulla. Fugit blanditiis corrupti quidem exercitationem totam eum expedita reiciendis animi omnis nulla iste, aut dignissimos eius provident porro placeat similique.
            Quaerat laborum, nam quis recusandae a molestiae mollitia, quod dignissimos eaque sapiente accusantium numquam sed laboriosam illum soluta deserunt vitae suscipit id consequatur reiciendis at corrupti earum libero. Ipsa, labore.
            Commodi placeat laudantium fuga aliquam culpa quod qui libero ullam ad cupiditate cumque natus nisi, quae veritatis nesciunt, vitae repellat non id quibusdam! Quibusdam sapiente cumque nulla inventore minima quasi!
            Asperiores, autem iure. Blanditiis obcaecati beatae ipsum sequi quisquam quia animi architecto a, magnam quae? Laborum velit aliquid, doloribus aut quasi voluptate quibusdam non quos excepturi, ullam, ut vitae quisquam.
            Tempore ullam fuga dolore quis magnam assumenda similique error natus dolorum vel debitis dolorem, quasi et. Soluta consequatur minus ipsam? Dolorum illum nihil labore dolore magnam quidem vitae quibusdam nam?
            Maiores magni animi beatae ad architecto aliquid quae, voluptate labore vitae provident repellat ea doloremque voluptas consequatur, eveniet eum blanditiis officia? Quam ab odit placeat enim adipisci fuga, repudiandae laborum?
            Earum praesentium adipisci dolores tenetur alias modi, architecto fugit, quidem excepturi tempora iusto odio rem. Quam cupiditate distinctio dolore ullam! Molestias dolorem assumenda id odio aspernatur facilis eius ex tenetur?
            Delectus sunt aut quae voluptates molestiae eaque facilis suscipit eveniet quam cupiditate explicabo officiis cum, impedit quas nobis laborum culpa, ea placeat pariatur accusamus dolor tenetur ducimus nostrum necessitatibus? Necessitatibus?
            Excepturi beatae aut odio quis modi quaerat maiores iste, ipsum animi consequatur alias nesciunt in delectus veritatis fugiat dolorum accusamus laborum ea cum suscipit dolorem labore, sint, quas voluptatum! A.
          </p>
          <p>
            For more information on Vuetify, check out the <a
              href="https://vuetifyjs.com"
              target="_blank"
            >
              documentation
            </a>.
          </p>
          <p>
            If you have questions, please join the official <a
              href="https://chat.vuetifyjs.com/"
              target="_blank"
              title="chat"
            >
              discord
            </a>.
          </p>
          <p>
            Find a bug? Report it on the github <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              title="contribute"
            >
              issue board
            </a>.
          </p>
          <p>Thank you for developing with Vuetify and I look forward to bringing more exciting features in the future.</p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
          <hr class="my-3">
          <a
            href="https://nuxtjs.org/"
            target="_blank"
          >
            Nuxt Documentation
          </a>
          <br>
          <a
            href="https://github.com/nuxt/nuxt.js"
            target="_blank"
          >
            Nuxt GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>
