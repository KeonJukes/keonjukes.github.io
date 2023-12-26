<script setup>
import RobotIcon from './icons/RobotIcon.vue'
import GithubIcon from './icons/GithubIcon.vue'
import LinkedInIcon from './icons/LinkedInIcon.vue'

function openInNewTab(url) {
  window.open(url, '_blank', 'noreferrer')
}
</script>

<template>
  <div class="profile-container">
    <span class="circle"></span>
    <div class="thunderbolt">
      <div class="shape1"></div>
    </div>
    <h1 class="profile-header-1">Keon Jukes</h1>
    <span>
      <h2>
        Software Engineer
        <robot-icon class="robot-icon" />
      </h2>
    </span>
    <p class="profile-p">
      I am a frontend focused software engineer, trained in fullstack web development, and currently
      work for Dolby.io helping deliver great user interfaces (UI) to customers all around the
      world.
    </p>
    <div class="profile-contact">
      <linked-in-icon
        class="social-icon"
        @click="openInNewTab('https://linkedin.com/in/keon-jukes')"
      />
      <github-icon class="social-icon" @click="openInNewTab('https://github.com/KeonJukes')" />
    </div>
  </div>
</template>

<style scoped>
.profile-container {
  margin-right: 50px;
  position: fixed;
  z-index: 2;
  width: 300px;
  top: 0;
  padding: 2rem;
}

@media screen and (max-width: 1023px) {
  .profile-container {
    margin-right: 50px;
    width: 300px;
    padding: 2rem;
    position: relative;
    z-index: 0;
  }
}

.circle {
  height: 150px;
  width: 150px;
  background-image: url('../../Keon.png');
  background-size: cover;
  background-position-x: -20px;
  background-repeat: no-repeat;
  border-radius: 50%;
  display: inline-block;
}

.profile-header-1 {
  color: #8dc931;
}

.profile-p {
  font-weight: 400;
  opacity: 75%;
}

.thunderbolt {
  display: flex;
  margin-top: -55px;
  width: 50px;
}
.thunderbolt .shape1 {
  position: relative;
  width: 0;
  height: 0;
  border-bottom: 60px solid purple;
  border-left: 30px solid transparent;
  transform: skewX(333deg) translate(-50%, -50%);
}

.thunderbolt .shape1::before {
  content: '';
  position: absolute;
  bottom: -110px;
  right: -20px;
  width: 0;
  height: 0;
  border-top: 60px solid purple;
  border-right: 30px solid transparent;
}

.thunderbolt:hover {
  &.thunderbolt .shape1 {
    border-bottom: 60px solid #8dc931;
    animation-name: thunderbolt-strike;
    animation-duration: 1s;
  }

  &.thunderbolt .shape1::before {
    border-top: 60px solid #8dc931;
  }
}

@keyframes thunderbolt-strike {
  0% {
    transform: skewX(-25deg) translate(-50%, -50%);
  }
  50% {
    transform: skewX(-35deg) translate(-50%, -50%);
  }
  100% {
    transform: skewX(-25deg) translate(-50%, -50%);
  }
}

.robot-icon {
  height: 15px;
  width: 15px;
  position: relative;
  top: 2px;
}

.profile-contact {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin-top: 20px;
}

.social-icon {
  height: 50px;
  width: 50px;
  margin-right: 5px;
  cursor: pointer;
  color: #ebebeba3;
}

.social-icon:hover {
  color: #8dc931;
}

@media (prefers-color-scheme: light) {
  .social-icon {
    color: #2c3e50;
  }
}
</style>
