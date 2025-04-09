<script setup lang="ts">
import { onMounted } from 'vue';
import { loadFull } from "tsparticles";

const particlesInit = async (engine: any) => {
  await loadFull(engine);
};

const options = {
  background: {
    color: {
      value: "transparent",
    },
  },
  fpsLimit: 60,
  particles: {
    color: {
      value: "#3b82f6",
    },
    links: {
      color: "#3b82f6",
      distance: 150,
      enable: true,
      opacity: 0.2,
      width: 1,
    },
    move: {
      enable: true,
      speed: 2,
      direction: "none",
      random: false,
      straight: false,
      outModes: {
        default: "bounce",
      },
      attract: {
        enable: true,
        rotateX: 600,
        rotateY: 1200,
      },
    },
    number: {
      density: {
        enable: true,
        area: 800,
      },
      value: 80,
    },
    opacity: {
      value: 0.2,
    },
    shape: {
      type: "circle",
    },
    size: {
      value: { min: 1, max: 3 },
    },
  },
  detectRetina: true,
};

onMounted(async () => {
  // @ts-ignore
  await window.tsParticles.load('tsparticles', options);
});
</script>

<template>
  <div id="tsparticles" class="absolute inset-0 -z-10"></div>
</template>