<!-- Dymiaz Custom README -->

<div align="center">
  <style>
    body {
      font-family: "Poppins", "Segoe UI", Arial, sans-serif;
      color: #eaeaea;
      background: #0a0a0a;
      margin: 0;
      padding: 0;
    }

    /* Header */
    .header {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
      margin: 25px auto;
      padding: 10px 20px;
    }

    .header img {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      border: 2px solid #333;
      box-shadow: 0 0 20px rgba(255, 255, 255, 0.05);
      filter: grayscale(100%);
      transition: 0.3s ease;
    }

    .header img:hover {
      filter: grayscale(0%);
      transform: scale(1.05);
    }

    .header h1 {
      font-size: 2.2rem;
      font-weight: 700;
      letter-spacing: 1px;
      color: #fff;
      margin: 0;
      text-shadow: 0 0 8px rgba(255, 50, 50, 0.4), 0 0 16px rgba(255, 70, 70, 0.3);
      animation: subtleGlow 3s ease-in-out infinite alternate;
    }

    @keyframes subtleGlow {
      0% {
        text-shadow: 0 0 6px rgba(255, 50, 50, 0.3), 0 0 12px rgba(255, 70, 70, 0.2);
      }
      100% {
        text-shadow: 0 0 10px rgba(255, 70, 70, 0.5), 0 0 20px rgba(255, 90, 90, 0.4);
      }
    }

    /* Navbar */
    .navbar {
      display: flex;
      justify-content: center;
      gap: 10px;
      background: #0d0d0d;
      border-bottom: 1px solid #222;
      padding: 12px 0;
      border-radius: 14px;
      box-shadow: 0 0 15px rgba(255, 255, 255, 0.05);
    }

    .tab {
      background: #111;
      color: #fff;
      border: 1px solid #333;
      border-radius: 8px;
      padding: 10px 20px;
      cursor: pointer;
      transition: all 0.25s ease;
      font-weight: 500;
      letter-spacing: 0.5px;
    }

    .tab:hover {
      background: #1c1c1c;
      transform: translateY(-2px);
    }

    .tab.active {
      background: #fff;
      color: #000;
      font-weight: 600;
      box-shadow: 0 0 15px rgba(255,255,255,0.1);
    }

    /* Content */
    .content {
      display: none;
      animation: fadeIn 0.6s ease;
    }

    .content.active {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      max-width: 950px;
      margin: 40px auto;
      text-align: left;
      background: #111;
      border: 1px solid #222;
      border-radius: 16px;
      padding: 30px;
      box-shadow: 0 0 20px rgba(255,255,255,0.05);
    }

    .text {
      flex: 1;
      margin-right: 25px;
      min-width: 260px;
    }

    .text h2 {
      margin-top: 0;
      color: #fff;
      font-weight: 700;
      letter-spacing: 0.8px;
    }

    .text p {
      line-height: 1.7;
      color: #d1d1d1;
    }

    .image {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .image img {
      width: 250px;
      height: auto;
      border-radius: 12px;
      border: 1px solid #333;
      box-shadow: 0 0 25px rgba(255,255,255,0.05);
      transition: transform 0.3s ease, filter 0.3s ease;
      filter: grayscale(100%);
    }

    .image img:hover {
      transform: scale(1.05);
      filter: grayscale(0%);
    }

    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(10px);}
      to {opacity: 1; transform: translateY(0);}
    }

    a {
      color: #fff;
      text-decoration: none;
      border-bottom: 1px solid #333;
      transition: 0.3s;
    }

    a:hover {
      color: #ccc;
      border-bottom: 1px solid #666;
    }
  </style>

  <!-- Header Section -->
  <div class="header">
    <img src="YOUR_PFP_URL_HERE" alt="Dymiaz Avatar">
    <h1>Dymiaz</h1>
  </div>

  <!-- Navbar -->
  <div class="navbar">
    <button class="tab active" onclick="showTab('test1')">test1</button>
    <button class="tab" onclick="showTab('test2')">test2</button>
  </div>

  <!-- Main Tab -->
  <div id="test1" class="content active">
    <div class="text">
      <h2>Welcome to Test1 👋</h2>
      <p>
        This is your main profile section — what visitors first see when they reach your GitHub.  
        <br><br>
        Keep it sleek, dark, and professional — exactly how your brand feels.  
        You can include a personal message, tagline, or even add GitHub stats below.
      </p>
    </div>
    <div class="image">
      <img src="YOUR_RIGHT_IMAGE_1_URL_HERE" alt="Test1 Image">
    </div>
  </div>

  <!-- Second Tab -->
  <div id="test2" class="content">
    <div class="text">
      <h2>Welcome to Test2 ⚙️</h2>
      <p>
        This tab is for projects, concepts, or visual showcases.  
        Use it to highlight repos, progress, or creative works with matching dark visuals.  
        Everything stays consistent with the black-and-white theme and cherry accent.
      </p>
    </div>
    <div class="image">
      <img src="YOUR_RIGHT_IMAGE_2_URL_HERE" alt="Test2 Image">
    </div>
  </div>

  <script>
    function showTab(tabId) {
      document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
      document.querySelectorAll('.content').forEach(c => c.classList.remove('active'));
      document.querySelector(`[onclick="showTab('${tabId}')"]`).classList.add('active');
      document.getElementById(tabId).classList.add('active');
    }
  </script>
</div>
