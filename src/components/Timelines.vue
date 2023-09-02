<template>
  <div class="timeline mt-5">
    <h5 class="text-h5 text-uppercase text-center text-deep-purple-accent-1">Education & work</h5>
    <v-timeline class="mt-5">
      <v-timeline-item v-for="timeline in timelines" :key="timeline.id" :dot-color="timeline.color"
                       :icon="timeline.icon" size="large">
        <template v-slot:opposite>
          <div :class="`pt-1 headline font-weight-bold text-button text-${timeline.color}`"
               v-text="timeline.period"></div>
        </template>
        <div>
          <h2 :class="`mt-n1 headline font-weight-light mb-4 text-${timeline.color}`">{{ timeline.title }}</h2>
          <h5 :class="`text-button text-${timeline.color}`">{{ timeline.position }}</h5>
          <span class="text-subtitle-2">{{ timeline.description }}</span>
        </div>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>

<script setup>
import { defineComponent, reactive } from 'vue';

defineComponent({
  name: 'Timelines'
})

const timelines = reactive([
  {
    id: 0,
    icon: 'mdi-book-education',
    color: 'cyan lighten-1',
    title: 'National Polytechnical University of Armenia',
    position: 'Software Engineer',
    period: 'SEP 2015 — JUN 2021',
    description: 'Bachelor of Software Engineer'
  },
  {
    id: 1,
    icon: 'mdi-briefcase-variant',
    color: 'amber darken-1',
    title: 'Serious Web',
    position: 'Student',
    period: 'JAN — AUG 2021',
    description: 'Build landing pages & make games'
  },
  {
    id: 2,
    icon: 'mdi-briefcase-variant',
    color: 'blue-darken-3',
    title: 'DEEP Agency',
    position: 'Front-end developer',
    period: 'JUN — OCT 2021',
    description: 'Build landing pages & Wordpress projects'
  },
  {
    id: 3,
    icon: 'mdi-briefcase-variant',
    color: 'blue-grey',
    title: 'Serious Web',
    position: 'Full-stack developer',
    period: 'OCT 2021 — DEC 2022',
    description: 'API integration to e-commerce based on PHP Laravel framework'
  },
  {
    id: 4,
    icon: 'mdi-briefcase-variant',
    color: 'deep-orange-lighten-1',
    title: 'Cretrix',
    position: 'Back-end developer',
    period: 'DEC 2022 — NOWADAYS',
    description: 'Developing the big business application with Ruby on Rails'
  },
])
</script>