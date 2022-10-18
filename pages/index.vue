<template>
  <div>
    <v-container class="text-center">
      <h1 class="text-md-h1 text-h3  mt-md-6">
        Quality <span class="primary--text">STEM education</span> for our <span class="primary--text">community</span>
      </h1>
      <div class="grey--text text--lighten-2 mt-4 text-body-1">
        ParagonX Academy is a 501(c)(3) student-led non-profit organization that strives to provide high-quality, readily available STEM education to everyone in need through free curricula.
      </div>
      <div class="mt-6">
        <v-btn x-large depressed to="/events" color="primary" class="my-1 mr-sm-1 w-full w-sm-auto">
          Events and Courses
        </v-btn>
        <v-btn x-large outlined href="https://discord.com/invite/kSXnnMm244" target="_blank" class="my-1 ml-sm-1 w-full w-sm-auto">
          Join Discord
        </v-btn>
      </div>
    </v-container>

    <v-container class="mt-6">
      <v-row>
        <v-col
          v-for="(item, i) in features"
          :key="i"
          cols="12"
          md="4"
        >
          <v-card class="py-4 px-2">
            <v-responsive max-width="300" class="mx-auto text-center">
              <div class="mb-2">
                <v-icon class="text-h1" color="primary">
                  {{ item.icon }}
                </v-icon>
              </div>
              <div class="text-h5 mt-3">
                {{ item.title }}
              </div>
              <div class="mt-2 text-body-2">
                {{ item.description }}
              </div>
            </v-responsive>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <v-container class="mt-4">
      <h3 class="text-md-h3 text-h4 text-center">
        Features of our classes
      </h3>
      <div class="mt-6">
        <div
          v-for="(item, i) in courseFeatures"
          :key="i"
          class="mt-4"
        >
          <v-card class="py-4 px-2">
            <div class="d-flex">
              <div class="mr-2">
                <v-sheet
                  color="primary"
                  rounded
                  class="pa-2"
                  style="margin-top: 3px"
                  dark
                >
                  <v-icon>{{ item.icon }}</v-icon>
                </v-sheet>
              </div>
              <div>
                <div class="text-h5 font-weight-bold">
                  {{ item.title }}
                </div>
                <div class="font-weight-regular mt-1">
                  {{ item.description }}
                </div>
              </div>
            </div>
          </v-card>
        </div>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      features: [{
        icon: 'mdi-cast-education',
        title: 'Online Classes',
        description: 'We teach online courses on topics such as math, computer science, physics, chemistry, and more! By providing online education, we hope that people from around the world can easily access our classes for free.'
      }, {
        icon: 'mdi-bookmark-box-multiple',
        title: 'Teaching at the Library',
        description: 'We also teach classes in local libraries, with the goal of directly impacting our community and establishing a personal relationship with our students. Direct communication with an instructor and small class sizes make the learning process much easier.'
      }, {
        icon: 'mdi-account-voice',
        title: 'Speaker Events',
        description: 'We invite industry professionals, professors, and national science competition winners to share their knowledge and experience with our students.'
      }],
      courseFeatures: [{
        icon: 'mdi-medal',
        title: 'Award-Winning Instructors',
        description: 'Our instructors are some of the highest-ranking high school students in nationwide math and science competitions, guaranteeing that our course content is of the highest-quality.'
      }, {
        icon: 'mdi-message-text',
        title: 'Direct Communication',
        description: 'Throughout the week, students have the opportunity to directly communicate with our instructors and ask questions via our Discord server.'
      }, {
        icon: 'mdi-file-tree',
        title: 'Structured Curriculum and Homework',
        description: 'This fall, our courses consist of eight classes, and the curriculum spanning these classes have been carefully cultivated by our instructors to maximize the usefulness and quality of knowledge that students will gain. Homework will also be assigned after each class. '
      }]
    }
  },
  head () {
    return {
      title: 'Home',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'ParagonX Academy is a 501(c)(3) student-led non-profit organization that strives to provide high-quality, readily available STEM education to everyone in need through free curricula.'
        }
      ]
    }
  }
}
</script>
