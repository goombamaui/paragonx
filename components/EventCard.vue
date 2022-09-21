<template>
  <v-card :to="link">
    <div class="pa-2 pa-md-3">
      <div class="text-uppercase font-weight-black text-body-2 primary--text mb-1">
        {{ event.location }}
      </div>
      <div class="title font-weight-bold text-h6">
        {{ event.title }}
      </div>
      <div class="mt-2 mb-1 text-body-2">
        {{ event.description }}
      </div>
      <div class="mt-3">
        <v-chip v-if="event.dateEnd" class="mr-1 mb-2" small>
          {{ event.dateStart | formatDate }} to {{ event.dateEnd | formatDate }}
        </v-chip>
        <v-chip v-else class="mr-1 mb-2" small>
          {{ event.dateStart | formatDate }}
        </v-chip>
        <v-chip small class="mr-1 mb-2">
          {{ event.time }}
        </v-chip>
        <v-chip v-if="event.instructor" small class="mr-1 mb-2">
          {{ event.instructor.replace(/ *\([^)]*\) */g, "") }}
        </v-chip>
      </div>
    </div>
  </v-card>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    event: {
      type: Object,
      default: () => {}
    }
  },
  computed: {
    link () {
      return `/events/${this.event.slug}`
    }
  }
}
</script>
