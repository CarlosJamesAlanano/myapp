<script>
    let technologies = [
      { title: "Artificial Intelligence (AI) in Daily Life", image: "ai.jpg", citation: "https://unsplash.com/photos/white-and-black-typewriter-with-white-printer-paper-tGBXiHcPKrM", description: "AI is transforming industries with applications in automation, healthcare, and personalized services." },
      { title: "Quantum Computing Breakthroughs", image: "quantum.jpg", citation: "https://unsplash.com/photos/a-cube-shaped-building-on-a-rock-e_xLO2vmiQI", description: "Quantum computers leverage quantum mechanics to solve problems previously thought impossible." },
      { title: "5G Connectivity Expansion", image: "5g.jpg", citation: "https://unsplash.com/photos/black-samsung-android-smartphone-displaying-icons-BI5JpNK5sE0", description: "5G technology is enabling ultra-fast internet speeds, lower latency, and improved connectivity." },
      { title: "Augmented & Virtual Reality", image: "arvr.jpg", citation: "https://unsplash.com/photos/blue-and-black-digital-device-npTT9rD8wd4", description: "AR and VR technologies are changing how we experience entertainment, education, and even remote work." },
      { title: "Blockchain & Cryptography Innovations", image: "blockchain.jpg", citation: "https://unsplash.com/photos/blue-and-red-line-illustration-vBCVcWUyvyM", description: "Blockchain technology is revolutionizing security, transparency, and financial transactions." },
      { title: "Biotechnology & Gene Editing", image: "biotech.jpg", citation: "https://unsplash.com/photos/woman-holding-test-tubes-GcrSgHDrniY", description: "Gene-editing tools like CRISPR are advancing medicine by allowing precise modifications in DNA." },
      { title: "Internet of Things (IoT) Evolution", image: "iot.jpg", citation: "https://unsplash.com/photos/close-up-photography-of-mining-rig-h3vT1Kp0FxA", description: "IoT devices connect and automate our world, from smart homes to industrial automation." },
      { title: "Space Technology & Exploration", image: "space.jpg", citation: "https://unsplash.com/photos/twom-white-flying-rockets-during-daytime-MEW1f-yu2KI", description: "Private and government-led space missions are expanding our reach beyond Earth." },
      { title: "Robotics & Automation", image: "robotics.jpg", citation: "https://unsplash.com/photos/black-and-white-industrial-machine-dRMQiAubdws", description: "Robots powered by AI are enhancing productivity in manufacturing, healthcare, and logistics." },
      { title: "Renewable Energy Innovations", image: "energy.jpg", citation: "https://unsplash.com/photos/white-and-blue-solar-panels-hxUcl0nUsIY", description: "Solar, wind, and battery storage technologies are driving sustainable energy solutions." }
    ];
  </script>
  
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: Arial, sans-serif;
      scroll-snap-type: y mandatory;
      overflow-y: scroll;
    }
  
    .section {
      height: 700px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      text-align: center;
      font-size: 28px;
      font-weight: bold;
      text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.8);
      scroll-snap-align: start;
    }
  
    .landing {
      background: black;
      color: white;
      font-size: 32px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 700px;
      padding: 20px;
      text-align: center;
    }
  
    .parallax {
      position: relative;
      width: 100%;
      height: 700px;
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
  
    .content {
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 10px;
      max-width: 80%;
    }
  
    .citation {
      font-size: 14px;
      color: lightgray;
      margin-top: 10px;
    }
  
    @media (max-width: 768px) {
      .section {
        height: 500px;
        font-size: 20px;
      }
      .landing {
        height: 500px;
        font-size: 24px;
        padding: 15px;
      }
      .parallax {
        height: 500px;
        background-attachment: scroll;
      }
      .content {
        max-width: 90%;
        padding: 15px;
      }
    }
  </style>
  
  <div class="landing section">
    <h1>Welcome to Technological Innovations</h1>
    <p>Scroll down to explore the latest advancements in technology.</p>
  </div>
  
  {#each technologies as tech}
    <div class="parallax section" style="background-image: url({tech.image})">
      <div class="content">
        <h2>{tech.title}</h2>
        <p>{tech.description}</p>
        <p class="citation">Source: <a href={tech.citation} target="_blank">{tech.citation}</a></p>
      </div>
    </div>
  {/each}
  