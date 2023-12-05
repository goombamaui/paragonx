<template>
  <div>
    <v-container>
      <h2 class="text-md-h2 text-h3 text-center">
        People behind ParagonX Academy
      </h2>
      <div style="width: 80px; height: 4px" class="my-4 secondary mx-auto" />
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
          image: '/images/bio/joe.png',
          bio: 'Joe is a senior at the Harker School. He is a USACO Finalist, USAPhO Gold Medalist, and 4x AIME qualifier. His CS journey began in the fall of 2017, when he first started learning C++ with X-Camp. In his free time, he plays violin and does karate.'
        },
        {
          name: 'Austin Geng',
          title: 'Vice President of Math',
          image: '/images/bio/austin.jpg',
          bio: 'Austin Geng is a senior at Benjamin Franklin High School. He is an International Olympiad in Informatics Gold Medalist and Math Olympiad Program invitee and has narrowly missed a perfect AMC10. In both math and competitive programming, he especially enjoys ad hoc problems. In his free time, he likes to code (unrelatedly in JavaScript) and play video games.'
        },
        {
          name: 'Aniketh Tummala',
          title: 'Vice President of Physics',
          image: '/images/bio/aniketh.jpg',
          bio: 'Aniketh is a senior at The Harker School. As well as being a USAPhO Silver medalist and top 50th in the nation in the Physics Bowl, he is a USACO Platinum contestant and 4 times AIME qualifier. In his free time, he enjoys taking his two dogs for walks around his neighborhood and playing the piano.'
        },
        {
          name: 'Harry Chen',
          title: 'Vice President of Tech',
          image: '/images/bio/harry.jpg',
          bio: 'Harry is a senior at Northwood High School in Irvine. He currently competes in USACO Platinum and has experience in full-stack web development. Harry is also involved with NLP research. In his free time Harry likes to play tennis.'
        },
        {
          name: 'Thomas Liu',
          title: 'Vice President of CS',
          image: '/images/bio/thomas.jpg',
          bio: 'Thomas is a senior at the Harker School. Fluent in C++, he enjoys competitive programming and is a USACO Finalist. In his spare time he enjoys playing video games and solving coding problems. He also dabbles in web development and AI.'
        },
        {
          name: 'Gautam Bhooma',
          title: 'Vice President of Chemistry',
          image: '/images/bio/gautam.jpg',
          bio: 'Gautam is a senior at the Harker School who enjoys science. He is a National Top 300 Broadcom MASTERS Semifinalist after winning the Grand Prize of the Synopsys Championship in 2020. As the captain of the Harker Science Bowl team, he led his team to advance to the 2020 Science Bowl National Championships.'
        },
        {
          name: 'Alex Huang',
          title: 'Vice President of Events',
          image: '/images/bio/alex.jpg',
          bio: 'Alex Huang is a junior at The Harker School who is a 2021 MathCounts National Round qualifier, two-time AIME qualifier, participant in The Ross Mathematics Program 2023, and USAMTS Bronze Prize Winner. Fluent in C++, Java, and Python, he is interested in both competitive programming and research about the applications of deep learning. In his free time, he likes reading Wikipedia articles and taking walks.'
        },
        {
          name: 'Arjun Gurjar',
          title: 'Vice President of Biology',
          image: '/images/bio/arjun.jpg',
          bio: 'Arjun Gurjar is a senior at The Harker School. In addition to being a nationalist in the North South Science Bee, he is passionate about biology and has many years of experience in teaching students as well as conducting wet lab research. When he isn’t studying for USABO, Arjun likes editing videos, going on walks, and listening to music.'
        },
        {
          name: 'Kevin Zhang',
          title: 'Vice President of Outreach',
          image: '/images/bio/kevin.png',
          bio: 'Kevin is a senior at the Harker School. Besides studying computer science and physical sciences, he is also interested in arts and design with experience in digital mediums such as Photoshop and Canva. He is also a graphic designer for the Harker Programming Club and produces media for his school’s journalism program too. In his free time, he enjoys photo and video editing, as well as playing and watching basketball.'
        },
        {
          name: 'Dustin Miao',
          image: '/images/bio/dustin.jpg',
          bio: 'Dustin is a senior at the Harker School who is passionate about computer science. He is in USACO\'s platinum division and a master on Codeforces, and is also interested in web development and artificial intelligence. In his spare time, he enjoys playing cello.'
        },
        {
          name: 'Henry Yao',
          image: '/images/bio/henry.png',
          bio: 'Henry is a senior at Lynbrook High School. He is passionate about STEM overall, and has won USAJMO HM and AMC10 DHR three times, and came close to USAPHO along with 5\'s in most AP Physics content. He is also passionate about STEM research and has taught and TA\'d classes at Alphastar and other summer camps. When he isn\'t grinding school, Henry enjoys biking, eating food, and listening to music.'
        },
        {
          name: 'Neil Krishnan',
          image: '/images/bio/neil.jpg',
          bio: 'Neil Krishnan is a junior at The Harker School. In addition to getting 1st award in Synopsys Physical Sciences & Engineering and qualifying for CSEF and Broadcom Masters, he has had large success in math competitions, especially Berkeley Math Tournament, AMC 10, and AIME. In his free time, he enjoys playing piano and bicycling.'
        },
        {
          name: 'Arnav Swaroop',
          image: '/images/bio/arnav.png',
          bio: 'Arnav Swaroop is a senior at the Harker School who enjoys Physics, Earth+Space Science, and biology. He is a USESO finalist, a USABO semifinalist, and has other STEM accolades in the above fields. He won the Regional Science Bowl in 2020, and is now part of Harker\'s High School Science Bowl A Team and a senior Middle School Science Bowl coach. When not studying science, he works on his diverse array of research projects ranging from astrophysics to biochemistry.'
        },
        {
          name: 'Juliana Li',
          image: '/images/bio/juliana.png',
          bio: 'Juliana Li is a junior at the Harker School. She is a 3x AIME qualifier, was invited to MathCounts Nationals, is competing in USACO Gold, and has coded in many languages, including C++, Python, Java, LISP, and HTML & CSS. In her free time, she enjoys dancing, as she has won many awards in dance, especially ballet.'
        },
        {
          name: 'Jacqueline Huang',
          image: '/images/bio/jacqueline.png',
          bio: 'Jacqueline Huang is a junior at the Harker School. She is a USAPhO semifinalist and 3x AIME qualifier and is interested in applied physics. She has several years of experience in teaching math and science, and she enjoys hiking and reading in her free time.'
        },
        {
          name: 'Aarush Vailaya',
          image: '/images/bio/aarush.png',
          bio: 'Aarush Vailaya is a junior at the Harker School. He is a 3 time qualifier of AIME, won 1st place in both the Synopsys Physical Sciences & Engineering as well as the Bay Area Math Olympiad, and competed in many math events, including the Stanford Math Tournament, AMC 10, AIME, and USAMTS. While not doing math, he enjoys working on random coding projects and playing piano.'
        },
        {
          name: 'Terry Xie',
          image: '/images/bio/terry.png',
          bio: 'Terry is a sophomore at The Harker School who is passionate about biology and math. He is a USABO Semifinalist, and has qualified for AIME twice. In his free time, Terry enjoys reading and playing water polo.'
        },
        {
          name: 'Andrew Liang',
          image: '/images/bio/andrew.png',
          bio: 'Andrew Liang is a junior at the Harker School. He is a USACO Gold contestant and International Science and Engineering Fair (ISEF) Finalist. He enjoys teaching other students and helping them discover their own passions. In his spare time, he likes to play chess and listen to classical music.'
        },
        {
          name: 'Andrew Xie',
          image: '/images/bio/andrewxie.jpg',
          bio: 'Andrew (Weian) Xie is a junior at The Hotchkiss School in Connecticut. An avid fan of math contests, he has qualified for the AIME 4 times, USAJMO 2 times, where he earned Top Winner and attended MOP in 2023. He is very passionate about promoting mathematical interest in younger kids, especially in under-represented communities, having co-founded a middle school math competition sponsored by his school, as well as AoPS and AwesomeMath. Outside of math, he enjoys playing the piano, reading poetry, cross country practice, and listening to R&B.'
        },
        {
          name: 'Sophia Liu',
          image: '/images/bio/sophia.png',
          bio: 'Sophia Liu is a junior at The Harker School. Her research focuses on the cognitive sciences—how early childhood development shapes later cognition, and how neurodegenerative diseases may be impacted by genetic signature. Outside of research, she enjoys robotics, cross country, and art. She is passionate about fine arts and graphic design, managing media and public relations for some other organizations.'
        }
      ]
    }
  },
  head () {
    return {
      title: 'About',
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
