<template>
  <v-card :to="link">
    <div class="pa-2 pa-md-3">
      <div class="mb-1">
        <span class="text-uppercase font-weight-black text-body-2 primary--text">
          {{ event.location }}
        </span>
        <span class="float-right">
          <v-chip v-if="event.open===true" text-color="white" color="green" class="ma-1">
            Open
          </v-chip>
          <v-chip v-else class="ma-1">
            Closed
          </v-chip>
        </span>
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
        <v-chip v-if="event.attendees" small class="mr-1 mb-2">
          {{ event.attendees }}
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
