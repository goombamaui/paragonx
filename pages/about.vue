<template>
  <div>
    <v-container>
      <h2 class="text-h2 text-center">
        People behind ParagonX
      </h2>
      <div style="width: 80px; height: 4px" class="my-4 white mx-auto" />
    </v-container>
    <v-container>
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
            <div class="text-h6 secondary--text">
              {{ person.title }}
            </div>
            <div class="text-body-1 mt-2">
              {{ person.bio }}
            </div>
          </v-col>
        </v-row>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  data () {
    return {
      people: [
        {
          name: 'Joe Li',
          title: 'President',
          image: '/images/bio/joe.jpg',
          bio: 'Joe is a junior at the Harker School. He is a USACO Finalist, USAPHO Bronze Medalist, and 3x AIME qualifier. His CS journey began in the fall of 2017, when he first started learning C++ with X-Camp. In his free time, he plays violin and does karate.'
        },
        {
          name: 'Austin Geng',
          title: 'Vice President of Math',
          image: '/images/bio/austin.jpg',
          bio: 'Austin Geng is a junior at Benjamin Franklin High School. He is a USACO finalist and Math Olympiad Program invitee and has narrowly missed a perfect AMC10. In both math and competitive programming, he especially enjoys ad hoc problems. In his free time, he likes to code (unrelatedly in JavaScript) and play video games.'
        },
        {
          name: 'Aniketh Tummala',
          title: 'Vice President of Physics',
          image: '/images/bio/aniketh.jpg',
          bio: 'Aniketh is a junior at the Harker School. As well as being a USAPhO qualifier, USACO Platinum contestant, and holder of multiple years\' worth of distinguished honor rolls on the AMCs, he also heads multiple AI initiatives. In his free time, he enjoys walking his dogs around his neighborhood and playing the piano.'
        },
        {
          name: 'Harry Chen',
          title: 'Vice President of Tech',
          image: '/images/bio/harry.jpg',
          bio: 'Harry is a junior at Northwood High School in Southern California. First exposed to programming in 6th grade, Harry enjoys designing complex systems and creating solutions to challenging problems. Besides being an active competitive programmer for three years, Harry has experience in full-stack web development and coding enterprise applications.'
        },
        {
          name: 'Thomas Liu',
          title: 'Vice President of CS',
          image: '/images/bio/thomas.jpg',
          bio: 'Thomas is a junior at the Harker School. Fluent in C++, he enjoys competitive programming and is a USACO Platinum competitor. In his spare time he enjoys playing video games and solving coding problems. He also dabbles in web development and AI.'
        },
        {
          name: 'Gautam Bhooma',
          title: 'Vice President of Chemistry',
          image: '/images/bio/gautam.jpg',
          bio: 'Gautam is a junior at the Harker School who enjoys science. He is a National Top 300 Broadcom MASTERS Semifinalist after winning the Grand Prize of the Synopsys Championship in 2020. As the captain of the Harker Science Bowl team, he led his team to advance to the 2020 Science Bowl National Championships.'
        },
        {
          name: 'Alex Huang',
          title: 'Vice President of Events',
          image: '/images/bio/alex.jpg',
          bio: 'Alex Huang is a sophomore at The Harker School who is a 2021 MathCounts National Round qualifier and two-time AIME qualifier. Fluent in C++, Java, and Python, he is interested in both competitive programming and machine learning research. In his free time, he likes reading historical fiction and doing speech and debate.'
        }
      ]
    }
  }
}
</script>
