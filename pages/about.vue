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
          bio: 'Joe is a rising senior at the Harker School. He is a USACO Finalist, USAPhO Gold Medalist, and 4x AIME qualifier. His CS journey began in the fall of 2017, when he first started learning C++ with X-Camp. In his free time, he plays violin and does karate.'
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
          bio: 'Harry is a junior at Northwood High School in Irvine. He currently competes in USACO Platinum and has experience in full-stack web development. Harry is also involved with NLP research. In his free time Harry likes to play tennis.'
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
        },
        {
          name: 'Arjun Gurjar',
          title: 'Vice President of Biology',
          image: '/images/bio/arjun.jpg',
          bio: 'Arjun Gurjar is a junior at The Harker School. In addition to being a nationalist in the North South Science Bee, he is passionate about biology and has many years of experience in teaching students as well as conducting wet lab research. When he isn’t studying for USABO, Arjun likes editing videos, going on walks, and listening to music.'
        },
        {
          name: 'Kevin Zhang',
          title: 'Vice President of Outreach',
          image: '/images/bio/kevin.png',
          bio: 'Kevin is a junior at the Harker School. Besides studying computer science and physical sciences, he is also interested in arts and design with experience in digital mediums such as Photoshop and Canva. He is also a graphic designer for the Harker Programming Club and produces media for his school’s journalism program too. In his free time, he enjoys photo and video editing, as well as playing and watching basketball.'
        },
        {
          name: 'Dustin Miao',
          image: '/images/bio/dustin.jpg',
          bio: 'Dustin is a junior at the Harker School who is passionate about computer science. He is in USACO\'s platinum division and a master on Codeforces, and is also interested in web development and artificial intelligence. In is spare time, he enjoys playing cello.'
        },
        {
          name: 'Henry Yao',
          image: '/images/bio/henry.png',
          bio: 'Henry is a junior at Lynbrook High School. He is passionate about STEM overall, and has won USAJMO HM and AMC10 DHR three times, and came close to USAPHO along with 5\'s in most AP Physics content. He is also passionate about STEM research and has taught and TA\'d classes at Alphastar and other summer camps.  When he isn\'t grinding school, Henry enjoys biking, eating food, and listening to music.'
        },
        {
          name: 'Neil Krishnan',
          image: '/images/bio/neil.jpg',
          bio: 'Neil Krishnan is a sophmore at The Harker School. In addition to getting 1st award in Synopsys Physical Sciences & Engineering and qualifying for CSEF and Broadcom Masters, he has had large success in math competitions, especially Berkeley Math Tournament, AMC 10, and AIME. In his free time, he enjoys playing piano and bicycling.'
        },
        {
          name: 'Arnav Swaroop',
          image: '/images/bio/arnav.png',
          bio: 'Arnav Swaroop is a Junior at the Harker School who enjoys Physics, Earth+Space Science, and biology. He is a USESO finalist,  a USABO semifinalist, and has other STEM accolades in the above fields. He won the Regional Science Bowl in 2020, and is now part of Harker\'s High School Science Bowl A Team and a senior Middle School Science Bowl coach. When not studying science, he works on his diverse array of research projects ranging from astrophysics to biochemistry.'
        },
        {
          name: 'Juliana Li',
          image: '/images/bio/juliana.png',
          bio: 'Juliana Li is a sophomore at the Harker School. She is a 3x AIME qualifier, was invited to MathCounts Nationals, is passionate about USACO, and has coded in many languages, including C++, Python, Java, LISP, and HTML & CSS. In her free time, she enjoys dancing, as she has won many awards in dance, especially ballet.'
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
