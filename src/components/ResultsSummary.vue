<script setup>
import resultData from "../assets/data.json";
</script>

<template>
  <div class="main-container">
    <div class="result-container">
      <div class="container-inner result">
        <h1 class="result-title">Your Result</h1>
        <div class="result-circle">
          <p class="result-score">76</p>
          <p class="result-lead">of 100</p>
        </div>
        <div class="result-score-msg">
          <p class="result-msg-title">Great</p>
          <p class="result-msg-lead">
            You scored higher than 65% of the people who have taken these tests.
          </p>
        </div>
      </div>
    </div>
    <div class="summary-container">
      <div class="container-inner summary">
        <h2 class="summary-title">Summary</h2>
        <div class="summary-details">
          <div
            v-for="{ category, score, icon } in resultData"
            :class="`detail detail-${category}`"
          >
            <div class="detail-inner">
              <img
                :src="`${icon}`"
                alt=""
                aria-hidden="true"
                width="24"
                height="24"
              />
              <p :class="`detail-category detail-${category}-cap`">
                {{ category }}
              </p>
            </div>
            <p class="detail-score">
              <strong>{{ score }}</strong> /100
            </p>
          </div>
        </div>
        <a class="btn-continue" href="#">Continue</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
a {
  all: unset;
}

.main-container {
  display: grid;
}

.result-container {
  background: linear-gradient(hsl(0deg 0% 17.39%), hsl(241deg 17.15% 27.54%));
  color: var(--white);
  text-align: center;
  border-radius: 0 0 3rem 3rem;
}

.container-inner {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 2rem;
}

.result-title {
  font-size: 1.15rem;
  color: var(--light-lavender);
}

.result-circle {
  border-radius: 50rem;
  width: 9rem;
  height: 9rem;
  margin: 1.5rem auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(hsl(254deg 8.66% 30.55%), hsl(0deg 0% 100% / 0%));
  font-size: 1rem;
  color: var(--light-lavender);
}

.result-msg-title {
  font-size: 1.5rem;
  font-weight: 700;
}

.result-msg-lead {
  font-size: 1rem;
  color: var(--light-lavender);
}

.summary-title {
  font-size: 1.15rem;
  color: var(--dark-gray-blue);
}

.summary-details {
  padding: 2rem 0;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  font-size: 1rem;
}

.detail {
  padding: 1rem;
  display: flex;
  justify-content: space-between;
  border-radius: 0.8rem;
  color: var(--dark-gray-blue);
}

.detail-category {
  text-transform: capitalize;
  font-weight: 700;
}

.detail-inner {
  display: flex;
  flex-direction: row;
  gap: 1rem;
}

.detail-reaction {
  background-color: hsla(0, 100%, 67%, 0.1);
}
.detail-memory {
  background-color: hsla(39, 100%, 56%, 0.1);
}
.detail-verbal {
  background-color: hsla(166, 100%, 37%, 0.1);
}
.detail-visual {
  background-color: hsla(234, 85%, 45%, 0.1);
}

.detail-reaction-cap {
  color: var(--light-red);
}
.detail-memory-cap {
  color: var(--orangey-yellow);
}
.detail-verbal-cap {
  color: var(--green-teal);
}
.detail-visual-cap {
  color: var(--cobalt-blue);
}

strong {
  font-weight: 800;
}

.btn-continue {
  text-align: center;
  background-color: var(--dark-gray-blue);
  color: var(--white);
  padding: 0.85rem;
  border-radius: 15em;
}

.btn-continue:hover {
  opacity: 0.8;
  cursor: pointer;
  transition: all 0.5s ease;
}

@media (width>=768px) {
  main {
    min-height: 100vh;
    place-content: center;
  }

  .main-container {
    grid-template-columns: 1fr 1fr;
    box-shadow: 10px 10px 19px 0px rgba(0, 0, 0, 0.26);
    border-radius: 3rem;
  }

  .container-inner {
    max-width: 23.0781rem;
    height: 32rem;
    padding: 2.85rem;
    justify-content: space-between;
  }

  .result-container {
    border-radius: 3rem;
  }

  .result-title {
    font-size: 1.5rem;
  }

  .result-msg-title {
    font-size: 2rem;
  }

  .result-msg-lead {
    font-size: 1.15rem;
    margin: 0.3rem;
  }

  .result-score {
    font-size: 4rem;
    font-weight: 800;
  }

  .result {
    height: 32rem;
  }

  .result-circle {
    width: 12rem;
    height: 12rem;
    line-height: 3.5rem;
  }

  .summary-details {
    padding: 1rem 0;
  }

  .summary-title {
    font-size: 1.5rem;
  }

  .detail-category {
    font-size: 1.1rem;
  }

  .detail {
    padding: 0.9rem;
  }
}
</style>
