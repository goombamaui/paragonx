<template>
  <div>
    <v-container>
      <h2 class="text-md-h2 text-h3 text-center">
        ParagonX Academy events and courses
      </h2>
      <div style="width: 80px; height: 4px" class="my-4 secondary mx-auto" />
      <div class="grey--text text--lighten-2 mt-4 text-body-1 text-center">
        Click on cards to see details and registration information.
      </div>
    </v-container>
    <v-container class="mt-2">
      <h4 class="text-h4 text-left">
        Online Classes
      </h4>
      <v-row class="mt-2">
        <v-col
          v-for="(event,index) in onlineClasses"
          :key="index"
          cols="12"
          md="6"
        >
          <event-card
            :event="
              event"
          />
        </v-col>
      </v-row>
    </v-container>
    <v-container class="mt-2">
      <h4 class="text-h4 text-left">
        Speaker Events
      </h4>
      <v-row class="mt-2">
        <v-col
          v-for="(event,index) in speakerEvents"
          :key="index"
          cols="12"
          md="6"
        >
          <event-card
            :event="
              event"
          />
        </v-col>
      </v-row>
    </v-container>
    <v-container class="mt-2">
      <h4 class="text-h4 text-left">
        In-Person Classes
      </h4>
      <v-row class="mt-2">
        <v-col
          v-for="(event,index) in inPersonClasses"
          :key="index"
          cols="12"
          md="6"
        >
          <event-card
            :event="
              event"
          />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'ContestIndex',
  async asyncData ({ params, error, $content }) {
    const events = await $content('events').sortBy('dateStart', 'asc').fetch()
    return { events }
  },
  head () {
    return {
      title: 'Events',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'ParagonX Academy is a 501(c)(3) student-led non-profit organization that strives to provide high-quality, readily available STEM education to everyone in need through free curricula.'
        }
      ]
    }
  },
  computed: {
    onlineClasses () {
      return this.events.filter(event => event.type === 'Online Class')
    },
    inPersonClasses () {
      return this.events.filter(event => event.type === 'In-Person Class')
    },
    speakerEvents () {
      return this.events.filter(event => event.type === 'Speaker Event')
    }
  }
}
</script>
