<template>
 <div class="bg-[#030303] min-h-screen">
  <Header />
  <HeroSection />
  <AboutSection />
  <ExperienceAndSkill />
  <SeminarSection />
  <ProjectSection />
  <ContactSection />
  <BackToTop />
  <Footer />
 </div>
</template>
<script setup>
import { defineAsyncComponent } from 'vue';

const Header = defineAsyncComponent(() =>import('./components/Header.vue'))
const HeroSection = defineAsyncComponent(() =>import('./components/HeroSection.vue'))
const AboutSection = defineAsyncComponent(() =>import('./components/AboutSection.vue'))
const ExperienceAndSkill = defineAsyncComponent(() =>import('./components/ExperienceAndSkill.vue'))
const SeminarSection = defineAsyncComponent(() =>import('./components/SeminarSection.vue'))
const ProjectSection = defineAsyncComponent(() =>import('./components/ProjectSection.vue'))
const ContactSection = defineAsyncComponent(() =>import('./components/ContactSection.vue'))
const Footer = defineAsyncComponent(() =>import('./components/Footer.vue'))
const BackToTop = defineAsyncComponent(() =>import('./components/BackToTop.vue'))
</script>