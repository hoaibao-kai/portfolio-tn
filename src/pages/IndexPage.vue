<template>
  <q-page style="overflow: hidden;" class="flex flex-center content-center">
    <div v-if="countdown > 0">
      <div>
        <h3 class=" welcome">From your lover to happy birthday for</h3>
        <h1 class="name typing-text">Trần Thị Thảo Nguyên</h1>
        <div style="text-align: center;" class="name">{{ countdown }}</div>
      </div>
    </div>
    <iframe v-if="countdown == 0" style="width:100vw;height: 100vh;" id="preview-frame" class="preview-desktop"
      src="https://devforum.info/DEMO/phaohoa/" frameborder="0">

    </iframe>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      seconds: 5,
      intervalId: null
    };
  },
  computed: {
    countdown() {
      return this.seconds;
    }
  },
  methods: {
    startCountdown() {
      this.intervalId = setInterval(() => {
        if (this.seconds > 0) {
          this.seconds--;
        } else {
          clearInterval(this.intervalId);
        }
      }, 1000);
    }
  },
  mounted() {
    this.startCountdown();
  }
};
</script>

<style>
body {
  background-image: url("../assets/hero-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

.welcome {
  font-family: "montserrat-bold", sans-serif;
  font-size: 2.2rem;
  color: white;
  text-transform: uppercase;
  letter-spacing: .3rem;
  margin: 0 0 0.9rem 0;
}

.name {
  font-family: "montserrat-bold", serif;
  font-size: 9rem;
  line-height: 1.133;
  color: #FFF;
}

@keyframes write {
  from {
    width: 0;
  }

  to {
    width: 100%;
  }
}

.typing-text {
  white-space: nowrap;
  overflow: hidden;
  animation: write 3s linear infinite alternate;
}
</style>
