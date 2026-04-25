---
layout: single
author_profile: true
---

<style>
  /* เอฟเฟกต์ไฟ RGB วิ่งรอบกรอบ */
  .robot-frame {
    border: 4px solid;
    border-image: linear-gradient(90deg, #ff0000, #00ff00, #0000ff, #ff00ff, #ff0000) 1;
    animation: rgb-glow 3s linear infinite;
    padding: 20px;
    background: rgba(0, 0, 0, 0.8);
    border-radius: 10px;
  }

  @keyframes rgb-glow {
    0% { filter: hue-rotate(0deg); box-shadow: 0 0 15px #ff0000; }
    100% { filter: hue-rotate(360deg); box-shadow: 0 0 15px #ff0000; }
  }

  .glitch-text {
    color: #00ff00;
    text-shadow: 2px 2px #ff00ff;
    font-family: 'Courier New', Courier, monospace;
    font-weight: bold;
  }
</style>

<div class="robot-frame">
  <h2 class="glitch-text"> > INITIALIZING AI_PROTOCOL...</h2>
  
  ### 🦾 CURRENT MISSION:
  - **Core:** Machine Learning & Metaheuristics (VNS, PSO, GA)
  - **Hardware:** ESP32 / ESP8266 Prototyping
  - **Status:** Exploring Large Language Models (LLMs)
  
  ---
  
  ### ⚡ SYSTEM STATS (RGB MODE)
  ![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Wichanard&show_icons=true&theme=tokyonight&bg_color=00000000&title_color=00ff00&text_color=ffffff)
</div>
