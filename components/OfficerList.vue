<template>
  <v-container>
    <h3 class="text-md-h3 text-h4 text-center">
      {{ title }}
    </h3>
    <div v-for="(person, i) in people" :key="i">
      <v-row class="align-center py-3">
        <v-col cols="12" md="4" lg="3" class="pr-4 text-center">
          <v-avatar size="190">
            <v-img :src="person.image" />
          </v-avatar>
        </v-col>
        <v-col cols="12" md="8" lg="9">
          <div class="text-h5">
            {{ person.name }}
          </div>
          <div v-if="person.title" class="text-h6 secondary--text">
            {{ person.title }}
          </div>
          <div class="text-body-1 mt-2">
            {{ person.bio }}
          </div>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'OfficerList',
  props: {
    people: {
      type: Array,
      required: true
    },
    title: {
      type: String,
      required: true
    }
  }
}
</script>
