<template>
  <div>
    <v-container>
      <h2 class="text-md-h2 text-h3 text-center">
        People behind ParagonX Academy
      </h2>
      <div style="width: 80px; height: 4px" class="my-4 secondary mx-auto" />
    </v-container>
    <v-container>
      <h3 class="text-md-h3 text-h4 text-center">
        Current Officers
      </h3>
      <div v-for="(person, i) in currentPeople" :key="i">
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
      <h3 class="text-md-h3 text-h4 text-center">
        Past Officers
      </h3>
      <div v-for="(person, i) in pastPeople" :key="i">
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
      currentPeople: [
        {
          name: 'Alex Huang',
          title: 'Co-President',
          image: '/images/bio/alex.jpg',
          bio: 'Alex Huang is a junior at The Harker School who is a 2021 MathCounts National Round qualifier, two-time AIME qualifier, participant in The Ross Mathematics Program 2023, and USAMTS Bronze Prize Winner. Fluent in C++, Java, and Python, he is interested in both competitive programming and research about the applications of deep learning. In his free time, he likes reading Wikipedia articles and taking walks.'
        },
        {
          name: 'Juliana Li',
          image: '/images/bio/juliana.png',
          title: 'Co-President',
          bio: 'Juliana Li is a junior at the Harker School. She is a 3x AIME qualifier, was invited to MathCounts Nationals, is competing in USACO Gold, and has coded in many languages, including C++, Python, Java, LISP, and HTML & CSS. In her free time, she enjoys dancing, as she has won many awards in dance, especially ballet.'
        },
        {
          name: 'Jacqueline Huang',
          image: '/images/bio/jacqueline.png',
          title: 'Vice President',
          bio: 'Jacqueline Huang is a junior at the Harker School. She is a USAPhO semifinalist and 3x AIME qualifier and is interested in applied physics. She has several years of experience in teaching math and science, and she enjoys hiking and reading in her free time.'
        },
        {
          name: 'Aarush Vailaya',
          image: '/images/bio/aarush.png',
          title: 'Vice President',
          bio: 'Aarush Vailaya is a junior at the Harker School. He is a 4 time qualifier of AIME, won 1st place in both the Synopsys Physical Sciences & Engineering as well as the Bay Area Math Olympiad, and competed in many math events, including the Stanford Math Tournament, AMC 10, AIME, and USAMTS. While not doing math, he enjoys working on random coding projects and playing piano.'
        },
        {
          name: 'Neil Krishnan',
          image: '/images/bio/neil.jpg',
          title: 'Head of Math',
          bio: 'Neil Krishnan is a junior at The Harker School. In addition to getting 1st award in Synopsys Physical Sciences & Engineering and qualifying for CSEF and Broadcom Masters, he has had large success in math competitions, especially Berkeley Math Tournament, AMC 10, and AIME. In his free time, he enjoys playing piano and bicycling.'
        },
        {
          name: 'Terry Xie',
          image: '/images/bio/terry.png',
          title: 'Head of Biology',
          bio: 'Terry is a sophomore at The Harker School who is passionate about biology and math. He is a USABO Semifinalist, and has qualified for AIME twice. In his free time, Terry enjoys reading and playing water polo.'
        },
        {
          name: 'Sophia Liu',
          image: '/images/bio/sophia.png',
          title: 'Head of Outreach',
          bio: 'Sophia Liu is a junior at The Harker School. Her research focuses on the cognitive sciences—how early childhood development shapes later cognition, and how neurodegenerative diseases may be impacted by genetic signature. Outside of research, she enjoys robotics, cross country, and art. She is passionate about fine arts and graphic design, managing media and public relations for some other organizations.'
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
          name: 'Kallie Wang',
          image: '/images/bio/kallie.png',
          bio: 'Kallie Wang is a sophomore at the Harker School who is passionate about math and the sciences. She is a 4x AIME qualifier, 3x Math Prize for Girls qualifier, and earned a perfect score on the 2022 AMC 8. She has won multiple awards at the Synopsys Science Fair and the California Science and Engineering Fair, and she has been named a 2x Top 300 Broadcom MASTER for her research. In her free time, she enjoys dancing and reading.'
        },
        {
          name: 'Yash Belani',
          image: '/images/bio/yash.png',
          bio: 'Yash Belani is a freshman at the Harker School. He recently started USACO and is competing in the USACO Silver with c++. In his free time, he enjoys playing video games, basketball, or solving problems.'
        }
      ],
      pastPeople: [
        {
          name: 'Joe Li',
          title: 'President',
          image: '/images/bio/joe.png',
          bio: 'Joe graduated from the Harker School in 2024. He is a USACO Finalist, USAPhO Gold Medalist, and 4x AIME qualifier. His CS journey began in the fall of 2017, when he first started learning C++ with X-Camp. In his free time, he plays violin and does karate.'
        },
        {
          name: 'Austin Geng',
          title: 'Vice President of Math',
          image: '/images/bio/austin.jpg',
          bio: 'Austin Geng graduated from the Benjamin Franklin High School in 2024. He is an International Olympiad in Informatics Gold Medalist and Math Olympiad Program invitee and has narrowly missed a perfect AMC10. In both math and competitive programming, he especially enjoys ad hoc problems. In his free time, he likes to code (unrelatedly in JavaScript) and play video games.'
        },
        {
          name: 'Aniketh Tummala',
          title: 'Vice President of Physics',
          image: '/images/bio/aniketh.jpg',
          bio: 'Aniketh graduated from The Harker School in 2024. As well as being a USAPhO Silver medalist and top 50th in the nation in the Physics Bowl, he is a USACO Platinum contestant and 4 times AIME qualifier. In his free time, he enjoys taking his two dogs for walks around his neighborhood and playing the piano.'
        },
        {
          name: 'Harry Chen',
          title: 'Vice President of Tech',
          image: '/images/bio/harry.jpg',
          bio: 'Harry graduated from Northwood High School in Irvine in 2024. He competed in USACO Platinum and has experience in full-stack web development. Harry also was involved with NLP research. In his free time Harry likes to play tennis.'
        },
        {
          name: 'Thomas Liu',
          title: 'Vice President of CS',
          image: '/images/bio/thomas.jpg',
          bio: 'Thomas graduated from The Harker School in 2024. Fluent in C++, he enjoys competitive programming and is a USACO Finalist. In his spare time he enjoys playing video games and solving coding problems. He also dabbles in web development and AI.'
        },
        {
          name: 'Gautam Bhooma',
          title: 'Vice President of Chemistry',
          image: '/images/bio/gautam.jpg',
          bio: 'Gautam graduated from the Harker School in 2024. He is a National Top 300 Broadcom MASTERS Semifinalist after winning the Grand Prize of the Synopsys Championship in 2020. As the captain of the Harker Science Bowl team, he led his team to advance to the 2020 Science Bowl National Championships.'
        },
        {
          name: 'Arjun Gurjar',
          title: 'Vice President of Biology',
          image: '/images/bio/arjun.jpg',
          bio: 'Arjun Gurjar graduated from The Harker School in 2024. In addition to being a nationalist in the North South Science Bee, he is passionate about biology and has many years of experience in teaching students as well as conducting wet lab research. Apart from studying for USABO, Arjun likes editing videos, going on walks, and listening to music.'
        },
        {
          name: 'Kevin Zhang',
          title: 'Vice President of Outreach',
          image: '/images/bio/kevin.png',
          bio: 'Kevin graduated from The Harker School in 2024. Besides studying computer science and physical sciences, he is also interested in arts and design with experience in digital mediums such as Photoshop and Canva. He was also a graphic designer for the Harker Programming Club and produced media for his school’s journalism program too. In his free time, he enjoys photo and video editing, as well as playing and watching basketball.'
        },
        {
          name: 'Dustin Miao',
          image: '/images/bio/dustin.jpg',
          bio: 'Dustin graduated from the Harker School in 2024. He is in USACO\'s platinum division and a master on Codeforces, and is also interested in web development and artificial intelligence. In his spare time, he enjoys playing cello.'
        },
        {
          name: 'Henry Yao',
          image: '/images/bio/henry.png',
          bio: 'Henry graduated from Lynbrook High School in 2024. He is passionate about STEM overall, and has won USAJMO HM and AMC10 DHR three times, and came close to USAPHO along with 5\'s in most AP Physics content. He is also passionate about STEM research and has taught and TA\'d classes at Alphastar and other summer camps. When he isn\'t grinding school, Henry enjoys biking, eating food, and listening to music.'
        },
        {
          name: 'Arnav Swaroop',
          image: '/images/bio/arnav.png',
          bio: 'Arnav Swaroop graduated from The Harker School in 2024. He enjoys Physics, Earth+Space Science, and biology. He is a USESO finalist, a USABO semifinalist, and has other STEM accolades in the above fields. He won the Regional Science Bowl in 2020, and was part of Harker\'s High School Science Bowl A Team and a senior Middle School Science Bowl coach. When not studying science, he works on his diverse array of research projects ranging from astrophysics to biochemistry.'
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
