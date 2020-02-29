<script>
export default {
  name: 'front',
  data () {
    return {
      projects: [
        {
          "title": "DIMIGOin Frontend",
          "duration": "2019 - 2020"
        },
        {
          "title": "ECHO Frontend",
          "duration": "2019 - 2020"
        },
        {
          "title": "UNICON@DIMIGO Landing Page",
          "duration": "2020"
        },
        {
          "title": "AIM@DIMIGO Landing Page",
          "duration": "2020"
        },
        {
          "title": "anythingBE@DIMIGO Landing Page",
          "duration": "2020"
        }
      ],
      prizes: [
        {
          "title": "2014 ICT 어워드 코리아 (C 프로그래밍)",
          "prize": "동상"
        },
        {
          "title": "2015 ICT 어워드 코리아 (C 프로그래밍)",
          "prize": "은상"
        },
        {
          "title": "2015 한국정보올림피아드 지역 본선",
          "prize": "동상"
        },
        {
          "title": "2016 한국정보올림피아드 지역 본선",
          "prize": "동상"
        },
        {
          "title": "2016 한국정보올림피아드 전국 대회",
          "prize": "동상"
        },
        {
          "title": "2016 제12회 전국 중학생 IT 올림피아드 (C 프로그래밍)",
          "prize": "금상"
        },
        {
          "title": "2017 전국 청소년 모의해킹대회",
          "prize": "은상"
        },
        {
          "title": "2017 Nexon Youth Programming Challenge",
          "prize": "특별상"
        },
        {
          "title": "2018 전국 청소년 모의해킹대회",
          "prize": "동상"
        },
        {
          "title": "2018 DIS CTF",
          "prize": "준우승"
        },
        {
          "title": "2018 Nexon Youth Programming Challenge",
          "prize": "특별상"
        },
        {
          "title": "2018 해킹캠프 CTF",
          "prize": "3위"
        },
        {
          "title": "2018 정보보안 경진대회 (개인전)",
          "prize": "우수상"
        },
        {
          "title": "2019 ICT 어워드 코리아 (C 프로그래밍)",
          "prize": "장려상"
        },
        {
          "title": "2019 1학년 1학기 교과우수상",
          "prize": "프로그래밍, 영어"
        },
        {
          "title": "2019 Samsung SDS - JA Korea 스마트 해커톤",
          "prize": "우수상"
        },
        {
          "title": "2019 정보보안 경진대회 (개인전)",
          "prize": "장려상"
        },
        {
          "title": "2019 정보보안 경진대회 (팀전)",
          "prize": "우수상"
        },
        {
          "title": "2019 한양대학교 안산시 청소년 프로그래밍 경진대회",
          "prize": "최우수상"
        }
      ],
      "careers": [
        "서울여자대학교 정보보호영재교육원 중등심화반 수료",
        "서울여자대학교 정보보호영재교육원 고등전문A반 수료"
      ]
    }
  }
}
</script>

<template>
  <div class='card'>
    <div class='project-wrapper'>
      <span class='category'>Projects</span>
      <ul>
        <li
          :key='`project-${i}`'
          v-for="(project, i) in projects"
          class='project'
        >
          <span>[{{ project.duration }}] {{ project.title }}</span>
        </li>
      </ul>
    </div>

    <div class='prize-wrapper'>
      <span class='category'>Prizes</span>
      <ul>
        <li
          :key='`prize-${i}`'
          v-for="(prize, i) in prizes"
          class='prize'
        >
          <span>{{ prize.title }} - {{ prize.prize }}</span>
        </li>
      </ul>
    </div>

    <div class='career-wrapper'>
      <span class='category'>Careers</span>
      <ul>
        <li
          :key='`career-${i}`'
          v-for="(career, i) in careers"
          class='career'
        >
          <span>{{ career }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.card {
  position: relative;
  width: 30em;
  height: 100%;
  background-color: #f6f6f6;
  border-radius: 15px;
  box-shadow: 20px 20px 60px #d1d1d1, -20px -20px 60px #ffffff;
  font-family: 'Inter', sans-serif;
  font-weight: 300;
  overflow-x: hidden; 
  overflow-y: scroll;
  margin-right: 10px;
}

.button {
  color: #606060;
  cursor: pointer;
  user-select: none;
}

.content-wrapper {
  position: relative;
}

.project-wrapper,
.prize-wrapper,
.career-wrapper {
  margin: 5% 0 0 5%;
  line-height: 1.5rem;
}
</style>
