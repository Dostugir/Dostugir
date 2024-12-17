<div style="position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1; overflow: hidden;">
  <img src="https://i.gifer.com/5ARz.gif" style="width: 100%; height: 100%; object-fit: cover; filter: brightness(0.4);" alt="Skyfall background">
</div>

<!-- Add Pikachu cursor follower -->
<div id="pikachu" style="position: fixed; z-index: 1000; pointer-events: none; transform: translate(-50%, -50%);">
  <img src="https://i.gifer.com/2GU.gif" width="100" height="100" alt="Pikachu">
</div>

<script>
  document.addEventListener('mousemove', (e) => {
    const pikachu = document.getElementById('pikachu');
    const x = e.clientX;
    const y = e.clientY;
    
    // Add smooth animation
    pikachu.style.transition = 'transform 0.3s ease-out';
    pikachu.style.left = x + 'px';
    pikachu.style.top = y + 'px';
  });
</script>

<div align="center">
  <h1>👋 Welcome to my GitHub Profile!</h1>
  <h2>Abdullah Aziz Dostugir</h2>
  
  <img src="https://i.gifer.com/3OdB.gif" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></img>

  <p>
    <a href="https://github.com/Dostugir"><img src="https://img.shields.io/github/followers/yourusername?label=Follow&style=social" alt="GitHub followers"></a>
    <a href="https://www.linkedin.com/in/abdullah-aziz-dostugir-a46b8a256/"><img src="https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="LinkedIn"></a>
  </p>
</div>

<!-- Simple Snake Game -->
<div style="text-align: center; margin: 20px 0;">
  <canvas id="snakeGame" width="400" height="400" style="border:1px solid #000; background: #f0f0f0;"></canvas>
  <p>Use arrow keys to play Snake! 🐍</p>
</div>

<script>
  const canvas = document.getElementById('snakeGame');
  const ctx = canvas.getContext('2d');
  
  let snake = [{x: 200, y: 200}];
  let food = {x: 300, y: 300};
  let dx = 10;
  let dy = 0;
  let score = 0;
  
  document.addEventListener('keydown', (e) => {
    if (e.key === 'ArrowUp' && dy === 0) { dx = 0; dy = -10; }
    if (e.key === 'ArrowDown' && dy === 0) { dx = 0; dy = 10; }
    if (e.key === 'ArrowLeft' && dx === 0) { dx = -10; dy = 0; }
    if (e.key === 'ArrowRight' && dx === 0) { dx = 10; dy = 0; }
  });
  
  function gameLoop() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    
    // Move snake
    const head = {x: snake[0].x + dx, y: snake[0].y + dy};
    snake.unshift(head);
    
    // Check for food collision
    if (head.x === food.x && head.y === food.y) {
      food.x = Math.floor(Math.random() * 40) * 10;
      food.y = Math.floor(Math.random() * 40) * 10;
      score += 10;
    } else {
      snake.pop();
    }
    
    // Draw snake
    ctx.fillStyle = 'green';
    snake.forEach(segment => {
      ctx.fillRect(segment.x, segment.y, 10, 10);
    });
    
    // Draw food
    ctx.fillStyle = 'red';
    ctx.fillRect(food.x, food.y, 10, 10);
    
    // Draw score
    ctx.fillStyle = 'black';
    ctx.font = '20px Arial';
    ctx.fillText(`Score: ${score}`, 10, 30);
    
    // Game over conditions
    if (head.x < 0 || head.x >= canvas.width || head.y < 0 || head.y >= canvas.height) {
      alert(`Game Over! Score: ${score}`);
      snake = [{x: 200, y: 200}];
      dx = 10;
      dy = 0;
      score = 0;
    }
    
    setTimeout(gameLoop, 100);
  }
  
  gameLoop();
</script>

## 🚀 About Me
I'm a passionate software developer specializing in:
- 💻 AI Development
- 🔧 Complex Problem Solving
- 🌟 Intelligent Systems Design

With expertise in C/C++, Python, and a strong foundation in AI/ML technologies, I focus on creating innovative solutions that push technological boundaries.

## 💻 Technical Stack

<table>
  <tr>
    <td><b>Programming Languages</b></td>
    <td>
      • C/C++ <br>
      • Python <br>
      • [Add other languages]
    </td>
  </tr>
  <tr>
    <td><b>AI & ML Expertise</b></td>
    <td>
      • Deep Learning & Neural Networks<br>
      • Computer Vision<br>
      • Natural Language Processing<br>
      • TensorFlow/PyTorch
    </td>
  </tr>
  <tr>
    <td><b>Professional Skills</b></td>
    <td>
      • Team Leadership & Project Management<br>
      • Problem Solving & Critical Thinking<br>
      • Effective Communication<br>
      • Time Management & Adaptability
    </td>
  </tr>
</table>

## 📊 GitHub Analytics

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true&theme=radical" alt="GitHub Stats">
  <br><br>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yourusername&layout=compact&theme=radical" alt="Top Languages">
</div>

## 🌱 Current Focus
- 🧠 Advanced AI Architectures
- ⚛️ Quantum Computing
- 🔄 [Technology/Skill 2]

## 🏆 Achievements & Certifications
<details>
<summary>Click to expand</summary>
<br>
<!-- • [Certification 1]<br>
• [Award/Recognition]<br>
• [Open Source Contribution] -->
</details>

## 📫 Connect With Me
<p align="center">
  📧 Email: dostugir2002@gmail.com<br>
  💼 LinkedIn: <a href="[Your LinkedIn Profile]">Abdullah Aziz Dostugir</a><br>
  
</p>

<!-- <div align="center">
  <img src="https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif" width="400" height="225" frameBorder="0" class="giphy-embed" allowFullScreen></img>
</div> -->

---
⭐️ From [Abdullah Aziz Dostugir](https://github.com/Dostugir)
