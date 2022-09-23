<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="12" md="10">
          <h3 class="text-md-h3 text-h4">
            {{ content.title }}
          </h3>
        </v-col>
        <v-col cols="12" md="2">
          <div class="sm-text-right">
            <v-btn color="primary" large :href="content.registration" target="_blank">
              Register
            </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-chip v-if="content.instructor" class="mr-1 mb-2">
        {{ content.instructor }}
      </v-chip>
      <v-chip class="mr-1 mb-2">
        @{{ content.location }}
      </v-chip>
      <v-chip v-if="content.dateEnd" class="mr-1 mb-2">
        {{ content.dateStart | formatDate }} to {{ content.dateEnd | formatDate }}
      </v-chip>
      <v-chip v-else class="mr-1 mb-2">
        {{ content.dateStart | formatDate }}
      </v-chip>
      <v-chip class="mr-1 mb-2">
        {{ content.time }}
      </v-chip>
    </v-container>
    <v-container>
      <nuxt-content :document="content" />
    </v-container>
  </div>
</template>

<script>
export default {
  async asyncData ({ params, error, $content }) {
    const content = (await $content('events').where({ slug: params.slug }).fetch())[0]
    if (!content) {
      error({ statusCode: 404, message: '404 Not Found' })
    } else {
      return { content }
    }
  }
}
</script>
