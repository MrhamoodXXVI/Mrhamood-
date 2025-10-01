# Mrhamood-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My Futuristic Portfolio</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Poppins:wght@300;500;700&display=swap');

    * {margin: 0; padding: 0; box-sizing: border-box;}

    body {
      font-family: 'Poppins', sans-serif;
      background: #0a0a0a;
      color: #fff;
      line-height: 1.6;
      overflow-x: hidden;
      position: relative;
    }

    header {
      display: flex; justify-content: space-between; align-items: center;
      padding: 20px 50px; background: rgba(10,10,10,0.9);
      position: fixed; top: 0; width: 100%; z-index: 1000;
      border-bottom: 1px solid rgba(255,123,0,0.2);
      box-shadow: 0 0 15px rgba(255,123,0,0.2);
    }

    header .logo {
      font-family: 'Orbitron', sans-serif; font-size: 1.5rem;
      color: #ff7b00; text-transform: uppercase; font-weight: 700; letter-spacing: 2px;
    }

    header nav a {
      margin: 0 15px; text-decoration: none; color: #fff; transition: 0.3s; font-weight: 500;
    }
    header nav a:hover {color: #ff7b00;}

    section {
      padding: 100px 50px; min-height: 100vh;
      display: flex; justify-content: center; align-items: center;
      flex-direction: column; position: relative; z-index: 1;
    }

    /* Hero Section */
    #home {flex-direction: row; justify-content: space-between; align-items: center; gap: 40px;}

    .intro {flex: 1; max-width: 600px;}
    .intro h1 {font-size: 2.5rem; margin-bottom: 20px; font-family: 'Orbitron', sans-serif;}
    .intro h1 span {color: #ff7b00; text-shadow: 0 0 10px rgba(255,123,0,0.8);}
    .intro p {margin-bottom: 30px; color: #ddd;}

    .btn {
      padding: 12px 25px;
      background: linear-gradient(135deg, #ff7b00, #ffb84d);
      border: none; border-radius: 30px; color: #000; font-weight: bold;
      cursor: pointer; transition: 0.3s;
      box-shadow: 0 0 20px rgba(255,123,0,0.6);
    }
    .btn:hover {box-shadow: 0 0 30px rgba(255,123,0,0.9);}

    .avatar {flex: 1; display: flex; justify-content: center;}
    .avatar img {
      width: 280px; height: 280px; border-radius: 50%; object-fit: cover;
      border: 6px solid rgba(255,123,0,0.8);
      box-shadow: 0 0 40px rgba(255,123,0,0.8);
    }

    /* Section Titles */
    h2 {
      font-size: 2rem; margin-bottom: 30px;
      font-family: 'Orbitron', sans-serif; color: #ff7b00;
      text-transform: uppercase; letter-spacing: 2px;
    }

    .card {
      background: rgba(255,255,255,0.03);
      border: 1px solid rgba(255,123,0,0.2);
      padding: 20px; border-radius: 15px;
      box-shadow: 0 0 20px rgba(255,123,0,0.1);
      margin: 15px; transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {transform: translateY(-8px); box-shadow: 0 0 30px rgba(255,123,0,0.4);}

    /* Projects grid */
    .projects {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px; width: 100%; max-width: 1000px;
    }

    /* Contact */
    .contact-info {text-align: center; font-size: 1.1rem; color: #ddd;}

    /* Footer */
    footer {
      background: rgba(10,10,10,0.95); padding: 20px 50px; text-align: center;
      border-top: 1px solid rgba(255,123,0,0.2); box-shadow: 0 -5px 15px rgba(255,123,0,0.2);
    }
    footer p {margin: 8px 0;}
    footer a {color: #ff7b00; text-decoration: none; transition: 0.3s;}
    footer a:hover {color: #ffb84d;}

    /* Floating random tech elements */
    .floating-icon {
      position: absolute;
      color: rgba(255,255,255,0.5);
      z-index: 0; pointer-events: none;
      animation: float 12s ease-in-out infinite, rotate 20s linear infinite;
    }

    /* variasi posisi + ukuran */
    .icon1 { top: 10%; left: 8%; font-size: 2.2rem; animation-delay: 0s; }
    .icon2 { top: 35%; right: 15%; font-size: 3.5rem; animation-delay: 2s; }
    .icon3 { bottom: 20%; left: 12%; font-size: 2.8rem; animation-delay: 4s; }
    .icon4 { bottom: 15%; right: 25%; font-size: 4rem; animation-delay: 6s; }
    .icon5 { top: 50%; left: 45%; font-size: 2.5rem; animation-delay: 3s; }
    .icon6 { bottom: 40%; right: 10%; font-size: 3.2rem; animation-delay: 1s; }
    .icon7 { top: 20%; right: 40%; font-size: 2rem; animation-delay: 5s; }
    .icon8 { bottom: 30%; left: 35%; font-size: 3rem; animation-delay: 7s; }
    .icon9 { top: 65%; right: 20%; font-size: 2.7rem; animation-delay: 8s; }
    .icon10 { bottom: 10%; left: 55%; font-size: 3.8rem; animation-delay: 9s; }

    @keyframes float {
      0%,100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }
    @keyframes rotate {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">MyPortofolio</div>
    <nav>
      
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
                      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Floating Background Icons (lebih banyak + variasi ukuran + rotasi) -->
  <div class="floating-icon icon1">🏐</div>
  <div class="floating-icon icon2">&lt;/&gt;</div>
  <div class="floating-icon icon3">⛓️</div>
  <div class="floating-icon icon4">📶</div>
  <div class="floating-icon icon5">🏐</div>
  <div class="floating-icon icon6">&lt;/&gt;</div>
  <div class="floating-icon icon7">⛓️</div>
  <div class="floating-icon icon8">📶</div>
  <div class="floating-icon icon9">🏐</div>
  <div class="floating-icon icon10">&lt;/&gt;</div>
  <div class="floating-icon icon11">&lt;/&gt;</div>

  <!-- Home -->
  <section id="home">
    <div class="intro">
      <h1>Hello, I'm <span>Muhammad Ilham Khairullah</span></h1>
      <p>Saya baru mulai belajar coding. Ini adalah portofolio pertama saya dengan tema futuristik. 
      Yuk lihat lebih lanjut!</p>
      <button class="btn">More About Me</button>
    </div>
    <div class="avatar">
      <img src="https://files.catbox.moe/twlbgz.jpg" alt="My Avatar">
    </div>
  </section>

  <!-- About -->
  <section id="about">
    <h2>About Me</h2>
    <div class="card">
      <p>Saat ini saya sedang belajar tentang dasar dasar pemograman. Saya senang memecahkan masalah dan saat ini saya berfokus mempelajari dasar HTML, CSS, dan JavaScript, selain belajar coding saya juga hobi olahraga voli yang melatih kerja sama tim.
      </p>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="projects">
      <div class="card">📄 Landing page HTML</div>
      <div class="card">🎨 Styling dengan CSS</div>
      <div class="card">⚜️ JavaScript dasar</div>
      <div class="card">🚀 Coming Soon....</div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact</h2>
    <div class="contact-info">
      <p>Jangan ragu untuk menghubungi saya melalui media sosial atau email di bawah ini.</p>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>Email: <a href="mailto:youremail@example.com">soloznpc@gmail.com</a></p>
    <p><a href="https://www.instagram.com/mrhammood?igsh=NDhtd3hrcHEzMmR2">Instagram</a></p>
  </footer>
</body>
</html>        
