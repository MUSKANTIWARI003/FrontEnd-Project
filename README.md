# FrontEnd-Project
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>YouTube Clone</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />
  <style>
    body {
      background-color: #121212;
      color: white;
    }

    .navbar {
      background-color: #212121;
      padding: 10px 20px;
    }

    .search-bar {
      position: relative;
      flex-grow: 1;
    }

    .search-icon-image {
      position: absolute;
      top: -45px;
      left: 0;
    }

    .search-icon-image img {
      height: 35px;
    }

    .icon-box {
      width: 40px;
      height: 40px;
      background: #333;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 8px;
    }

    .btn-red {
      background-color: red;
      border: none;
      color: white;
    }

    .btn-dark {
      background-color: black;
      border: none;
      color: white;
    }

    input.form-control {
      background-color: #333;
      border: none;
      color: white;
    }
  </style>
</head>
<body>

<!-- Navbar -->
<nav class="navbar navbar-expand-lg">
  <div class="container-fluid d-flex align-items-center">
      <!-- Top-left Image -->
      <div class="search-icon-image me-2">
        <img src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\logo.png" alt="Logo" />
      </div>
      </div>
    </div>
  </div>
</nav>
  <style>
    :root {
      --text-color: #fff;
      --sidebar-bg: linear-gradient(to bottom, #0f2027, #203a43, #2c5364);
      --button-gradient: linear-gradient(to right, #ff416c, #ff4b2b);
      --button-gradient-alt: linear-gradient(to right, #232526, #414345);
      --content-bg: linear-gradient(to right, #141e30, #243b55);
    }

    body {
      background: var(--content-bg);
      color: var(--text-color);
      font-family: Arial, sans-serif;
      transition: background 0.5s, color 0.5s;
    }

    body.light-mode {
      background: #f1f1f1;
      color: #222;
    }

    .light-mode .sidebar {
      background: #fff;
      color: #222;
    }

    .light-mode .sidebar a,
    .light-mode .sidebar h4,
    .light-mode .short-card p {
      color: #222;
    }

    .sidebar {
      background: var(--sidebar-bg);
      padding: 15px;
      width: 250px;
      height: 100vh;
      position: fixed;
      top: 0;
      left: 0;
      overflow-y: auto;
      transition: transform 0.3s ease;
    }

    .sidebar.hidden {
      transform: translateX(-100%);
    }

    .sidebar a {
      color: var(--text-color);
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 10px 0;
      text-decoration: none;
    }

    .sidebar a:hover {
      background-color: rgba(255, 255, 255, 0.1);
      border-radius: 8px;
      padding: 5px;
    }

    .content {
      margin-left: 270px;
      padding: 20px;
    }

    .video-card,
    .short-card {
      border-radius: 10px;
      background-color: #1e1e2f;
      padding: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
    }

    .light-mode .video-card,
    .light-mode .short-card {
      background-color: #fff;
      color: #000;
    }

    .navbar {
      background: var(--sidebar-bg);
      border-bottom: 1px solid #444;
    }

    .search-bar {
      max-width: 600px;
      margin: 0 auto;
    }

    .btn {
      border: none;
      color: white;
    }

    .btn-red {
      background: var(--button-gradient);
    }

    .btn-dark {
      background: var(--button-gradient-alt);
    }

    .btn-warning {
      background: linear-gradient(to right, #f7971e, #ffd200);
      color: white;
    }

    .btn-success {
      background: linear-gradient(to right, #56ab2f, #a8e063);
    }

    .btn-screenshot {
      background: linear-gradient(to right, #396afc, #2948ff);
    }

    .shorts-section {
      display: flex;
      overflow-x: auto;
      gap: 15px;
      padding: 10px 0;
    }

    .short-card img {
      height: 150px;
      object-fit: cover;
      border-radius: 10px;
    }

    .short-card p {
      font-weight: bold;
      color: white;
    }

    .modal-content {
      background: var(--content-bg);
      color: white;
    }

    .light-mode .modal-content {
      background: white;
      color: black;
    }

    @media (max-width: 768px) {
      .sidebar {
        transform: translateX(-100%);
        position: fixed;
        z-index: 1000;
      }

      .sidebar.show {
        transform: translateX(0);
      }

      .content {
        margin-left: 0;
      }

      .navbar .search-bar {
        flex-direction: column;
        gap: 5px;
        width: 100%;
      }

      .navbar .btn {
        margin-top: 5px;
      }
    }
  </style>
</head>

<body>
    
  <nav class="navbar navbar-dark px-3 d-flex justify-content-between flex-wrap">
    <div class="d-flex align-items-center">
      <button class="btn btn-dark me-2" onclick="toggleSidebar()">
        <i class="fas fa-bars"></i>
      </button>
      <a class="navbar-brand" href="#">
        <img src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\logo.png" height="30" />
        <span class="ms-2 fw-bold fs-5">YouTube</span>
      </a>
    </div>
    <div class="search-bar d-flex flex-grow-1">
      <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" />
      <button class="btn btn-red"><i class="fas fa-search"></i></button>
      <button class="btn btn-dark ms-2" onclick="startVoiceSearch()"><i class="fas fa-microphone"></i></button>
    </div>
    <div class="mt-2 mt-md-0">
      <button class="btn btn-success me-2" data-bs-toggle="modal" data-bs-target="#loginModal">Login</button>
      <button class="btn btn-warning" onclick="toggleTheme()">🌙/🌞</button>
    </div>
  </nav>

  <div class="sidebar" id="sidebar">
    <div class="mt-2 mt-md-0 d-flex align-items-center gap-2">
      <img src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\logo.png" height="30" alt="YouTube Logo" /> <b>You Tube</b>
    </div>
    
    <h4>Menu</h4>
    <a href="#"><i class="fas fa-home"></i> Home</a>
    <a href="#"><i class="fas fa-film"></i> Shorts</a>
    <a href="#"><i class="fas fa-play-circle"></i> Subscriptions</a>
    <hr style="border-color: #999;">
    <a href="#"><i class="fas fa-clock"></i> History</a>
    <a href="#"><i class="fas fa-list"></i> Playlists</a>
    <a href="#"><i class="fas fa-clock"></i> Watch later</a>
    <a href="#"><i class="fas fa-thumbs-up"></i> Liked videos</a>
    <hr style="border-color: #999;">
    <h5>Explore</h5>
    <a href="#"><i class="fas fa-fire"></i> Trending</a>
    <a href="#"><i class="fas fa-shopping-bag"></i> Shopping</a>
    <a href="#"><i class="fas fa-music"></i> Music</a>
    <a href="#"><i class="fas fa-film"></i> Movies</a>
    <a href="#"><i class="fas fa-broadcast-tower"></i> Live</a>
    <a href="#"><i class="fas fa-gamepad"></i> Gaming</a>
    <a href="#"><i class="fas fa-newspaper"></i> News</a>
  </div>

  <div class="content" id="content">
    <h2>Featured Video</h2>
    <div class="video-card">
      <video id="video" controls poster="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\pro4.png">
        <source src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\videos\jaat-anthem.mp4" type="video/mp4" />
      </video>
      <audio id="audio" controls class="w-100 mt-2">
        <source src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\audio\Jaat Anthem - D Naveen (pagalall.com) (1).mp3" type="audio/mpeg" />
      </audio>
      <h5 class="mt-3">Jaat Anthem - D Naveen</h5>
      <p>12k views • 2 weeks ago</p>

      <div class="d-flex flex-wrap gap-2 mt-2">
        <button class="btn btn-success" id="playBtn"><i class="fas fa-play"></i> Play</button>
        <select id="speedControl" class="form-select w-auto mt-2">
          <option value="0.5">0.5x</option>
          <option value="1" selected>1x (Normal)</option>
          <option value="1.5">1.5x</option>
          <option value="2">2x</option>
        </select>
        <button class="btn btn-red" id="likeBtn"><i class="fas fa-thumbs-up"></i> Like <span id="likeCount">0</span></button>
        <button class="btn btn-dark" id="commentToggle"><i class="fas fa-comment"></i> Comment</button>
        <a class="btn btn-warning" download href="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\videos\jaat-anthem.mp4"><i class="fas fa-download"></i> Download</a>
        <button class="btn btn-screenshot" onclick="takeScreenshot()"><i class="fas fa-camera"></i> Screenshot</button>
      </div>

      <div id="commentSection" class="mt-3" style="display: none;">
        <input type="text" class="form-control mb-2" id="commentInput" placeholder="Write a comment..." />
        <button class="btn btn-primary mb-2" id="postComment">Post</button>
        <div id="commentList"></div>
      </div>
    </div>

<h3 class="mt-4">Shorts</h3>
<!-- New shorts section (your added code) -->
<div class="shorts-section flex-wrap d-flex justify-content-start">
  <div class="short-card text-center">
    <a href="https://youtube.com/shorts/5GlgIRLQ96g?si=XunWfUoLPDZ4Bpdc" target="_blank">
      <img src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\pro1.png" class="img-fluid" alt="New Short 1" />
    </a>
    <p class="mt-2">Birds Chirping Sound</p>
  </div>
  <div class="short-card text-center">
    <a href="https://youtube.com/shorts/W4EJNRlXivA?si=W_4Q_f7vxyeoeExf" target="_blank">
      <img src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\pro2.png" class="img-fluid" alt="New Short 2" />
    </a>
    <p class="mt-2">Tmkoc episode short video</p>
  </div>
  <div class="short-card text-center">
    <a href="https://youtube.com/shorts/8xkEICotpOM?si=uRC7pnSkgKLG3zmJ" target="_blank">
      <img src="C:\Users\muska\OneDrive\Desktop\FET PROJECT\assets\images\pro3.png" class="img-fluid" alt="New Short 3" />
    </a>
    <p class="mt-2">Guide for YouTube video</p>
  </div>
</div>

  <!-- Login Modal -->
  <div class="modal fade" id="loginModal" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
      <div class="modal-content p-3">
        <div class="modal-header">
          <h5 class="modal-title">Login</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
        </div>
        <div class="modal-body">
          <input type="text" class="form-control mb-2" placeholder="Username" />
          <input type="password" class="form-control mb-2" placeholder="Password" />
          <button class="btn btn-success w-100">Login</button>
        </div>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>
  <script>
    function startVoiceSearch() {
      if ('webkitSpeechRecognition' in window) {
        const recognition = new webkitSpeechRecognition();
        recognition.lang = 'en-US';
        recognition.start();
        recognition.onresult = function (event) {
          document.querySelector('.search-bar input').value = event.results[0][0].transcript;
        };
      } else {
        alert('Voice recognition not supported in this browser.');
      }
    }

    function toggleSidebar() {
      document.getElementById('sidebar').classList.toggle('show');
    }

    function toggleTheme() {
      document.body.classList.toggle('light-mode');
    }

    const playBtn = document.getElementById('playBtn');
    const video = document.getElementById('video');
    const audio = document.getElementById('audio');
    let isPlaying = false;

    playBtn.addEventListener('click', () => {
      if (!isPlaying) {
        video.play();
        audio.play();
        playBtn.innerHTML = '<i class="fas fa-pause"></i> Pause';
      } else {
        video.pause();
        audio.pause();
        playBtn.innerHTML = '<i class="fas fa-play"></i> Play';
      }
      isPlaying = !isPlaying;
    });

    document.getElementById('speedControl').addEventListener('change', function () {
      video.playbackRate = parseFloat(this.value);
    });

    const likeBtn = document.getElementById('likeBtn');
    const likeCount = document.getElementById('likeCount');
    let liked = JSON.parse(localStorage.getItem('liked')) || false;
    let count = parseInt(localStorage.getItem('likeCount')) || 0;
    likeCount.innerText = count;

    likeBtn.addEventListener('click', () => {
      liked = !liked;
      count = liked ? count + 1 : count - 1;
      likeCount.innerText = count;
      localStorage.setItem('likeCount', count);
      localStorage.setItem('liked', JSON.stringify(liked));
    });

    const commentToggle = document.getElementById('commentToggle');
    const commentSection = document.getElementById('commentSection');
    const commentInput = document.getElementById('commentInput');
    const postComment = document.getElementById('postComment');
    const commentList = document.getElementById('commentList');

    commentToggle.addEventListener('click', () => {
      commentSection.style.display = commentSection.style.display === 'none' ? 'block' : 'none';
    });

    postComment.addEventListener('click', () => {
      const text = commentInput.value.trim();
      if (text) {
        const div = document.createElement('div');
        div.className = 'comment-item';
        div.innerHTML = `<span>${text}</span> <button class="btn btn-sm btn-danger">Delete</button>`;
        div.querySelector('button').onclick = () => div.remove();
        commentList.appendChild(div);
        commentInput.value = '';
      }
    });

    function takeScreenshot() {
      html2canvas(document.querySelector('.video-card')).then(canvas => {
        let link = document.createElement('a');
        link.download = 'screenshot.png';
        link.href = canvas.toDataURL();
        link.click();
      });
    }
  </script>

</body>
</html>
