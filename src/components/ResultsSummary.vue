<script setup></script>

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
          <div class="detail detail-reaction">
            <p class="detail-caption detail-reaction-cap">Reaction</p>
            <p class="detail-score"><strong>80</strong> /100</p>
          </div>
          <div class="detail detail-memory">
            <p class="detail-caption detail-memory-cap">Memory</p>
            <p class="detail-score"><strong>92</strong> /100</p>
          </div>
          <div class="detail detail-verbal">
            <p class="detail-caption detail-verbal-cap">Verbal</p>
            <p class="detail-score"><strong>61</strong> /100</p>
          </div>
          <div class="detail detail-visual">
            <p class="detail-caption detail-visual-cap">Visual</p>
            <p class="detail-score"><strong>72</strong> /100</p>
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
  background: linear-gradient(hsl(252, 100%, 67%), hsl(241, 81%, 54%));
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
  background: linear-gradient(hsla(256, 72%, 46%, 1), hsla(241, 72%, 46%, 0));
}

.result-score {
  font-size: 3.5rem;
  font-weight: 800;
}

.result-lead {
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

.detail-caption {
  font-weight: 700;
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

.detail-caption::before {
  margin-right: 0.5rem;
  position: relative;
  top: 5px;
}

.detail-reaction-cap::before {
  content: url("../assets/icon-reaction.svg");
}
.detail-memory-cap::before {
  content: url("../assets/icon-memory.svg");
}
.detail-verbal-cap::before {
  content: url("../assets/icon-verbal.svg");
}
.detail-visual-cap::before {
  content: url("../assets/icon-visual.svg");
}

strong {
  font-weight: 800;
}

.btn-continue {
  text-align: center;
  background-color: var(--dark-gray-blue);
  color: var(--white);
  padding: 1rem;
  border-radius: 15em;
}

.btn-continue:hover {
  background-color: var(--cobalt-blue);
  cursor: pointer;
}

@media (width>=1024px) {
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
    max-width: 340px;
    height: auto;
    padding: 2.25rem;
  }

  .result-container {
    border-radius: 3rem;
  }

  .result-score {
    font-size: 4rem;
  }

  .result {
    height: 490px;
  }

  .result-circle {
    width: 12rem;
    height: 12rem;
    line-height: 3.5rem;
  }
}
</style>
