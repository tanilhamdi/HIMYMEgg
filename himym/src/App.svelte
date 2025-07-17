<script lang="ts">
  import rawText from "./himym.txt?raw";
  import _ from "lodash";
  const episodes = rawText.split("\n");

  let randNum = _.random(0, 208);

  function opentheEp() {
    const ep = episodes[randNum];
    if (randNum == 208) {
      return randNum;
    } else {
      window.location.href = ep;
    }
  }
</script>

{#if randNum == 208}
  <img
    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR7Aw290-nMttq5Z9DghMKc70OCMCv1l4q6Vg&s
"
    alt=""
  />
  <br />
  <h1>Yarrami YEEE</h1>
{:else}{/if}
<div id="button-container">
  <div id="texts">You're a Loser</div>
  <button id="porn" on:click={opentheEp}>
    <i class="fas fa-play"></i>
    <span class="sr-only">Play Episode</span>
  </button>
</div>

<style>
  #texts {
    font-size: 3em;
    text-align: center;
    margin-bottom: 30px;
  }

  #button-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #292929;
    justify-content: center;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
  }
  /* Global styles */
  :global(body) {
    margin: 0;
    padding: 0;
    font-family: "Montserrat", Arial, sans-serif;
    background-color: #1b1b1b;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #e0e0e0;
    overflow: hidden;
  }

  /* Visually hidden text for accessibility (screen readers ONLY) */
  .sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border-width: 0;
  }

  /* Button specific styles */
  #porn {
    background-color: #ffa31a; /* Your primary orange */
    color: #1b1b1b; /* Dark icon color on orange for good contrast */
    border: none;
    outline: none;
    cursor: pointer;
    /* --- KEY CHANGES FOR ICON BUTTON --- */
    width: 200px; /* Make it a square for a circular icon button */
    height: 80px; /* Make it a square for a circular icon button */
    font-size: 2.5em; /* This controls the icon's size (make the icon larger) */
    display: flex; /* Use flexbox to center the icon */
    justify-content: center;
    align-items: center;
    /* --- END KEY CHANGES --- */

    transition:
      background-color 0.3s ease,
      transform 0.3s ease,
      box-shadow 0.3s ease; /* Smoother transitions for all properties */
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3); /* Subtle initial shadow for depth */
  }

  #porn:hover {
    background-color: #ff9900; /* Slightly darker orange on hover */
    transform: scale(1.05); /* Slightly enlarge the button */
    /* --- THE GLOW EFFECT --- */
  }

  #porn:active {
    transform: scale(0.98); /* "Press down" effect */
    background-color: #e68a00; /* Even darker orange when pressed */
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2); /* Smaller shadow when pressed */
  }

  /* Optional: Add a subtle overlay or background pattern */
  :global(body)::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: radial-gradient(
      circle at center,
      rgba(255, 163, 26, 0.05) 0%,
      rgba(27, 27, 27, 0.9) 70%
    );
    z-index: -1;
    opacity: 0.7;
  }

  /* Basic responsiveness for very small screens */
  @media (max-width: 400px) {
    #porn {
      width: 70px; /* Adjust button size for small screens */
      height: 70px;
      font-size: 2em; /* Adjust icon size for small screens */
    }
  }
</style>
