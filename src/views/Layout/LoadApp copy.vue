<script setup>
import { onMounted, ref } from 'vue';
const theme = ref(localStorage.getItem('theme') || 'dark');

</script>

<template>
  <div class="wr" :data-theme="theme">
    <div class="l">
      <!-- From Uiverse.io by Ashon-G --> 
<div class="loading">
  <svg height="48px" width="64px">
      <polyline id="back" points="0.157 23.954, 14 23.954, 21.843 48, 43 0, 50 24, 64 24"></polyline>
    <polyline id="front" points="0.157 23.954, 14 23.954, 21.843 48, 43 0, 50 24, 64 24"></polyline>
  </svg>
</div>

    </div>
  </div>
</template>

<style scoped>
.wr {
  height: 100vh;
    background: var(--background-color);
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
}
.wr .l {
  position: absolute;
  top: 48%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.pl,
.pl__worm {
  animation-duration: 3s;
  animation-iteration-count: infinite;
}

.pl {
  animation-name: bump9;
  animation-timing-function: linear;
  width: 8em;
  height: 8em;
}

.pl__ring {
  stroke: hsla(var(--hue), 10%, 10%, 0.1);
  transition: stroke 0.3s;
}

.pl__worm {
  animation-name: worm9;
  animation-timing-function: cubic-bezier(0.42, 0.17, 0.75, 0.83);
}

/* From Uiverse.io by Ashon-G */ 
/* From Uiverse.io by RaspberryBee */ 
.loading svg polyline {
  fill: none;
  stroke-width: 4;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.loading svg polyline#back {
  fill: none;
}

.loading svg polyline#front {
  fill: none;
  stroke: rgb(250, 166, 0);
  stroke-dasharray: 48, 144;
  stroke-dashoffset: 192;
  animation: dash_682 1.4s linear infinite;
}

@keyframes dash_682 {
  72.5% {
    opacity: 0;
  }

  to {
    stroke-dashoffset: 0;
  }
}


</style>
