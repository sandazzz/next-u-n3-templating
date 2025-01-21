<script lang="ts" setup>
import AnnonceProject from '@/components/AnnonceProject.vue'
import CardProject from '@/components/CardProject.vue'
import TrendCard from '@/components/TrendCard.vue'

const announcements = [
  {
    title: 'Site Maintenance',
    description: `Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore
    culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim
    cupidatat excepteur officia. Reprehenderit nostrud nostrud ipsum Lorem est aliquip
    amet voluptate voluptate dolor minim nulla est proident. Nostrud officia pariatur ut
    officia. Sit irure elit esse ea nulla sunt ex occaecat reprehenderit commodo officia
    dolor Lorem duis laboris cupidatat officia voluptate. Culpa proident adipisicing id
    nulla nisi laboris ex in Lorem sunt duis officia eiusmod. Aliqua reprehenderit
    commodo ex non excepteur duis sunt velit enim. Voluptate laboris sint cupidatat
    ullamco ut ea consectetur et est culpa et culpa duis.`,
  },
  {
    title: 'Community Share Day',
    description: `Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore
    culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim
    cupidatat excepteur officia. Reprehenderit nostrud nostrud ipsum Lorem est aliquip
    amet voluptate voluptate dolor minim nulla est proident. Nostrud officia pariatur ut
    officia. Sit irure elit esse ea nulla sunt ex occaecat reprehenderit commodo officia
    dolor Lorem duis laboris cupidatat officia voluptate. Culpa proident adipisicing id
    nulla nisi laboris ex in Lorem sunt duis officia eiusmod. Aliqua reprehenderit
    commodo ex non excepteur duis sunt velit enim. Voluptate laboris sint cupidatat
    ullamco ut ea consectetur et est culpa et culpa duis.`,
  },
  {
    title: 'Updated Privacy Policy',
    description: `Lorem ipsum dolor sit amet, officia excepteur ex fugiat reprehenderit enim labore
    culpa sint ad nisi Lorem pariatur mollit ex esse exercitation amet. Nisi anim
    cupidatat excepteur officia. Reprehenderit nostrud nostrud ipsum Lorem est aliquip
    amet voluptate voluptate dolor minim nulla est proident. Nostrud officia pariatur ut
    officia. Sit irure elit esse ea nulla sunt ex occaecat reprehenderit commodo officia
    dolor Lorem duis laboris cupidatat officia voluptate. Culpa proident adipisicing id
    nulla nisi laboris ex in Lorem sunt duis officia eiusmod. Aliqua reprehenderit
    commodo ex non excepteur duis sunt velit enim. Voluptate laboris sint cupidatat
    ullamco ut ea consectetur et est culpa et culpa duis.`,
  },
]

const trends = [
  {
    avatar: 'https://robohash.org/irwi32.png?set=set4',
    username: '@tegan',
    description: 'World Peace Builder',
  },
  {
    avatar: 'https://robohash.org/ijrwi32.png?set=set4',
    username: '@morgan',
    description: 'Super cool Project',
  },
  {
    avatar: 'https://robohash.org/irw2.png?set=set4',
    username: '@kindall',
    description: 'Life Changing App',
  },
  {
    avatar: 'https://robohash.org/ireqwe2.png?set=set4',
    username: '@alex',
    description: 'No Traffic Maker',
  },
]
</script>
<template>
  <div class="container project-box">
    <section class="dashboard">
      <div class="project">
        <h4>Your Projects</h4>
        <div class="project-grid">
          <CardProject v-for="n in 6" :key="n" />
        </div>
      </div>
      <section class="side">
        <div class="announcement">
          <h4>Announcements</h4>
          <div class="background-box">
              <AnnonceProject
                v-for="(announcement, index) in announcements"
                :key="index"
                :title="announcement.title"
                :description="announcement.description"
                :isLast="index === announcements.length - 1"
              />
          </div>
        </div>
        <div>
          <h4>Trending</h4>
          <div class="background-box trending">
            <TrendCard
              v-for="(trend, index) in trends"
              :key="index"
              :avatar="trend.avatar"
              :username="trend.username"
              :description="trend.description"
            />
          </div>
        </div>
      </section>
    </section>
  </div>
</template>
