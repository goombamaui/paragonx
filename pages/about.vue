<template>
  <div>
    <v-container>
      <h2 class="text-md-h2 text-h3 text-center">
        People behind ParagonX Academy
      </h2>
      <div style="width: 80px; height: 4px" class="my-4 secondary mx-auto" />
    </v-container>
    <officer-list :people="people" title="Current Officers" />
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  data () {
    return {
      people: [
        {
          name: 'Alex Huang',
          title: 'Co-President',
          image: '/images/bio/alex.jpg',
          bio: 'Alex Huang is a senior at The Harker School who is a 2021 MathCounts National Round qualifier, three-time AIME qualifier, participant in The Ross Mathematics Program 2023 and 2024, and USAMTS Silver Prize Winner. Fluent in C++, Java, and Python, he is interested in both competitive programming and research about the applications of deep learning. In his free time, he is passionate about volunteer teaching and has won the President\'s Volunteer Service Gold Award three times.'
        },
        {
          name: 'Juliana Li',
          image: '/images/bio/juliana.png',
          title: 'Co-President',
          bio: 'Juliana Li is a senior at the Harker School. She is a 4x AIME qualifier, was invited to MathCounts Nationals, is competing in USACO Gold, and won 1st place in biology research at both the local & state science fair. In her free time, she enjoys web/app development, volunteering, and dancing.'
        },
        {
          name: 'Jacqueline Huang',
          image: '/images/bio/jacqueline.png',
          title: 'Vice President',
          bio: 'Jacqueline Huang is a senior at the Harker School. She is a USAPhO semifinalist and 3x AIME qualifier and is interested in applied physics. She has several years of experience in teaching math and science, and she enjoys hiking and reading in her free time.'
        },
        {
          name: 'Aarush Vailaya',
          image: '/images/bio/aarush.png',
          title: 'Vice President',
          bio: 'Aarush Vailaya is a senior at the Harker School. He is a 4 time qualifier of AIME, won 1st place in both the Synopsys Physical Sciences & Engineering as well as the Bay Area Math Olympiad, and competed in many math events, including the Stanford Math Tournament, AMC 10, AIME, and USAMTS. While not doing math, he enjoys working on random coding projects and playing piano.'
        },
        {
          name: 'Neil Krishnan',
          image: '/images/bio/neil.jpg',
          title: 'Head of Math',
          bio: 'Neil Krishnan is a senior at The Harker School. In addition to getting 1st award in Synopsys Physical Sciences & Engineering and qualifying for CSEF and Broadcom Masters, he has had large success in math competitions, especially Berkeley Math Tournament, AMC 10, and AIME. In his free time, he enjoys playing piano and bicycling.'
        },
        {
          name: 'Terry Xie',
          image: '/images/bio/terry.png',
          title: 'Head of Biology',
          bio: 'Terry is a junior at The Harker School who is passionate about biology and math. He is a USABO Semifinalist, and has qualified for AIME twice. In his free time, Terry enjoys reading and playing water polo.'
        },
        {
          name: 'Sophia Liu',
          image: '/images/bio/sophia.png',
          title: 'Head of Outreach',
          bio: 'Sophia Liu is a senior at The Harker School. Her research focuses on the cognitive sciences—how early childhood development shapes later cognition, and how neurodegenerative diseases may be impacted by genetic signature. Outside of research, she enjoys robotics, cross country, and art. She is passionate about fine arts and graphic design, managing media and public relations for some other organizations.'
        },
        {
          name: 'Andrew Liang',
          image: '/images/bio/andrew.png',
          bio: 'Andrew Liang is a senior at the Harker School. He is a USACO Gold contestant and International Science and Engineering Fair (ISEF) Finalist. He enjoys teaching other students and helping them discover their own passions. In his spare time, he likes to play chess and listen to classical music.'
        },
        {
          name: 'Andrew Xie',
          image: '/images/bio/andrewxie.jpg',
          bio: 'Andrew (Weian) Xie is a senior at The Hotchkiss School in Connecticut. An avid fan of math contests, he has qualified for the AIME 4 times, USAJMO 2 times, where he earned Top Winner and attended MOP in 2023. He is very passionate about promoting mathematical interest in younger kids, especially in under-represented communities, having co-founded a middle school math competition sponsored by his school, as well as AoPS and AwesomeMath. Outside of math, he enjoys playing the piano, reading poetry, cross country practice, and listening to R&B.'
        },
        {
          name: 'Kallie Wang',
          image: '/images/bio/kallie.png',
          bio: 'Kallie Wang is a junior at the Harker School who is passionate about math and the sciences. She is a 4x AIME qualifier, 3x Math Prize for Girls qualifier, and earned a perfect score on the 2022 AMC 8. She has won multiple awards at the Synopsys Science Fair and the California Science and Engineering Fair, and she has been named a 2x Top 300 Broadcom MASTER for her research. In her free time, she enjoys dancing and reading.'
        },
        {
          name: 'Yash Belani',
          image: '/images/bio/yash.png',
          bio: 'Yash Belani is a sophomore at the Harker School. He recently started USACO and is competing in the USACO Silver with C++. In his free time, he enjoys playing video games, basketball, or solving problems.'
        },
        {
          name: 'Pascal Qin',
          image: '/images/bio/pascal.png',
          bio: 'Pascal Qin is a sophomore at the Harker School in the class of 2027. He has qualified for AIME and USAPhO, and he is currently in USACO Silver. Pascal loves to spend his time learning advanced math topics like non-Euclidean geometry, linear algebra, and differential equations, and a wide variety of physics including quantum mechanics, special relativity, and electromagnetism.'
        },
        {
          name: 'Cyrus Ghane',
          image: '/images/bio/cyrus.png',
          bio: 'Cyrus Ghane is a junior at The Harker School. He has earned an honorable mention on the USAPhO and qualified for the AIME twice. He is especially interested in the intersection of physics and neuroscience and enjoys playing soccer and the guitar in his free time.'
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
