<script>
    let technologies = [
      { title: "Artificial Intelligence (AI) in Daily Life", image: "ai.jpg", citation: "https://unsplash.com/photos/white-and-black-typewriter-with-white-printer-paper-tGBXiHcPKrM", description: "AI is transforming industries with applications in automation, healthcare, and personalized services. From virtual assistants like Siri and Alexa to advanced machine learning algorithms in healthcare, AI is reshaping how we interact with technology." },
      { title: "Quantum Computing Breakthroughs", image: "quantum.jpg", citation: "https://unsplash.com/photos/a-cube-shaped-building-on-a-rock-e_xLO2vmiQI", description: "Quantum computers leverage quantum mechanics to solve problems previously thought impossible. Companies like Google and IBM are leading the charge in developing quantum processors capable of revolutionizing cryptography, material science, and AI." },
      { title: "5G Connectivity Expansion", image: "5g.jpg", citation: "https://unsplash.com/photos/black-samsung-android-smartphone-displaying-icons-BI5JpNK5sE0", description: "5G technology is enabling ultra-fast internet speeds, lower latency, and improved connectivity. It is paving the way for smart cities, autonomous vehicles, and enhanced remote working experiences." },
      { title: "Augmented & Virtual Reality", image: "arvr.jpg", citation: "https://unsplash.com/photos/blue-and-black-digital-device-npTT9rD8wd4", description: "AR and VR technologies are changing how we experience entertainment, education, and even remote work. With applications in gaming, training simulations, and virtual tourism, these immersive technologies are bridging the gap between reality and the digital world." },
      { title: "Blockchain & Cryptography Innovations", image: "blockchain.jpg", citation: "https://unsplash.com/photos/blue-and-red-line-illustration-vBCVcWUyvyM", description: "Blockchain technology is revolutionizing security, transparency, and financial transactions. Beyond cryptocurrencies, blockchain is being used for secure voting systems, supply chain management, and decentralized applications (dApps)." },
      { title: "Biotechnology & Gene Editing", image: "biotech.jpg", citation: "https://unsplash.com/photos/woman-holding-test-tubes-GcrSgHDrniY", description: "Gene-editing tools like CRISPR are advancing medicine by allowing precise modifications in DNA. This technology has the potential to eliminate genetic disorders, create disease-resistant crops, and revolutionize personalized medicine." },
      { title: "Internet of Things (IoT) Evolution", image: "iot.jpg", citation: "https://unsplash.com/photos/close-up-photography-of-mining-rig-h3vT1Kp0FxA", description: "IoT devices connect and automate our world, from smart homes to industrial automation. The technology is optimizing energy use, improving healthcare monitoring, and enhancing security through interconnected devices." },
      { title: "Space Technology & Exploration", image: "space.jpg", citation: "https://unsplash.com/photos/twom-white-flying-rockets-during-daytime-MEW1f-yu2KI", description: "Private and government-led space missions are expanding our reach beyond Earth. From reusable rockets by SpaceX to NASA's Artemis program, advancements in space technology are making deep-space exploration a reality." },
      { title: "Robotics & Automation", image: "robotics.jpg", citation: "https://unsplash.com/photos/black-and-white-industrial-machine-dRMQiAubdws", description: "Robots powered by AI are enhancing productivity in manufacturing, healthcare, and logistics. From robotic-assisted surgeries to warehouse automation, these innovations are increasing efficiency and reducing human labor in high-risk environments." },
      { title: "Renewable Energy Innovations", image: "energy.jpg", citation: "https://unsplash.com/photos/white-and-blue-solar-panels-hxUcl0nUsIY", description: "Solar, wind, and battery storage technologies are driving sustainable energy solutions. Breakthroughs in energy storage and efficiency are helping transition the world toward a cleaner and more resilient power grid." }
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
      height: 800px;
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
      font-size: 36px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 800px;
      scroll-snap-align: start;
    }
    .parallax {
      position: relative;
      width: 100%;
      height: 800px;
      background-size: cover;
      background-position: center;
      background-attachment: fixed;
    }
    .content {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
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
        <p class="citation">Source: {tech.citation}</p>
      </div>
    </div>
  {/each}
  