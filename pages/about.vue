<template>
  <div>
    <v-container>
      <h2 class="text-md-h2 text-h3 text-center">
        People behind ParagonX Academy
      </h2>
      <img src="/images/group_photo.png" alt="Group photo of ParagonX Academy team" class="group-photo">
    </v-container>
    <officer-list :people="executive" title="Executive Team" />
    <officer-list :people="math" title="Mathematics Officers" />
    <officer-list :people="cs" title="Computer Science Officers" />
    <officer-list :people="physics" title="Physics Officers" />
    <officer-list :people="chem" title="Chemistry Officers" />
    <officer-list :people="bio" title="Biology Officers" />
    <officer-list :people="outreach" title="Outreach Team" />
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  data () {
    return {
      executive: [
        {
          name: 'Alex Huang',
          title: 'Co-President',
          image: '/images/bio/alex.jpg',
          bio: 'Alex Huang is a senior at The Harker School who is a 2021 MathCounts National Round qualifier, four-time AIME qualifier, participant in The Ross Mathematics Program 2023 and 2024, and PRIMES-USA 2024 researcher. Fluent in C++, Java, and Python, he enjoys applying scientific machine learning to elucidate biophysical processes. To disseminate his knowledge to aspiring students, he has led volunteer teaching initiatives and has won the President\'s Volunteer Service Gold Award three times. In his free time, he enjoys playing bridge and engaging friends in thought-provoking conversations.'
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
          bio: 'Jacqueline Huang is a senior at the Harker School. She is a USAPhO medalist and 4x AIME qualifier and is interested in applied physics. She has several years of experience in teaching math and science, and she enjoys hiking and reading in her free time.'
        },
        {
          name: 'Aarush Vailaya',
          image: '/images/bio/aarush.jpg',
          title: 'Vice President',
          bio: 'Aarush Vailaya is a senior at the Harker School. He is a 5 time qualifier of AIME, USAMO gold medalist, won 1st place in both the Synopsys Physical Sciences & Engineering as well as the Bay Area Math Olympiad, a USAMTS gold medalist, and competed in many math events, including the Stanford Math Tournament, AMC 10, and AIME. He also participated in the HCSSiM and SUMaC summer programs, and does math research through PRIMES-USA. While not doing math, he enjoys working on random coding projects, grinding Wynncraft, and playing piano.'
        }
      ],
      math: [
        {
          name: 'Neil Krishnan',
          image: '/images/bio/neil.jpg',
          title: 'Head of Math',
          bio: 'Neil Krishnan is a senior at The Harker School. In addition to getting 1st award in Synopsys Physical Sciences & Engineering and qualifying for CSEF and Broadcom Masters, he has done a lot of math as a five-time AIME qualifier, USAMO silver medalist, USAMTS gold winner (near perfect score), and recipient of multiple distinguished honorable mentions in BMT. He has also participated in in math summer programs, namely Hampshire College Summer Studies in Mathematics and USA-Canada MathCamp. Neil also likes doing mathematical research on friends-and-stranger graphs and graph connectivity. In his free time, he enjoys playing piano and doing NYT mini crosswords (and the regular if he feels smart that day).'
        },
        {
          name: 'Kallie Wang',
          image: '/images/bio/kallie.png',
          bio: 'Kallie Wang is a junior at the Harker School who is passionate about math and the sciences. She won a USAJMO honorable mention award in 2024 and is a 4x AIME qualifier, 3x Math Prize for Girls qualifier, and USAPhO semifinalist. This summer, Kallie participated in SUMaC. In 2022, she earned a perfect score on the AMC 8. She has won multiple awards at the Synopsys Science Fair and the California Science and Engineering Fair, and has been named a Top 300 Broadcom MASTER for her research twice. In her free time, she enjoys dancing and reading.'
        },
        {
          name: 'Hengrui Liang',
          image: '/images/bio/hengrui.png',
          bio: 'Hengrui is a sophomore at The Harker School. He is a USAMO medalist, USAJMO Winner, and a BMT and SMT Distinguished HM. In his free time, he enjoys playing chess and board games, reading science magazines, and hiking.'
        },
        {
          name: 'Anushka Polapally',
          image: '/images/bio/anushka.png',
          bio: 'Anushka Polapally is a junior at Obra D. Tompkins High School in Katy, Texas. She is an AIME qualifier and USACO Silver qualifier, along with being an officer of her school’s math club. Anushka is very passionate about teaching competition math to others, shown by her contribution to forming a contest math team and classes at her high school. In her free time, you can find Anushka listening to music, playing with her dog, and eating food with her friends.'
        },
        {
          name: 'Arjun Joisha',
          image: '/images/bio/arjunj.png',
          bio: 'Arjun Joisha is a junior at the Lynbrook High School. He is a 3 time AIME qualifier, won a bronze medal twice and a silver medal once at the PiMC, and continues to compete in several other regional and college mathematics competitions, including the Stanford Math Tournament and the Berkeley Math Tournament. When not working on math competitions, he also enjoys competitive programming, and has reached USACO Gold. In his free time, you can find him hanging out with his friends, reading interesting math articles, or playing chess or Minecraft.'
        }
      ],
      cs: [
        {
          name: 'Yash Belani',
          title: 'Head of Computer Science',
          image: '/images/bio/yash.png',
          bio: 'Yash Belani is a sophomore at the Harker School. He is competing in the USACO Platinum with C++. In his free time, he enjoys playing video games, basketball, or solving problems.'
        },
        {
          name: 'Ryan Miao',
          image: '/images/bio/ryan.png',
          bio: 'Ryan is a sophomore at The Harker School. He is an AIME qualifier, USNCO national qualifier, USACO Gold Division competitor, and has experience in Java and Python. He is also interested in Neuroscience and Artificial Intelligence and enjoys playing tennis and dancing in his free time.'
        },
        {
          name: 'Ellie Zhou',
          image: '/images/bio/ellie.png',
          bio: 'Ellie is a sophomore at The Harker School. She is competing in USACO gold, has qualified for AIME several times, and led a team making it to the Wharton Global High School Investment Competition finale. In her free time, she loves problem-solving, swimming, dancing, and playing with her dog.'
        },
        {
          name: 'Samuel Tong',
          image: '/images/bio/samuel.png',
          bio: 'Samuel is a junior at The Harker School. He competes in the USACO Gold division, and he uses his expertise in computer science on bioinformatics and drug reaction models. Samuel is a retired fencer, and he loves watching dramas and walking his dog.'
        },
        {
          name: 'Vaishnav Krishnan',
          image: '/images/bio/vaishnav.png',
          bio: 'Vaishnav is a junior at Obra D. Tompkins High School in Katy, Texas. He represents his school in UIL Computer Science and is currently competing in USACO Gold. He is very passionate about teaching computer science and enjoys learning advanced techniques in computer science such as centroid decomposition and treaps. In his free time, he likes playing music and working out at the gym.'
        }
      ],
      physics: [
        {
          name: 'Pascal Qin',
          title: 'Head of Physics',
          image: '/images/bio/pascal.png',
          bio: 'Pascal Qin is a sophomore at The Harker School. He has qualified for AIME and USACO Silver, earned silver at USAPhO, and earned bronze at the National Astronomy Competition. Pascal has studied physics for two years now and has participated in several physics contests, such as USAYPT and Physics Brawl. In his free time, he enjoys playing basketball and listening to music.'
        },
        {
          name: 'Cyrus Ghane',
          image: '/images/bio/cyrus.png',
          bio: 'Cyrus Ghane is a junior at The Harker School. He has earned an honorable mention on the USAPhO and qualified for the AIME twice. He is especially interested in the intersection of physics and neuroscience and enjoys playing soccer and the guitar in his free time.'
        },
        {
          name: 'Karthik Veeramallu',
          image: '/images/bio/karthik.png',
          bio: 'Karthik Veeramallu is a junior at Obra D. Tompkins High School in Katy, Texas, who is an AIME qualifier, USAPhO qualifier, the president of his school\'s physics club, and an officer of his school\'s math club. Fluent in Java, he is interested in building projects and modeling real world scenarios. In his free time, he enjoys working his job, volunteering, and teaching independently.'
        },
        {
          name: 'Harshil Nukala',
          image: '/images/bio/harshil.png',
          bio: 'Harshil Nukala is a junior at Dougherty Valley High School. He is really interested in multiple STEM subjects and participated in many competitions from AMC and AIME to F=ma and USACO. Outside of olympiads, he is interested in the field of positive geometry. Harshil has many years of experience in teaching and loves to help the younger generation. In his free time, he likes to go on bike rides, play badminton, and practice carnatic singing.'
        },
        {
          name: 'Lucas Wu',
          image: '/images/bio/lucas.png',
          bio: 'Lucas Wu is a freshman at The Harker School. He is an AIME Qualifier, won Honorable Mention at the Synopsys Science and Engineering Fair, and earned an honorable mention at USAPhO. Lucas is deeply passionate about physics, especially Electromagnetism, and can often be found doing interesting physics problems. Outside of math and science, he plays basketball, piano, and runs outside.'
        },
        {
          name: 'Shamik Khowala',
          image: '/images/bio/shamik.png',
          bio: 'Shamik Khowala is a sophomore at the Harker School. He has qualified for AIME four times as well as participated in several college math competitions, including BMT, HMMT, and SMT. He is also part of Harker’s Science Bowl team. He has earned a bronze medal in USAPhO and a bronze in National Astronomy Competition (NAC). At school, he is an active member of the math, physical sciences, and astronomy clubs. In his free time, he loves to explore advanced math and physics topics and solve interesting problems.'
        },
        {
          name: 'Andy Long',
          image: '/images/bio/andy.webp',
          bio: 'Andy is a junior at Seven Lakes High School in Katy, Texas. He is really passionate about physics and is a 2x USAAAO semifinalist, TXSEF finalist, president of his school’s Physics Club, an officer for his school’s astronomy club, and a bronze medalist at the National Astronomy Competition. This summer he will be participating in the Astrophysics program at SSP and in his free time he really enjoys playing pickleball and going out with friends.'
        }
      ],
      chem: [
        {
          name: 'Leo Zhang',
          title: 'Head of Chemistry',
          image: '/images/bio/leo.png',
          bio: 'Leo Zhang is a sophomore at The Harker School. He has qualified for AIME two times and made it to the national level of USNCO. In his free time, he enjoys playing chess, Brawl Stars, card games, and solving difficult logic puzzles.'
        },
        {
          name: 'Kevin He',
          image: '/images/bio/kevinhe.png',
          bio: 'Kevin is a sophomore at The Harker School. He has qualified for the AIME, earned an honorable mention at USAPhO, and also takes part in other STEM related activities such as USAYPT, USNCO, and robotics where he is a design lead on the school team. In his free time, he loves to play golf, saxophone, and chess.'
        },
        {
          name: 'William Jiang',
          image: '/images/bio/william.png',
          bio: 'William is a sophomore at The Harker School. He is very passionate about physics and chemistry, participating in competitions like USAYPT, Physics Brawl, and USNCO, as well as working on research projects related to the intersection of physics, chemistry, and machine learning. In his free time, he enjoys playing chess and solving interesting physics problems.'
        }
      ],
      bio: [
        {
          name: 'Terry Xie',
          image: '/images/bio/terry.png',
          title: 'Head of Biology',
          bio: 'Terry is a junior at The Harker School who is passionate about biology and math. He is a USABO Semifinalist, and has qualified for AIME twice. In his free time, Terry enjoys reading and playing water polo.'
        },
        {
          name: 'Shreyas Kini',
          image: '/images/bio/shreyas.jpg',
          bio: 'Shreyas Kini is a junior at Obra D. Tompkins High School in Katy, Texas. He is a two time USABO Semifinalist, the president of his science olympiad and biology clubs, and has placed as a runner up in the Brain Bee Texas division. Shreyas is excited to spreading a passion for biology in others, as seen in his past experience as a director of the American Regional Biology Competition nonprofit. Outside of biology, Shreyas loves to play basketball, go on long runs, work out at the gym, and play the cello.'
        }
      ],
      outreach: [
        {
          name: 'Sophia Liu',
          image: '/images/bio/sophia.png',
          title: 'Head of Outreach',
          bio: 'Sophia Liu is a senior at The Harker School. A lover of graphic design and fine arts, she manages outreach/media for a few organizations, serves as an art editor for The Expressionist, and is a Scholastic Arts national gold and silver medalist. Aside from art, she researches childhood cognitive development and neuroscience.'
        },
        {
          name: 'Teresa Song',
          title: 'Graphic Designer',
          bio: 'Teresa Song is a freshman at the Harker School in San Jose, California. She is a national Scholastic gold medalist. In her free time, she creates haute couture-esque clothing and grinds Tetris.',
          image: '/images/bio/teresa.jpg'
        },
        {
          name: 'Akshitaa Arun',
          title: 'Officer of International Outreach',
          bio: 'Akshitaa Arun (Akshu/Ash) is a Rising Senior in Tamil Nadu, India. She has attended various math camps in India such as PROMYS INDIA 2024, RAMTP 2023, AGMNC 2022 & 2023. She is a teaching assistant Athemath, a part of the international outreach team of URBAN HARMONY PROJECT and runs NC^2! She enjoys tutoring outside school, and showing people that math can be fun! She loves puzzles (especially sudoku) and singing!',
          image: '/images/bio/akshitaa.png'
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
