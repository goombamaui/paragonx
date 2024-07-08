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
          bio: 'Aarush Vailaya is a senior at the Harker School. He is a 4 time qualifier of AIME, won 1st place in both the Synopsys Physical Sciences & Engineering as well as the Bay Area Math Olympiad, a USAMTS gold medalist, and competed in many math events, including the Stanford Math Tournament, AMC 10, AIME, and USAMTS. He also participated in the HCSSiM and SUMaC summer programs, and does math research through PRIMES-USA. While not doing math, he enjoys working on random coding projects, grinding Wynncraft, and playing piano.'
        },
        {
          name: 'Neil Krishnan',
          image: '/images/bio/neil.jpg',
          title: 'Head of Math',
          bio: 'Neil Krishnan is a senior at The Harker School. In addition to getting 1st award in Synopsys Physical Sciences & Engineering and qualifying for CSEF and Broadcom Masters, he has done a lot of math as a four-time AIME qualifier, USAMTS gold winner (near perfect score), and recipient of multiple distinguished honorable mentions in BMT. He has also participated in in math summer programs, namely Hampshire College Summer Studies in Mathematics and USA-Canada MathCamp. Neil also likes doing mathematical research on friends-and-stranger graphs and graph connectivity. In his free time, he enjoys playing piano and doing NYT mini crosswords (and the regular if he feels smart that day).'
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
          bio: 'Sophia Liu is a senior at The Harker School. A lover of graphic design and fine arts, she manages outreach/media for a few organizations, serves as an art editor for The Expressionist, and is a Scholastic Arts national gold and silver medalist. Aside from art, she researches childhood cognitive development and neuroscience.'
        },
        {
          name: 'Andrew Liang',
          title: 'Head of Computer Science',
          image: '/images/bio/andrew.png',
          bio: 'Andrew Liang is a senior at the Harker School. He is a USACO Gold contestant and International Science and Engineering Fair (ISEF) Finalist. He enjoys teaching other students and helping them discover their own passions. In his spare time, he likes to play chess and listen to classical music.'
        },
        {
          name: 'Pascal Qin',
          title: 'Head of Physics',
          image: '/images/bio/pascal.png',
          bio: 'Pascal Qin is a sophomore at the Harker School in the class of 2027. He has qualified for AIME and USAPhO, and he is currently in USACO Silver. Pascal loves to spend his time learning advanced math topics like non-Euclidean geometry, linear algebra, and differential equations, and a wide variety of physics including quantum mechanics, special relativity, and electromagnetism.'
        },
        {
          name: 'Andrew Xie',
          image: '/images/bio/andrewxie.jpg',
          bio: 'Andrew (Weian) Xie is a senior at The Hotchkiss School in Connecticut. An avid fan of math contests, he has qualified for the AIME 4 times, USAJMO 2 times, where he earned Top Winner and attended MOP in 2023. He is very passionate about promoting mathematical interest in younger kids, especially in under-represented communities, having co-founded a middle school math competition sponsored by his school, as well as AoPS and AwesomeMath. Outside of math, he enjoys playing the piano, reading poetry, cross country practice, and listening to R&B.'
        },
        {
          name: 'Kallie Wang',
          image: '/images/bio/kallie.png',
          bio: 'Kallie Wang is a junior at the Harker School who is passionate about math and the sciences. She won a USAJMO honorable mention award in 2024 and is a 4x AIME qualifier, 3x Math Prize for Girls qualifier, and USAPhO semifinalist. This summer, Kallie participated in SUMaC. In 2022, she earned a perfect score on the AMC 8. She has won multiple awards at the Synopsys Science Fair and the California Science and Engineering Fair, and has been named a Top 300 Broadcom MASTER for her research twice. In her free time, she enjoys dancing and reading.'
        },
        {
          name: 'Yash Belani',
          image: '/images/bio/yash.png',
          bio: 'Yash Belani is a sophomore at the Harker School. He recently started USACO and is competing in the USACO Silver with C++. In his free time, he enjoys playing video games, basketball, or solving problems.'
        },
        {
          name: 'Cyrus Ghane',
          image: '/images/bio/cyrus.png',
          bio: 'Cyrus Ghane is a junior at The Harker School. He has earned an honorable mention on the USAPhO and qualified for the AIME twice. He is especially interested in the intersection of physics and neuroscience and enjoys playing soccer and the guitar in his free time.'
        },
        {
          name: 'Ryan Miao',
          image: '/images/bio/ryan.png',
          bio: 'Ryan is a sophomore at The Harker School. He competes in the USACO Gold Division in C++ and had experience in Java and Python. He is also interested in Neuroscience and Artificial Intelligence and enjoys playing tennis and dancing in his free time.'
        },
        {
          name: 'Ellie Zhou',
          image: '/images/bio/ellie.png',
          bio: 'Ellie is a sophomore at The Harker School. She is competing in USACO gold, has qualified for AIME several times, and led a team making it to the Wharton Global High School Investment Competition finale. In her free time, she loves problem-solving, swimming, dancing, and playing with her dog.'
        },
        {
          name: 'James Lin',
          image: '/images/bio/james.png',
          bio: 'James Lin is a junior at The Harker School. He is a USACO platinum contestant, three-time AIME qualifier, and USAJMO qualifier. He has also competed in many math and computer science competitions, such as SMT, Teamscode, and LIT. In his free time, he reads and listens to music.'
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
