<template>
  <q-page style="overflow: hidden;" class="flex flex-center content-center">
    <div v-if="countdown > 0">
      <div>
        <h3 class=" welcome">From your lover to</h3>
        <h1 class="name typing-text">Trần Thị Thảo Nguyên</h1>
        <div style="text-align: center;" class="name">{{ countdown }}</div>
      </div>
    </div>
    <div v-if="countdown == 0 && !showFire">
      <h1 class="name">Are you ready?</h1>
      <q-btn class="" flat outline style="background-color: white;" label="Yes, I am ready" @click="play"></q-btn>
    </div>
    <iframe v-show="showFire" style="width:100vw;height: 100vh;" id="preview-frame" class="preview-desktop"
      src="https://devforum.info/DEMO/phaohoa/" frameborder="0">
    </iframe>
    <q-dialog full-height full-width persistent v-model="showDialog">
      <div style="overflow: hidden;">
        <h1 class="blinking-text" style="font-weight: 700;text-align: center;color: white;">Happy birthday</h1>
        <h3 style="font-weight: 700;text-align: center;color: white;">Trần Thị Thảo Nguyên</h3>
        <marquee style="color: aliceblue;" behavior="" direction="">
          <h4 style="font-weight: 700;text-align: center;color: white;">A wish for you on your
            birthday, whatever you ask
            may you receive, whatever you seek may you find, whatever you wish may it be fulfilled on your birthday and
            always. Happy birthday!</h4>
        </marquee>
        <marquee direction="right" style="color: aliceblue;" behavior="">
          <div>
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-13.fna.fbcdn.net/v/t39.30808-6/323883622_1100014424005336_2337883768263539547_n.jpg?_nc_cat=106&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=yCrKcgrxHKwAX-9QDFM&amp;_nc_ht=scontent.fsgn5-13.fna&amp;oh=00_AfABx2RN-fcPJCmEWDeBEsgPzDRIyjd8rAJ48Qjn0qbYRA&amp;oe=64F2E789">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/305849131_1113719875909322_5872577173571885935_n.jpg?_nc_cat=107&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=WzXfufCkcvkAX8w1ztZ&amp;_nc_ht=scontent.fsgn5-10.fna&amp;oh=00_AfCfpR14OdYOCaigT6nlotS-nYy2Yky7wIwjc8bBJhU8uw&amp;oe=64F357C9">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-13.fna.fbcdn.net/v/t39.30808-6/323883622_1100014424005336_2337883768263539547_n.jpg?_nc_cat=106&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=yCrKcgrxHKwAX-9QDFM&amp;_nc_ht=scontent.fsgn5-13.fna&amp;oh=00_AfABx2RN-fcPJCmEWDeBEsgPzDRIyjd8rAJ48Qjn0qbYRA&amp;oe=64F2E789">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/305849131_1113719875909322_5872577173571885935_n.jpg?_nc_cat=107&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=WzXfufCkcvkAX8w1ztZ&amp;_nc_ht=scontent.fsgn5-10.fna&amp;oh=00_AfCfpR14OdYOCaigT6nlotS-nYy2Yky7wIwjc8bBJhU8uw&amp;oe=64F357C9">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-13.fna.fbcdn.net/v/t39.30808-6/323883622_1100014424005336_2337883768263539547_n.jpg?_nc_cat=106&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=yCrKcgrxHKwAX-9QDFM&amp;_nc_ht=scontent.fsgn5-13.fna&amp;oh=00_AfABx2RN-fcPJCmEWDeBEsgPzDRIyjd8rAJ48Qjn0qbYRA&amp;oe=64F2E789">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/305849131_1113719875909322_5872577173571885935_n.jpg?_nc_cat=107&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=WzXfufCkcvkAX8w1ztZ&amp;_nc_ht=scontent.fsgn5-10.fna&amp;oh=00_AfCfpR14OdYOCaigT6nlotS-nYy2Yky7wIwjc8bBJhU8uw&amp;oe=64F357C9">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-13.fna.fbcdn.net/v/t39.30808-6/323883622_1100014424005336_2337883768263539547_n.jpg?_nc_cat=106&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=yCrKcgrxHKwAX-9QDFM&amp;_nc_ht=scontent.fsgn5-13.fna&amp;oh=00_AfABx2RN-fcPJCmEWDeBEsgPzDRIyjd8rAJ48Qjn0qbYRA&amp;oe=64F2E789">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/305849131_1113719875909322_5872577173571885935_n.jpg?_nc_cat=107&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=WzXfufCkcvkAX8w1ztZ&amp;_nc_ht=scontent.fsgn5-10.fna&amp;oh=00_AfCfpR14OdYOCaigT6nlotS-nYy2Yky7wIwjc8bBJhU8uw&amp;oe=64F357C9">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-13.fna.fbcdn.net/v/t39.30808-6/323883622_1100014424005336_2337883768263539547_n.jpg?_nc_cat=106&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=yCrKcgrxHKwAX-9QDFM&amp;_nc_ht=scontent.fsgn5-13.fna&amp;oh=00_AfABx2RN-fcPJCmEWDeBEsgPzDRIyjd8rAJ48Qjn0qbYRA&amp;oe=64F2E789">
            <img style="width:150px;margin: 10px;" data-visualcompletion="media-vc-image" alt="Không có mô tả ảnh."
              class="x1bwycvy x193iq5w x4fas0m x19kjcj4" referrerpolicy="origin-when-cross-origin"
              src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/305849131_1113719875909322_5872577173571885935_n.jpg?_nc_cat=107&amp;ccb=1-7&amp;_nc_sid=8bfeb9&amp;_nc_ohc=WzXfufCkcvkAX8w1ztZ&amp;_nc_ht=scontent.fsgn5-10.fna&amp;oh=00_AfCfpR14OdYOCaigT6nlotS-nYy2Yky7wIwjc8bBJhU8uw&amp;oe=64F357C9">
          </div>
        </marquee>
      </div>
    </q-dialog>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      seconds: 10,
      intervalId: null,
      showDialog: false,
      showFire: false,
      redirect: true
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
    },
    play() {
      this.showFire = true
      this.showDialog = true
      new Audio("https://itov3-s3-cms-lcms.s3.amazonaws.com/uploads/question/audio/2023/8/29/638289170230271695_chucmungsinhnhat.mp3").play();
      // Đợi 30 giây
      setTimeout(function () {
        window.location.href = "https://www.facebook.com/profile.php?id=100018139598645&sk=photos";
      }, 60000);
    }
  },
  mounted() {
    this.startCountdown();
  }
};
</script>

<style>
@keyframes colorChange {
  0% {
    color: red;
  }

  25% {
    color: blue;
  }

  50% {
    color: green;
  }

  75% {
    color: yellow;
  }

  100% {
    color: red;
  }
}

.blinking-text {
  animation: colorChange 2s linear infinite;
}

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
