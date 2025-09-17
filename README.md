# rajjeet-saha.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ImmersiLearn VR | Transformative Learning for ASD & ID</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet" />
<script src="https://kit.fontawesome.com/3b161c540c.js" crossorigin="anonymous"></script>
<style>
  :root {
    --primary: #4a6cf7;
    --primary-dark: #3c5ce0;
    --secondary: #6cbbf2;
    --accent: #ff6b6b;
    --success: #4ade80;
    --background: #f8fafc;
    --card-bg: #ffffff;
    --text: #1e293b;
    --text-light: #64748b;
    --border: #e2e8f0;
    --gradient-primary: linear-gradient(135deg, #4a6cf7, #6cbbf2);
    --gradient-accent: linear-gradient(135deg, #ff6b6b, #ff9a3d);
    --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    --shadow-lg: 0 20px 40px rgba(0, 0, 0, 0.15);
    --color-module1: #f9a825;
    --color-module2: #0288d1;
    --color-module3: #d32f2f;
    --dark-bg: #121212;
    --dark-card-bg: #1e1e1e;
    --dark-text: #e0e0e0;
    --dark-text-light: #a0a0a0;
    --dark-border: #333;
  }

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Poppins', sans-serif;
    background-color: var(--background);
    color: var(--text);
    line-height: 1.6;
    overflow-x: hidden;
    transition: background-color 0.3s, color 0.3s;
  }

  /* Dark mode styles */
  body.dark-mode {
    background-color: var(--dark-bg);
    color: var(--dark-text);
  }
  body.dark-mode .login-container,
  body.dark-mode .card,
  body.dark-mode .stat-card,
  body.dark-mode .sidebar,
  body.dark-mode .dashboard-header,
  body.dark-mode .content-card {
    background-color: var(--dark-card-bg);
    box-shadow: none;
    border-color: var(--dark-border);
  }
  body.dark-mode .input-group input {
    background-color: var(--dark-card-bg);
    border-color: var(--dark-border);
    color: var(--dark-text);
  }
  body.dark-mode .input-group input::placeholder {
    color: var(--dark-text-light);
  }
  body.dark-mode .nav-item,
  body.dark-mode .user-info,
  body.dark-mode .progress-name,
  body.dark-mode .progress-date,
  body.dark-mode .progress-value {
    color: var(--dark-text);
  }
  body.dark-mode .nav-item:hover,
  body.dark-mode .nav-item.active {
    background: rgba(74, 108, 247, 0.2);
    color: var(--primary);
  }
  body.dark-mode .progress-item {
    border-bottom: 1px solid var(--dark-border);
  }
  body.dark-mode .user-avatar {
    background: var(--primary);
    color: white;
  }

    /* Login Screen */
  #login-screen {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    /* colorful gradient background */
    background: linear-gradient(45deg, #ff6b6b, #f9a825, #4a6cf7, #6cbbf2);
    background-size: 400% 400%;
    animation: gradientBG 15s ease infinite;
    padding: 20px;
    position: relative;
  }
  @keyframes gradientBG {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
  }

  .login-container {
    background-color: var(--card-bg);
    width: 100%;
    max-width: 420px;
    border-radius: 20px;
    padding: 40px 30px 30px;
    box-shadow: var(--shadow-lg);
    text-align: center;
    animation: fadeIn 0.8s ease-in-out;
    z-index: 2;
  }

  .login-logo {
    margin-bottom: 30px;
  }

  .login-logo h1 {
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    font-size: 2.5rem;
    color: var(--primary);
    margin-bottom: 10px;
  }

  .login-logo p {
    color: var(--text-light);
    font-size: 1rem;
  }

  .user-type-selector {
    display: flex;
    margin-bottom: 25px;
    background: #f1f5f9;
    padding: 4px;
    border-radius: 10px;
    justify-content: center;
    gap: 15px;
  }

  .user-type {
    flex: 1;
    text-align: center;
    padding: 10px 0;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s;
    font-weight: 600;
    font-size: 1.1rem;
    color: var(--text-light);
    user-select: none;
  }

  .user-type.active {
    background: var(--card-bg);
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    color: var(--primary);
  }

  .login-form {
    text-align: left;
  }

  .input-group {
    margin-bottom: 20px;
  }

  .input-group label {
    display: block;
    margin-bottom: 8px;
    font-weight: 500;
    color: var(--text);
  }

  .input-group input {
    width: 100%;
    padding: 15px;
    border: 1px solid var(--border);
    border-radius: 10px;
    font-size: 1rem;
    transition: all 0.3s;
  }

  .input-group input:focus {
    outline: none;
    border-color: var(--primary);
    box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.2);
  }

  .btn {
    padding: 15px;
    border: none;
    border-radius: 10px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    width: 100%;
  }

  .btn-primary {
    background: var(--gradient-primary);
    color: white;
  }

  .btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 20px rgba(74, 108, 247, 0.3);
  }

  .login-extra {
    margin-top: 15px;
    text-align: center;
    font-size: 0.9rem;
    color: var(--text-light);
  }
  .login-extra a {
    color: var(--primary);
    cursor: pointer;
    text-decoration: none;
    font-weight: 600;
  }
  .login-extra a:hover {
    text-decoration: underline;
  }

  /* Main Dashboard */
  #main-dashboard {
    display: none;
    min-height: 100vh;
  }

  .dashboard-header {
    background: var(--gradient-primary);
    color: white;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: var(--shadow);
  }

  .header-logo h2 {
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    font-size: 1.8rem;
  }

  .user-profile {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .user-avatar {
    width: 45px;
    height: 45px;
    border-radius: 50%;
    background: var(--secondary);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: 600;
    font-size: 1.2rem;
  }

  .dashboard-container {
    display: flex;
  }

  .sidebar {
    width: 260px;
    background: var(--card-bg);
    height: calc(100vh - 80px);
    border-right: 1px solid var(--border);
    padding: 20px 0;
    overflow-y: auto;
    transition: background-color 0.3s, color 0.3s;
  }

  .nav-item {
    padding: 15px 25px;
    display: flex;
    align-items: center;
    gap: 15px;
    color: var(--text);
    text-decoration: none;
    transition: all 0.3s;
    font-weight: 500;
    cursor: pointer;
    user-select: none;
  }

  .nav-item:hover,
  .nav-item.active {
    background: rgba(74, 108, 247, 0.1);
    color: var(--primary);
  }

  .nav-item i {
    font-size: 1.2rem;
    width: 24px;
  }

  .dashboard-content {
    flex: 1;
    padding: 30px;
    overflow-y: auto;
    height: calc(100vh - 80px);
    transition: background-color 0.3s, color 0.3s;
  }

  .dashboard-content h2 {
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    margin-bottom: 25px;
    color: var(--text);
    font-size: 1.8rem;
  }

  /* Dashboard Sections */
  .dashboard-section {
    display: none;
    animation: fadeIn 0.5s ease-in-out;
  }

  .dashboard-section.active {
    display: block;
  }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-bottom: 30px;
  }

  .stat-card {
    background: var(--card-bg);
    border-radius: 15px;
    padding: 25px;
    box-shadow: var(--shadow);
    display: flex;
    flex-direction: column;
    position: relative;
    overflow: hidden;
  }

  /* Add subtle background images or colors in stat cards */
  .stat-card.active-patients::before {
    content: "";
    position: absolute;
    top: -20px;
    right: -20px;
    width: 120px;
    height: 120px;
    background: url('https://cdn-icons-png.flaticon.com/512/1077/1077114.png') no-repeat center/contain;
    opacity: 0.1;
    pointer-events: none;
  }
  .stat-card.completion-rate::before {
    content: "";
    position: absolute;
    top: -15px;
    left: -15px;
    width: 110px;
    height: 110px;
    background: url('https://cdn-icons-png.flaticon.com/512/190/190411.png') no-repeat center/contain;
    opacity: 0.1;
    pointer-events: none;
  }
  .stat-card.avg-session-time::before {
    content: "";
    position: absolute;
    bottom: -20px;
    right: -20px;
    width: 130px;
    height: 130px;
    background: url('https://cdn-icons-png.flaticon.com/512/2921/2921222.png') no-repeat center/contain;
    opacity: 0.1;
    pointer-events: none;
  }

  .stat-icon {
    width: 50px;
    height: 50px;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 15px;
    font-size: 1.5rem;
    z-index: 1;
  }

  .stat-icon.blue {
    background: rgba(74, 108, 247, 0.1);
    color: var(--primary);
  }

  .stat-icon.green {
    background: rgba(74, 222, 128, 0.1);
    color: var(--success);
  }

  .stat-icon.orange {
    background: rgba(255, 107, 107, 0.1);
    color: var(--accent);
  }

  .stat-value {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 5px;
    z-index: 1;
  }

  .stat-label {
    color: var(--text-light);
    font-size: 0.9rem;
    z-index: 1;
  }

  .content-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
  }

  .content-card {
    background: var(--card-bg);
    border-radius: 15px;
    padding: 25px;
    box-shadow: var(--shadow);
    transition: background-color 0.3s, color 0.3s;
  }

  .content-card h3 {
    font-family: 'Montserrat', sans-serif;
    font-weight: 600;
    margin-bottom: 15px;
    color: var(--text);
    font-size: 1.3rem;
  }

  .demo-video {
    width: 100%;
    border-radius: 12px;
    overflow: hidden;
    position: relative;
    margin-bottom: 20px;
  }

  .demo-video img {
    width: 100%;
    height: 180px;
    object-fit: cover;
  }

  .play-button {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 60px;
    height: 60px;
    background: rgba(255, 255, 255, 0.8);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: all 0.3s;
  }

  .play-button:hover {
    background: rgba(255, 255, 255, 1);
    transform: translate(-50%, -50%) scale(1.1);
  }

  .play-button i {
    color: var(--primary);
    font-size: 1.5rem;
  }

  .progress-list {
    list-style: none;
  }

  .progress-item {
    display: flex;
    justify-content: space-between;
    padding: 15px 0;
    border-bottom: 1px solid var(--border);
  }

  .progress-item:last-child {
    border-bottom: none;
  }

  .progress-info {
    display: flex;
    flex-direction: column;
  }

  .progress-name {
    font-weight: 500;
    margin-bottom: 5px;
  }

  .progress-date {
    color: var(--text-light);
    font-size: 0.85rem;
  }

  .progress-value {
    font-weight: 600;
    color: var(--primary);
  }

  /* Animations */
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(10px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Responsive */
  @media (max-width: 992px) {
    .dashboard-container {
      flex-direction: column;
    }

    .sidebar {
      width: 100%;
      height: auto;
    }

    .dashboard-content {
      height: auto;
    }

    .stats-grid {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media (max-width: 768px) {
    .stats-grid {
      grid-template-columns: 1fr;
    }

    .content-grid {
      grid-template-columns: 1fr;
    }

    .login-container {
      padding: 30px 20px;
    }
  }

  /* Patient Management Table */
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.95rem;
  }
  th, td {
    padding: 12px 15px;
    border-bottom: 1px solid var(--border);
    text-align: left;
  }
  th {
    background-color: var(--secondary);
    color: white;
    font-weight: 600;
  }
  body.dark-mode th {
    background-color: var(--primary-dark);
  }
  tr:hover {
    background-color: rgba(74, 108, 247, 0.1);
  }

 /* Progress Tracking Bars */
  .progress-bar-container {
    margin-top: 20px;
  }
  .progress-bar {
    background: var(--border);
    border-radius: 10px;
    overflow: hidden;
    height: 25px;
    margin-bottom: 15px;
  }
  .progress-bar-fill {
    height: 100%;
    border-radius: 10px;
    transition: width 0.5s ease;
    color: white;
    font-weight: 600;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.9rem;
  }
  .progress-bar-fill.improvement {
    background: var(--success);
  }
  .progress-bar-fill.decline {
    background: var(--accent);
  }
  .progress-bar-label {
    margin-bottom: 5px;
    font-weight: 600;
  }

  /* Learning Modules Cards */
  .modules-list {
    display: flex;
    gap: 30px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .module-card {
    flex: 0 0 250px;
    height: 250px;
    background: var(--card-bg);
    border-radius: 20px;
    padding: 0;
    box-shadow: var(--shadow);
    cursor: pointer;
    color: var(--text);
    font-weight: 700;
    font-size: 1.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.3s, box-shadow 0.3s;
    user-select: none;
    text-align: center;
  }

  .module-card:hover {
    transform: translateY(-8px);
    box-shadow: var(--shadow-lg);
  }

  /* Module Video Page */
  #module-video-page {
    display: none;
    min-height: 100vh;
    padding: 40px 30px;
    position: relative;
    background: url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
    color: white;
  }
  #module-video-page .video-container {
    max-width: 900px;
    margin: 0 auto;
    background: rgba(0,0,0,0.7);
    border-radius: 15px;
    padding: 20px;
  }
  #module-video-page video,
  #module-video-page .video-placeholder {
    width: 100%;
    height: 480px;
    background: #222;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #888;
    font-size: 1.5rem;
  }
  #module-video-page .back-btn {
    position: absolute;
    top: 30px;
    left: 30px;
    background: rgba(0,0,0,0.6);
    border: none;
    color: white;
    padding: 10px 15px;
    border-radius: 8px;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s;
  }
  #module-video-page .back-btn:hover {
    background: rgba(0,0,0,0.9);
  }

  /* Demo Videos Fullscreen */
  #demos-section video,
  #demos-section .video-placeholder {
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    border-radius: 0;
  }
  #demos-section .video-placeholder {
    background: #000;
    color: #666;
    font-size: 2rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  /* Reports Section */
  #reports-section {
    max-width: 900px;
  }
  #reports-section .report-controls {
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
    flex-wrap: wrap;
    gap: 10px;
  }
  #reports-section select {
    padding: 8px 12px;
    border-radius: 8px;
    border: 1px solid var(--border);
    font-size: 1rem;
  }
  #reports-section button {
    background: var(--primary);
    color: white;
    border: none;
    padding: 10px 18px;
    border-radius: 8px;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s;
  }
  #reports-section button:hover {
    background: var(--primary-dark);
  }
  #reports-section table {
    width: 100%;
    border-collapse: collapse;
  }
  #reports-section th, #reports-section td {
    padding: 12px 15px;
    border-bottom: 1px solid var(--border);
    text-align: left;
  }
  #reports-section th {
    background-color: var(--secondary);
    color: white;
  }
  body.dark-mode #reports-section th {
    background-color: var(--primary-dark);
  }
  #reports-section tr:hover {
    background-color: rgba(74, 108, 247, 0.1);
  }

  /* Settings Section */
  #settings-section {
    max-width: 700px;
  }
  #settings-section h3 {
    margin-top: 25px;
    margin-bottom: 15px;
  }
  #settings-section label {
    display: block;
    margin-bottom: 6px;
    font-weight: 600;
  }
  #settings-section input, #settings-section textarea, #settings-section select {
    width: 100%;
    padding: 12px 15px;
    margin-bottom: 20px;
    border-radius: 10px;
    border: 1px solid var(--border);
    font-size: 1rem;
  }
  #settings-section input:focus, #settings-section textarea:focus, #settings-section select:focus {
    outline: none;
    border-color: var(--primary);
    box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.2);
  }
  #settings-section button {
    background: var(--primary);
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 10px;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s;
  }
  #settings-section button:hover {
    background: var(--primary-dark);
  }
  #settings-section .toggle-switch {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 20px;
  }
  #settings-section .toggle-switch input[type="checkbox"] {
    width: 40px;
    height: 20px;
    position: relative;
    appearance: none;
    background: var(--border);
    outline: none;
    border-radius: 20px;
    transition: background 0.3s;
    cursor: pointer;
  }
  #settings-section .toggle-switch input[type="checkbox"]:checked {
    background: var(--primary);
  }
  #settings-section .toggle-switch input[type="checkbox"]::before {
    content: "";
    position: absolute;
    width: 18px;
    height: 18px;
    border-radius: 50%;
    top: 1px;
    left: 1px;
    background: white;
    transition: 0.3s;
  }
  #settings-section .toggle-switch input[type="checkbox"]:checked::before {
    left: 21px;
  }
  #settings-section .issue-list {
    list-style: none;
    padding-left: 0;
  }
  #settings-section .issue-list li {
    margin-bottom: 10px;
  }
  #settings-section .issue-list label {
    font-weight: 500;
    cursor: pointer;
  }

  /* Scrollbar styling for sidebar and dashboard content */
  .sidebar::-webkit-scrollbar,
  .dashboard-content::-webkit-scrollbar {
    width: 8px;
  }
  .sidebar::-webkit-scrollbar-thumb,
  .dashboard-content::-webkit-scrollbar-thumb {
    background-color: rgba(74, 108, 247, 0.3);
    border-radius: 10px;
  }

</style>
</head>
<body>
  <!-- Login Screen -->
  <div id="login-screen">
    <div class="login-container">
      <div class="login-logo">
        <h1>ImmersiLearn VR</h1>
        <p>Transforming Learning for Children with ASD &amp; ID</p>
      </div>

      <div class="user-type-selector">
        <div class="user-type active" data-type="user">
          <i class="fas fa-user"></i> User
        </div>
        <div class="user-type" data-type="supervisor">
          <i class="fas fa-user-shield"></i> Supervisor
        </div>
      </div>

      <div class="login-form">
        <div class="input-group">
          <label for="email">Email Address</label>
          <input type="email" id="email" placeholder="name@example.com" />
        </div>
        <div class="input-group">
          <label for="password">Password</label>
          <input type="password" id="password" placeholder="Enter your password" />
        </div>
        <button class="btn btn-primary" id="login-btn">Login to Dashboard</button>
      </div>

      <div class="login-extra">
        <a href="#" id="forgot-password-link">Forgot Password?</a> | 
        <a href="#" id="sign-up-link">Sign Up</a>
      </div>
    </div>
  </div>

  <!-- Sign Up Screen -->
  <div id="signup-screen" style="display:none; min-height:100vh; display:flex; align-items:center; justify-content:center; background: var(--background);">
    <div class="login-container" style="max-width: 420px;">
      <div class="login-logo">
        <h1>Sign Up</h1>
        <p>Create a new account</p>
      </div>
      <div class="login-form">
        <div class="input-group">
          <label for="signup-name">Full Name</label>
          <input type="text" id="signup-name" placeholder="Your full name" />
        </div>
        <div class="input-group">
          <label for="signup-email">Email Address</label>
          <input type="email" id="signup-email" placeholder="name@example.com" />
        </div>
        <div class="input-group">
          <label for="signup-password">Password</label>
          <input type="password" id="signup-password" placeholder="Create a password" />
        </div>
        <div class="input-group">
          <label for="signup-type">Account Type</label>
          <select id="signup-type">
            <option value="user">User </option>
            <option value="supervisor">Supervisor</option>
          </select>
        </div>
        <button class="btn btn-primary" id="signup-btn">Create Account</button>
      </div>
      <div class="login-extra" style="margin-top: 10px;">
        <a href="#" id="back-to-login-link">Back to Login</a>
      </div>
    </div>
  </div>

  <!-- Forgot Password Screen -->
  <div id="forgot-password-screen" style="display:none; min-height:100vh; display:flex; align-items:center; justify-content:center; background: var(--background);">
    <div class="login-container" style="max-width: 420px;">
      <div class="login-logo">
        <h1>Forgot Password</h1>
        <p>Enter your email to reset password</p>
      </div>
      <div class="login-form">
        <div class="input-group">
          <label for="forgot-email">Email Address</label>
          <input type="email" id="forgot-email" placeholder="name@example.com" />
        </div>
        <button class="btn btn-primary" id="reset-password-btn">Reset Password</button>
      </div>
      <div class="login-extra" style="margin-top: 10px;">
        <a href="#" id="back-to-login-link2">Back to Login</a>
      </div>
    </div>
  </div>

  <!-- Main Dashboard -->
  <div id="main-dashboard">
    <div class="dashboard-header">
      <div class="header-logo">
        <h2>ImmersiLearn VR Dashboard</h2>
      </div>
      <div class="user-profile">
        <div class="user-avatar" id="user-avatar">JD</div>
        <div class="user-info">
          <div class="user-name" id="user-name">Dr. Jane Doe</div>
          <div class="user-role" id="user-role">User </div>
        </div>
      </div>
    </div>

    <div class="dashboard-container">
      <div class="sidebar" id="sidebar">
        <a href="#" class="nav-item active" data-section="overview">
          <i class="fas fa-home"></i> Overview
        </a>
        <a href="#" class="nav-item" data-section="patients" id="nav-patients">
          <i class="fas fa-users"></i> Patients
        </a>
        <a href="#" class="nav-item" data-section="progress">
          <i class="fas fa-chart-line"></i> Progress Tracking
        </a>
        <a href="#" class="nav-item" data-section="modules">
          <i class="fas fa-cube"></i> Learning Modules
        </a>
        <a href="#" class="nav-item" data-section="demos" id="nav-demos">
          <i class="fas fa-video"></i> Demo Videos
        </a>
        <a href="#" class="nav-item" data-section="reports">
          <i class="fas fa-file-alt"></i> Reports
        </a>
        <a href="#" class="nav-item" data-section="settings">
          <i class="fas fa-cog"></i> Settings
        </a>
        <a href="#" class="nav-item" id="logout-btn">
          <i class="fas fa-sign-out-alt"></i> Logout
        </a>
      </div>

      <div class="dashboard-content">
        <!-- Overview Section -->
        <div class="dashboard-section active" id="overview-section">
          <h2>Dashboard Overview</h2>

          <div class="stats-grid">
            <div class="stat-card active-patients">
              <div class="stat-icon blue">
                <i class="fas fa-users"></i>
              </div>
              <div class="stat-value" id="stat-active-patients">24</div>
              <div class="stat-label">Active Patients</div>
            </div>

            <div class="stat-card completion-rate">
              <div class="stat-icon green">
                <i class="fas fa-check-circle"></i>
              </div>
              <div class="stat-value" id="stat-completion-rate">83%</div>
              <div class="stat-label">Average Completion Rate</div>
            </div>

            <div class="stat-card avg-session-time">
              <div class="stat-icon orange">
                <i class="fas fa-clock"></i>
              </div>
              <div class="stat-value" id="stat-avg-session-time">7.5</div>
              <div class="stat-label">Avg. Session Time (mins)</div>
            </div>
          </div>

          <div class="content-grid">
            <div class="content-card">
              <h3>Recent Activity</h3>
              <div class="progress-list" id="recent-activity-list">
                <div class="progress-item">
                  <div class="progress-info">
                    <div class="progress-name">Michael completed Morning Routine</div>
                    <div class="progress-date">Today, 10:24 AM</div>
                  </div>
                  <div class="progress-value">92%</div>
                </div>
                <div class="progress-item">
                  <div class="progress-info">
                    <div class="progress-name">Sarah practiced Social Greetings</div>
                    <div class="progress-date">Yesterday, 3:45 PM</div>
                  </div>
                  <div class="progress-value">78%</div>
                </div>
                <div class="progress-item">
                  <div class="progress-info">
                    <div class="progress-name">Alex started Emotional Regulation</div>
                    <div class="progress-date">Sept 12, 9:15 AM</div>
                  </div>
                  <div class="progress-value">In Progress</div>
                </div>
              </div>
            </div>

            <div class="content-card">
              <h3>Latest Demo Video</h3>
              <div class="demo-video">
                <img src="https://placeholder-image-service.onrender.com/image/500x300?prompt=VR%20learning%20environment%20for%20children%20with%20ASD%20and%20ID&id=1" alt="Immersive VR learning environment showing a child interacting with educational content" />
                <div class="play-button">
                  <i class="fas fa-play"></i>
                </div>
              </div>
              <p>Morning Routine Module - v2.3 updated with improved interaction feedback</p>
            </div>
          </div>
        </div>

        <!-- Patients Section -->
        <div class="dashboard-section" id="patients-section">
          <h2>Patient Management</h2>
          <table id="patients-table" aria-label="Patient Management Table">
            <thead>
              <tr>
                <th>Name</th>
                <th>Age</th>
                <th>Diagnosis</th>
                <th>Last Session</th>
                <th>Status</th>
              </tr>
            </thead>
            <tbody>
              <!-- Patient rows will be inserted dynamically -->
            </tbody>
          </table>
        </div>

        <!-- Progress Tracking Section -->
        <div class="dashboard-section" id="progress-section">
          <h2>Progress Tracking</h2>
          <p>Comparison of user progress over time:</p>
          <div id="progress-comparison">
            <!-- Progress bars will be inserted dynamically -->
          </div>
        </div>

        <!-- Learning Modules Section -->
        <div class="dashboard-section" id="modules-section">
          <h2>Learning Modules</h2>
          <div class="modules-list" id="modules-list">
            <div class="module-card module1" data-module="module1">Module 1</div>
            <div class="module-card module2" data-module="module2">Module 2</div>
            <div class="module-card module3" data-module="module3">Module 3</div>
          </div>
        </div>

        <!-- Module Video Page -->
        <div id="module-video-page">
          <button class="back-btn" id="module-back-btn"><i class="fas fa-arrow-left"></i> Back</button>
          <div class="video-container">
            <div class="video-placeholder" id="module-video-placeholder">
              Video will be uploaded here later
            </div>
          </div>
        </div>

        <!-- Demo Videos Section -->
        <div class="dashboard-section" id="demos-section">
          <h2> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Demo Videos</h2>
          <div class="video-placeholder" style="height: 100vh; width: 100vw; background: #000; color: #666; display: flex; align-items: center; justify-content: center; font-size: 2rem;">
            Demo video will cover the whole screen here
          </div>
        </div>

        <!-- Reports Section -->
        <div class="dashboard-section" id="reports-section">
          <h2>Reports</h2>
          <div class="report-controls">
            <label for="sort-reports">Sort by:</label>
            <select id="sort-reports">
              <option value="date-desc">Date (Newest First)</option>
              <option value="date-asc">Date (Oldest First)</option>
              <option value="name-asc">Name (A-Z)</option>
              <option value="name-desc">Name (Z-A)</option>
            </select>
            <button id="download-pdf-btn">Download PDF</button>
          </div>
          <table id="reports-table" aria-label="Reports Table">
            <thead>
              <tr>
                <th>Patient Name</th>
                <th>Report Date</th>
                <th>Summary</th>
              </tr>
            </thead>
            <tbody>
              <!-- Report rows inserted dynamically -->
            </tbody>
          </table>
        </div>

        <!-- Settings Section -->
        <div class="dashboard-section" id="settings-section">
          <h2>Settings</h2>

          <h3>Edit Profile</h3>
          <label for="profile-name">Name</label>
          <input type="text" id="profile-name" />
          <label for="profile-email">Email</label>
          <input type="email" id="profile-email" />
          <button id="save-profile-btn">Save Profile</button>

          <h3>Change Password</h3>
          <label for="current-password">Current Password</label>
          <input type="password" id="current-password" />
          <label for="new-password">New Password</label>
          <input type="password" id="new-password" />
          <label for="confirm-password">Confirm New Password</label>
          <input type="password" id="confirm-password" />
          <button id="change-password-btn">Change Password</button>

          <h3>Contact Us</h3>
          <p>Phone: +91 9115207977</p>
          <p>Email: dratexinclusion@gmail.com</p>
          <p>Social Media:</p>
          <ul>
            <li><a href="#" target="_blank">Facebook</a></li>
            <li><a href="#" target="_blank">Twitter</a></li>
            <li><a href="#" target="_blank">Instagram</a></li>
          </ul>

          <h3>Dark Mode</h3>
          <div class="toggle-switch">
            <input type="checkbox" id="dark-mode-toggle" />
            <label for="dark-mode-toggle">Enable Dark Mode</label>
          </div>

          <h3>Report an Issue</h3>
          <label for="issue-select">Select a problem:</label>
          <select id="issue-select">
            <option value="">-- Select an issue --</option>
            <option value="navigation">How to navigate through the dashboard</option>
            <option value="login">Login issues</option>
            <option value="video">Video playback problems</option>
            <option value="module">Module content questions</option>
            <option value="other">Other</option>
          </select>
          <label for="issue-description">Describe your issue:</label>
          <textarea id="issue-description" rows="4" placeholder="Provide more details here..."></textarea>
          <button id="submit-issue-btn">Submit Issue</button>
          <div id="issue-feedback" style="margin-top:10px; font-weight:600;"></div>
        </div>
      </div>
    </div>
  </div>

<script>
  // Data for patients
  const patientsData = [
    { name: "Michael Smith", age: 8, diagnosis: "ASD", lastSession: "2024-06-10", status: "Active" },
    { name: "Sarah Johnson", age: 10, diagnosis: "ID", lastSession: "2024-06-09", status: "Active" },
    { name: "Alex Lee", age: 7, diagnosis: "ASD", lastSession: "2024-06-08", status: "In Progress" },
    { name: "Emily Davis", age: 9, diagnosis: "ID", lastSession: "2024-06-07", status: "Active" },
    { name: "Daniel Brown", age: 11, diagnosis: "ASD", lastSession: "2024-06-05", status: "Inactive" },
    { name: "Olivia Wilson", age: 8, diagnosis: "ID", lastSession: "2024-06-04", status: "Active" }
  ];

  // Data for reports
  const reportsData = patientsData.map(p => ({
    name: p.name,
    date: new Date(p.lastSession),
    summary: Report summary for ${p.name} with diagnosis ${p.diagnosis}.
  }));

  // Current logged in user info (simulate)
  let currentUser = {
    name: "Dr. Jane Doe",
    role: "user", // or "supervisor"
    initials: "JD"
  };

  // Utility to format date
  function formatDate(date) {
    return date.toLocaleDateString() + " " + date.toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
  }

  // Populate patients table
  function populatePatients() {
    const tbody = document.querySelector("#patients-table tbody");
    tbody.innerHTML = "";
    patientsData.forEach(p => {
      const tr = document.createElement("tr");
      tr.innerHTML = `
        <td>${p.name}</td>
        <td>${p.age}</td>
        <td>${p.diagnosis}</td>
        <td>${p.lastSession}</td>
        <td>${p.status}</td>
      `;
      tbody.appendChild(tr);
    });
  }

  // Populate reports table
  function populateReports(sortBy = "date-desc") {
    const tbody = document.querySelector("#reports-table tbody");
    tbody.innerHTML = "";

    let sortedReports = [...reportsData];
    switch(sortBy) {
      case "date-desc":
        sortedReports.sort((a,b) => b.date - a.date);
        break;
      case "date-asc":
        sortedReports.sort((a,b) => a.date - b.date);
        break;
      case "name-asc":
        sortedReports.sort((a,b) => a.name.localeCompare(b.name));
        break;
      case "name-desc":
        sortedReports.sort((a,b) => b.name.localeCompare(a.name));
        break;
    }

    sortedReports.forEach(r => {
      const tr = document.createElement("tr");
      tr.innerHTML = `
        <td>${r.name}</td>
        <td>${r.date.toLocaleDateString()}</td>
        <td>${r.summary}</td>
      `;
      tbody.appendChild(tr);
    });
  }

  // Generate progress tracking line graphs
  function generateProgressTracking() {
    const container = document.getElementById("progress-comparison");
    container.innerHTML = "";

    patientsData.forEach(p => {
      // Generate random data points for past and present (7 days)
      const days = 7;
      const pastData = Array.from({length: days}, () => Math.floor(Math.random() * 50) + 30);
      const presentData = pastData.map(val => Math.min(100, val + Math.floor(Math.random() * 30)));

      // Create SVG line graph container
      const svgWidth = 300;
      const svgHeight = 150;
      const padding = 30;

      // Scale function for y-axis (0-100%)
      const scaleY = val => svgHeight - padding - (val / 100) * (svgHeight - 2 * padding);
      // Scale function for x-axis
      const scaleX = i => padding + (i * (svgWidth - 2 * padding)) / (days - 1);

      // Create SVG element
      const svgNS = "http://www.w3.org/2000/svg";
      const svg = document.createElementNS(svgNS, "svg");
      svg.setAttribute("width", svgWidth);
      svg.setAttribute("height", svgHeight);
      svg.style.marginBottom = "30px";
      svg.style.background = "var(--card-bg)";
      svg.style.borderRadius = "15px";
      svg.style.boxShadow = "var(--shadow)";
      svg.style.display = "block";

      // Title label
      const label = document.createElement("div");
      label.className = "progress-bar-label";
      label.textContent = ${p.name} (${p.diagnosis});
      label.style.fontWeight = "700";
      label.style.marginBottom = "8px";

      // Draw axes lines
      const axisX = document.createElementNS(svgNS, "line");
      axisX.setAttribute("x1", padding);
      axisX.setAttribute("y1", svgHeight - padding);
      axisX.setAttribute("x2", svgWidth - padding);
      axisX.setAttribute("y2", svgHeight - padding);
      axisX.setAttribute("stroke", "#ccc");
      axisX.setAttribute("stroke-width", "2");
      svg.appendChild(axisX);

      const axisY = document.createElementNS(svgNS, "line");
      axisY.setAttribute("x1", padding);
      axisY.setAttribute("y1", padding);
      axisY.setAttribute("x2", padding);
      axisY.setAttribute("y2", svgHeight - padding);
      axisY.setAttribute("stroke", "#ccc");
      axisY.setAttribute("stroke-width", "2");
      svg.appendChild(axisY);

      // Function to create polyline points string
      const createPoints = data => data.map((val, i) => ${scaleX(i)},${scaleY(val)}).join(" ");

      // Past data polyline (red)
      const pastLine = document.createElementNS(svgNS, "polyline");
      pastLine.setAttribute("points", createPoints(pastData));
      pastLine.setAttribute("fill", "none");
      pastLine.setAttribute("stroke", "var(--accent)");
      pastLine.setAttribute("stroke-width", "3");
      svg.appendChild(pastLine);

      // Present data polyline (green)
      const presentLine = document.createElementNS(svgNS, "polyline");
      presentLine.setAttribute("points", createPoints(presentData));
      presentLine.setAttribute("fill", "none");
      presentLine.setAttribute("stroke", "var(--success)");
      presentLine.setAttribute("stroke-width", "3");
      svg.appendChild(presentLine);

      // Legend
      const legend = document.createElement("div");
      legend.style.display = "flex";
      legend.style.justifyContent = "center";
      legend.style.gap = "20px";
      legend.style.marginBottom = "20px";

      const pastLegend = document.createElement("div");
      pastLegend.innerHTML = <span style="display:inline-block;width:15px;height:15px;background:var(--accent);margin-right:6px;"></span>Past;

      const presentLegend = document.createElement("div");
      presentLegend.innerHTML = <span style="display:inline-block;width:15px;height:15px;background:var(--success);margin-right:6px;"></span>Present;

      legend.appendChild(pastLegend);
      legend.appendChild(presentLegend);

      // Container div for label + legend + svg
      const wrapper = document.createElement("div");
      wrapper.style.marginBottom = "40px";
      wrapper.style.maxWidth = svgWidth + "px";
      wrapper.style.marginLeft = "auto";
      wrapper.style.marginRight = "auto";

      wrapper.appendChild(label);
      wrapper.appendChild(legend);
      wrapper.appendChild(svg);

      container.appendChild(wrapper);
    });
  }

  // Show/hide nav items based on role
  function updateNavForRole(role) {
    const patientsNav = document.getElementById("nav-patients");
    const demosNav = document.getElementById("nav-demos");

    if(role === "user") {
      patientsNav.style.display = "none";
      demosNav.style.display = "block";
    } else if(role === "supervisor") {
      patientsNav.style.display = "block";
      demosNav.style.display = "none";}
      }

  // Navigation and section switching
  const navItems = document.querySelectorAll('.nav-item');
  const sections = document.querySelectorAll('.dashboard-section');
  const moduleVideoPage = document.getElementById('module-video-page');
  const modulesList = document.getElementById('modules-list');

  function showSection(sectionId) {
    sections.forEach(section => {
      section.classList.remove('active');
    });
    moduleVideoPage.style.display = 'none';
    if(sectionId === 'module-video-page') {
      moduleVideoPage.style.display = 'block';
    } else {
      const section = document.getElementById(sectionId + '-section');
      if(section) section.classList.add('active');
    }
  }

  navItems.forEach(item => {
    item.addEventListener('click', e => {
      e.preventDefault();
      if(item.id === 'logout-btn') return;
      const targetSection = item.getAttribute('data-section');
      if(!targetSection) return;

      // Update active nav
      navItems.forEach(nav => nav.classList.remove('active'));
      item.classList.add('active');

      showSection(targetSection);
    });
  });

  // Module cards click event
  modulesList.querySelectorAll('.module-card').forEach(card => {
    card.addEventListener('click', () => {
      // Show module video page
      showSection('module-video-page');
      // Update video placeholder text
      const moduleName = card.textContent.trim();
      const placeholder = document.getElementById('module-video-placeholder');
      placeholder.textContent = ${moduleName} video will be uploaded here later;
    });
  });

  // Back button on module video page
  document.getElementById('module-back-btn').addEventListener('click', () => {
    // Return to modules section
    showSection('modules');
    // Set modules nav active
    navItems.forEach(nav => nav.classList.remove('active'));
    document.querySelector('.nav-item[data-section="modules"]').classList.add('active');
  });

  // Login functionality
  const loginBtn = document.getElementById('login-btn');
  const loginScreen = document.getElementById('login-screen');
  const mainDashboard = document.getElementById('main-dashboard');
  const userTypes = document.querySelectorAll('.user-type');
  const userNameDisplay = document.getElementById('user-name');
  const userRoleDisplay = document.getElementById('user-role');
  const userAvatar = document.getElementById('user-avatar');

  loginBtn.addEventListener('click', () => {
    // Get selected user type
    const selectedType = document.querySelector('.user-type.active').getAttribute('data-type');
    currentUser .role = selectedType;
    currentUser .name = selectedType === 'user' ? 'John Doe' : 'Dr. Jane Doe';
    currentUser .initials = currentUser .name.split(' ').map(n => n[0]).join('').toUpperCase();

    // Update dashboard user info
    userNameDisplay.textContent = currentUser .name;
    userRoleDisplay.textContent = currentUser .role.charAt(0).toUpperCase() + currentUser .role.slice(1);
    userAvatar.textContent = currentUser .initials;

    // Show/hide nav items based on role
    updateNavForRole(currentUser .role);

    // Show dashboard, hide login
    loginScreen.style.display = 'none';
    mainDashboard.style.display = 'block';

    // Populate patients and reports
    populatePatients();
    populateReports();
    generateProgressTracking();

    // Show overview section by default
    showSection('overview');
    navItems.forEach(nav => nav.classList.remove('active'));
    document.querySelector('.nav-item[data-section="overview"]').classList.add('active');
  });

  // Logout functionality
  document.getElementById('logout-btn').addEventListener('click', e => {
    e.preventDefault();
    mainDashboard.style.display = 'none';
    loginScreen.style.display = 'flex';
    // Reset login form
    document.getElementById('email').value = '';
    document.getElementById('password').value = '';
    // Reset user type to user
    userTypes.forEach(t => t.classList.remove('active'));
    userTypes[0].classList.add('active');
  });

  // User type selection on login screen
  userTypes.forEach(type => {
    type.addEventListener('click', () => {
      userTypes.forEach(t => t.classList.remove('active'));
      type.classList.add('active');
    });
  });

  // Sign Up and Forgot Password navigation
  const signupScreen = document.getElementById('signup-screen');
  const forgotPasswordScreen = document.getElementById('forgot-password-screen');

  document.getElementById('sign-up-link').addEventListener('click', e => {
    e.preventDefault();
    loginScreen.style.display = 'none';
    signupScreen.style.display = 'flex';
  });

  document.getElementById('forgot-password-link').addEventListener('click', e => {
    e.preventDefault();
    loginScreen.style.display = 'none';
    forgotPasswordScreen.style.display = 'flex';
  });

  document.getElementById('back-to-login-link').addEventListener('click', e => {
    e.preventDefault();
    signupScreen.style.display = 'none';
    loginScreen.style.display = 'flex';
  });

  document.getElementById('back-to-login-link2').addEventListener('click', e => {
    e.preventDefault();
    forgotPasswordScreen.style.display = 'none';
    loginScreen.style.display = 'flex';
  });

  // Sign Up button (simulate account creation)
  document.getElementById('signup-btn').addEventListener('click', () => {
    alert('Account created successfully! Please login.');
    signupScreen.style.display = 'none';
    loginScreen.style.display = 'flex';
  });

  // Reset Password button (simulate)
  document.getElementById('reset-password-btn').addEventListener('click', () => {
    alert('Password reset link sent to your email.');
    forgotPasswordScreen.style.display = 'none';
    loginScreen.style.display = 'flex';
  });

  // Reports sorting
  document.getElementById('sort-reports').addEventListener('change', e => {
    populateReports(e.target.value);
  });

  // Download PDF report (simple text PDF generation)
  document.getElementById('download-pdf-btn').addEventListener('click', () => {
    let content = 'ImmersiLearn VR - Patient Reports\n\n';
    reportsData.forEach(r => {
      content += Name: ${r.name}\nDate: ${r.date.toLocaleDateString()}\nSummary: ${r.summary}\n\n;
    });
    const blob = new Blob([content], { type: 'application/pdf' });
    const link = document.createElement('a');
    link.href = URL.createObjectURL(blob);
    link.download = 'patient_reports.txt'; // Using .txt because PDF generation requires libraries
    link.click();
  });

  // Settings: Save profile
  document.getElementById('save-profile-btn').addEventListener('click', () => {
    const newName = document.getElementById('profile-name').value.trim();
    const newEmail = document.getElementById('profile-email').value.trim();
    if(newName && newEmail) {
      currentUser .name = newName;
      userNameDisplay.textContent = newName;
      alert('Profile updated successfully!');
    } else {
      alert('Please fill in all profile fields.');
    }
  });

  // Settings: Change password (simulate)
  document.getElementById('change-password-btn').addEventListener('click', () => {
    const currentPass = document.getElementById('current-password').value;
    const newPass = document.getElementById('new-password').value;
    const confirmPass = document.getElementById('confirm-password').value;
    if(!currentPass || !newPass || !confirmPass) {
      alert('Please fill in all password fields.');
      return;
    }
    if(newPass !== confirmPass) {
      alert('New passwords do not match.');
      return;
    }
    alert('Password changed successfully!');
    // Clear fields
    document.getElementById('current-password').value = '';
    document.getElementById('new-password').value = '';
    document.getElementById('confirm-password').value = '';
  });

  // Dark mode toggle
  const darkModeToggle = document.getElementById('dark-mode-toggle');
  darkModeToggle.addEventListener('change', () => {
    if(darkModeToggle.checked) {
      document.body.classList.add('dark-mode');
    } else {
      document.body.classList.remove('dark-mode');
    }
  });

  // Report an issue submission
  document.getElementById('submit-issue-btn').addEventListener('click', () => {
    const issueType = document.getElementById('issue-select').value;
    const issueDesc = document.getElementById('issue-description').value.trim();
    const feedback = document.getElementById('issue-feedback');

    if(!issueType) {
      feedback.style.color = 'red';
      feedback.textContent = 'Please select an issue type.';
      return;
    }
    if(issueType === 'other' && !issueDesc) {
      feedback.style.color = 'red';
      feedback.textContent = 'Please describe your issue.';
      return;
    }

    // Simulate submission
    feedback.style.color = 'green';
    feedback.textContent = 'Thank you for reporting the issue. We will look into it.';
    // Clear inputs
    document.getElementById('issue-select').value = '';
    document.getElementById('issue-description').value = '';
  });

  // Initialize profile fields on dashboard load
  function initProfileFields() {
    document.getElementById('profile-name').value = currentUser .name;
    document.getElementById('profile-email').value = 'user@example.com'; // Placeholder email
  }

  // Initialize on page load
  window.addEventListener('load', () => {
    initProfileFields();
  });
</script>
</body>
</html>
