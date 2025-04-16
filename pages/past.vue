<template>
  <div>
    <v-container>
      <h2 class="text-md-h2 text-h3 text-center">
        People behind ParagonX Academy
      </h2>
      <div style="width: 80px; height: 4px" class="my-4 secondary mx-auto" />
    </v-container>
    <officer-list :people="people" title="Past Officers" />
  </div>
</template>

<script>
export default {
  name: 'PastPage',
  data () {
    return {
      people: [
        {
          name: 'Joe Li',
          title: 'Founder, Stanford \'28',
          image: '/images/bio/joe.png',
          bio: 'Joe graduated from the Harker School in 2024. He is a USACO Finalist, USAPhO Gold Medalist, and 4x AIME qualifier. His CS journey began in the fall of 2017, when he first started learning C++ with X-Camp. In his free time, he plays violin and does karate.'
        },
        {
          name: 'Austin Geng',
          title: 'Massachusetts Institute of Technology \'28',
          image: '/images/bio/austin.jpg',
          bio: 'Austin Geng graduated from the Benjamin Franklin High School in 2024. He is an International Olympiad in Informatics Gold Medalist and Math Olympiad Program invitee and has narrowly missed a perfect AMC10. In both math and competitive programming, he especially enjoys ad hoc problems. In his free time, he likes to code (unrelatedly in JavaScript) and play video games.'
        },
        {
          name: 'Aniketh Tummala',
          title: 'Berkeley \'28',
          image: '/images/bio/aniketh.jpg',
          bio: 'Aniketh graduated from The Harker School in 2024. As well as being a USAPhO Silver medalist and top 50th in the nation in the Physics Bowl, he is a USACO Platinum contestant and 4 times AIME qualifier. In his free time, he enjoys taking his two dogs for walks around his neighborhood and playing the piano.'
        },
        {
          name: 'Harry Chen',
          title: 'California Institute of Technology \'28',
          image: '/images/bio/harry.jpg',
          bio: 'Harry graduated from Northwood High School in Irvine in 2024. He competed in USACO Platinum and has experience in full-stack web development. Harry also was involved with NLP research. In his free time Harry likes to play tennis.'
        },
        {
          name: 'Thomas Liu',
          title: 'Massachusetts Institute of Technology \'28',
          image: '/images/bio/thomas.jpg',
          bio: 'Thomas graduated from The Harker School in 2024. Fluent in C++, he enjoys competitive programming and is a USACO Finalist. In his spare time he enjoys playing video games and solving coding problems. He also dabbles in web development and AI.'
        },
        {
          name: 'Gautam Bhooma',
          title: 'Berkeley \'28',
          image: '/images/bio/gautam.jpg',
          bio: 'Gautam graduated from the Harker School in 2024. He is a National Top 300 Broadcom MASTERS Semifinalist after winning the Grand Prize of the Synopsys Championship in 2020. As the captain of the Harker Science Bowl team, he led his team to advance to the 2020 Science Bowl National Championships.'
        },
        {
          name: 'Arjun Gurjar',
          title: 'Berkeley \'28',
          image: '/images/bio/arjung.jpg',
          bio: 'Arjun Gurjar graduated from The Harker School in 2024. In addition to being a nationalist in the North South Science Bee, he is passionate about biology and has many years of experience in teaching students as well as conducting wet lab research. Apart from studying for USABO, Arjun likes editing videos, going on walks, and listening to music.'
        },
        {
          name: 'Kevin Zhang',
          title: 'University of Illinois Urbana-Champaign \'28',
          image: '/images/bio/kevin.png',
          bio: 'Kevin graduated from The Harker School in 2024. Besides studying computer science and physical sciences, he is also interested in arts and design with experience in digital mediums such as Photoshop and Canva. He was also a graphic designer for the Harker Programming Club and produced media for his school’s journalism program too. In his free time, he enjoys photo and video editing, as well as playing and watching basketball.'
        },
        {
          name: 'Dustin Miao',
          title: 'Carnegie Melon University \'28',
          image: '/images/bio/dustin.jpg',
          bio: 'Dustin graduated from the Harker School in 2024. He is in USACO\'s platinum division and a master on Codeforces, and is also interested in web development and artificial intelligence. In his spare time, he enjoys playing cello.'
        },
        {
          name: 'Arnav Swaroop',
          title: 'Berkeley \'28',
          image: '/images/bio/arnav.png',
          bio: 'Arnav Swaroop graduated from The Harker School in 2024. He enjoys Physics, Earth+Space Science, and biology. He is a USESO finalist, a USABO semifinalist, and has other STEM accolades in the above fields. He won the Regional Science Bowl in 2020, and was part of Harker\'s High School Science Bowl A Team and a senior Middle School Science Bowl coach. When not studying science, he works on his diverse array of research projects ranging from astrophysics to biochemistry.'
        },
        {
          name: 'Henry Yao',
          title: 'Johns Hopkins University \'28'
          image: '/images/bio/henry.png',
          bio: 'Henry graduated from Lynbrook High School in 2024. He is passionate about STEM overall, and has won USAJMO HM and AMC10 DHR three times, and came close to USAPHO along with 5\'s in most AP Physics content. He is also passionate about STEM research and has taught and TA\'d classes at Alphastar and other summer camps. When he isn\'t grinding school, Henry enjoys biking, eating food, and listening to music.'
        },
        {
          name: 'Andrew Xie',
          image: '/images/bio/andrewxie.jpg',
          bio: 'Andrew (Weian) Xie is a senior at The Hotchkiss School in Connecticut. An avid fan of math contests, he has qualified for the AIME 4 times, USAJMO 2 times, where he earned Top Winner and attended MOP in 2023. He is very passionate about promoting mathematical interest in younger kids, especially in under-represented communities, having co-founded a middle school math competition sponsored by his school, as well as AoPS and AwesomeMath. Outside of math, he enjoys playing the piano, reading poetry, cross country practice, and listening to R&B.'
        },
        {
          name: 'Andrew Liang',
          image: '/images/bio/andrew.png',
          bio: 'Andrew Liang is a senior at the Harker School. He is a USACO Gold contestant and International Science and Engineering Fair (ISEF) Finalist. He enjoys teaching other students and helping them discover their own passions. In his spare time, he likes to play chess and listen to classical music.'
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
      title: 'Past Officers',
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
