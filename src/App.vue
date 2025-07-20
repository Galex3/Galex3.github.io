<template>
  <NavBar />
  <main class="container py-5">
    <!-- <header>
      <div class="form-check form-switch">
        <input class="form-check-input" type="checkbox" role="switch" id="switchCheckDefault" v-model.lazy="darkMode" :aria-checked="darkMode" @changed="darkMode = !darkMode" switch>
        <label class="form-check-label" for="switchCheckDefault">{{ darkMode ? 'Light Mode' : 'Dark Mode' }}</label>
      </div>
      <button class="btn btn-sm btn-primary" @click="printCV">Print CV</button>
    </header> -->
    <Header :name="name" :title="title" :summary="summary" />
    <Contact :contact="contact" />
    <Experience :experience="experience" />
    <Education :education="education" />
    <Skills :skills="skills" />
    <Projects :projects="projects" />
    <Languages :languages="languages" />
    <SoftSkills :soft-skills="softSkills" />
  </main>
</template>

<script setup>
import Header from './components/HeaderSection.vue'
import Contact from './components/ContactSection.vue'
import Experience from './components/ExperienceSection.vue'
import Education from './components/EducationSection.vue'
import Skills from './components/SkillsSection.vue'
import Projects from './components/ProjectsSection.vue'
import Languages from './components/LanguagesSection.vue'
import SoftSkills from './components/SoftSkills.vue'
import NavBar from './components/NavBar.vue'

const name = 'Gustavo Silva'
const title = 'Software Engineer'
const summary =
  'Multilingual and experienced software engineer seeking new challenges and learning opportunities!'

const contact = {
  email: 'gustavoalex9@hotmail.com',
  phone: '+44 7784 704505',
  location: 'Nottingham, UK',
  linkedin: 'https://linkedin.com/in/galexs',
  github: 'https://github.com/Galex3',
}

const experience = [
  {
    role: 'Graduate Software Developer',
    company: 'The Bank of New York Mellon Corporation',
    duration: 'Aug 2022 – Sep 2023',
    description:
      'Worked in cross-functional teams to build and secure frontend/backends, participate in Agile events, and improve stakeholder communication.',
  },
  {
    role: 'Web Developer',
    company: 'Unumbox Ltd',
    duration: 'Sep 2020 – May 2022',
    description:
      'Built websites using HTML, CSS, PHP, and JS, created APIs with NodeJS, managed support tickets, and used GitHub and ClickUp for dev ops.',
  },
]

const education = [
  {
    degree: "MSci Computer Science (Integrated Master's)",
    institution: 'University of Birmingham',
    year: '2018 – 2022',
    details: [
      "Smart Unlock (Master's Project)",
      'Bribery&Corruption strategy game',
      'Virtual Psychologist (UML app)',
      'Human-Robot interaction system using ROS, OpenCV, CNNs and speech recognition',
    ],
  },
]

const skills = [
  'JavaScript',
  'Vue.js',
  'TypeScript',
  'Angular',
  'Flutter',
  'Java',
  'Python',
  'PHP',
  'C',
  'VB.NET',
  'SQL',
  'MongoDB',
  'Oracle',
  'MariaDB',
  'Bash',
  'Git',
  'CI/CD',
  'Agile/Scrum',
  'Jenkins',
  'UML',
]

const projects = [
  {
    name: 'Smart Unlock',
    description:
      'Smart lock project enabling global access using Flutter, Python, Bash, SSH, and IP routing.',
    link: '#',
  },
  {
    name: 'Bribery&Corruption',
    description:
      'Strategy game in Java/JavaFX using H2 database, simulating election bribery dynamics.',
    link: '#',
  },
  {
    name: 'sensAI',
    description:
      'AI-based education tailoring platform sponsored by IBM & University of Birmingham.',
    link: '#',
  },
  {
    name: 'Condutor Seguro',
    description:
      "VB.NET app for driver's license exam prep with SQLite backend and promotional site.",
    link: '#',
  },
]

const languages = [
  { name: 'Portuguese', level: 'Native Proficiency' },
  { name: 'English', level: 'Bilingual Proficiency' },
  { name: 'Spanish', level: 'Limited Working Proficiency' },
]

const softSkills = [
  'Proactivity',
  'Resiliency',
  'Teamwork',
  'Leadership',
  'Time Management',
  'Project Management',
  'Research',
  'Creativity',
]
</script>

<style>
  @media print {
    nav, button, .btn { display: none !important; }
    section { page-break-inside: avoid; }
  }

  a {
    text-decoration: none;
  }
</style>