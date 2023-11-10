<template>
  <div>
    <v-container>
      <div>
        <span class="text-md-h3 text-h4">
          {{ content.title }}
        </span>
        <span class="sm-text-right float-right mr-2 d-none d-sm-block">
          <v-btn
            v-if="content.zoom"
            outlined
            large
            :href="content.zoom"
            target="_blank"
            class="mr-1"
          >
            Zoom Link
          </v-btn>
          <span v-if="content.registration">
            <v-btn v-if="content.open" color="primary" large :href="content.registration" target="_blank">
              Register
            </v-btn>
            <v-btn v-else color="error" large disabled>
              Registration Closed
            </v-btn>
          </span>
        </span>
      </div>
    </v-container>
    <v-container>
      <div class="d-none d-sm-block">
        <v-chip v-if="content.open===true" color="green" class="mr-1 mb-2">
          Registration Open
        </v-chip>
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
        <v-chip v-if="content.attendees" class="mr-1 mb-2">
          {{ content.attendees }}
        </v-chip>
        <v-chip v-if="content.recording" class="mr-1 mb-2">
          {{ content.recording }}
        </v-chip>
      </div>
      <div class="d-sm-none">
        <v-list-item v-if="content.instructor" class="pl-0">
          <v-list-item-avatar>
            <v-icon>mdi-account</v-icon>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>
              {{ content.instructor }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item class="pl-0">
          <v-list-item-avatar>
            <v-icon>mdi-map-marker</v-icon>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>
              {{ content.location }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item class="pl-0">
          <v-list-item-avatar>
            <v-icon>mdi-calendar</v-icon>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>
              <span v-if="content.dateEnd" class="mr-1 mb-2">
                {{ content.dateStart | formatDate }} to {{ content.dateEnd | formatDate }}
              </span>
              <span v-else class="mr-1 mb-2">
                {{ content.dateStart | formatDate }}
              </span>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item class="pl-0">
          <v-list-item-avatar>
            <v-icon>mdi-clock-time-two</v-icon>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>
              {{ content.time }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </div>
    </v-container>
    <v-container class="d-sm-none">
      <v-btn
        v-if="content.open"
        block
        color="primary"
        large
        :href="content.registration"
        target="_blank"
      >
        Register
      </v-btn>
      <v-btn
        v-else
        block
        color="primary"
        large
        disabled
      >
        Registration Closed
      </v-btn>
      <v-btn
        v-if="content.zoom"
        block
        outlined
        large
        :href="content.zoom"
        target="_blank"
        class="mt-1"
      >
        Zoom Link
      </v-btn>
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
  },
  head () {
    return {
      title: this.content.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.content.description || this.content.title
        }
      ]
    }
  }
}
</script>
