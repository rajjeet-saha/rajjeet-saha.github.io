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
    --color-module1: #ffb300;
    --color-module2: #039be5;
    --color-module3: #e53935;
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
  body.dark-mode .content-card,
  body.dark-mode .progress-graph-svg {
    background-color: var(--dark-card-bg);
    box-shadow: none;
    border-color: var(--dark-border);
  }
  body.dark-mode .input-group input,
  body.dark-mode .input-group select {
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
  body.dark-mode .progress-value,
  body.dark-mode .progress-graph-label {
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

  .input-group input, .input-group select {
    width: 100%;
    padding: 15px;
    border: 1px solid var(--border);
    border-radius: 10px;
    font-size: 1rem;
    transition: all 0.3s;
    font-family: 'Poppins', sans-serif; /* Ensure select inherits font */
  }

  .input-group input:focus, .input-group select:focus {
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
    height: calc(100vh - 85px); /* Adjusted for header height */
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
    height: calc(100vh - 85px); /* Adjusted for header height */
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
  .stat-icon.blue { background: rgba(74, 108, 247, 0.1); color: var(--primary); }
  .stat-icon.green { background: rgba(74, 222, 128, 0.1); color: var(--success); }
  .stat-icon.orange { background: rgba(255, 107, 107, 0.1); color: var(--accent); }

  .stat-value { font-size: 2rem; font-weight: 700; margin-bottom: 5px; z-index: 1; }
  .stat-label { color: var(--text-light); font-size: 0.9rem; z-index: 1; }

  .content-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }

  .content-card { background: var(--card-bg); border-radius: 15px; padding: 25px; box-shadow: var(--shadow); transition: background-color 0.3s, color 0.3s; }
  .content-card h3 { font-family: 'Montserrat', sans-serif; font-weight: 600; margin-bottom: 15px; color: var(--text); font-size: 1.3rem; }

  .progress-list { list-style: none; }
  .progress-item { display: flex; justify-content: space-between; padding: 15px 0; border-bottom: 1px solid var(--border); }
  .progress-item:last-child { border-bottom: none; }
  .progress-info { display: flex; flex-direction: column; }
  .progress-name { font-weight: 500; margin-bottom: 5px; }
  .progress-date { color: var(--text-light); font-size: 0.85rem; }
  .progress-value { font-weight: 600; color: var(--primary); }

  @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

  /* Patient Management Table */
  table { width: 100%; border-collapse: collapse; font-size: 0.95rem; }
  th, td { padding: 12px 15px; border-bottom: 1px solid var(--border); text-align: left; }
  th { background-color: var(--secondary); color: white; font-weight: 600; }
  body.dark-mode th { background-color: var(--primary-dark); }
  tr:hover { background-color: rgba(74, 108, 247, 0.1); }

  /* Progress Tracking Graphs */
  .progress-graph-wrapper { margin-bottom: 40px; max-width: 300px; margin-left: auto; margin-right: auto; }
  .progress-graph-label { font-weight: 700; margin-bottom: 8px; text-align: center; }
  .progress-graph-legend { display: flex; justify-content: center; gap: 20px; margin-bottom: 10px; font-size: 0.9rem; }
  .progress-graph-svg { border-radius: 15px; box-shadow: var(--shadow); display: block; background-color: var(--card-bg); }
  .axis-line { stroke: var(--border); stroke-width: 2; }
  .past-line { fill: none; stroke: var(--accent); stroke-width: 3; }
  .present-line { fill: none; stroke: var(--success); stroke-width: 3; }

  /* Learning Modules Cards */
  .modules-list { display: flex; gap: 30px; flex-wrap: wrap; justify-content: center; }
  .module-card { flex: 0 0 250px; height: 250px; border-radius: 20px; padding: 20px; box-shadow: var(--shadow); cursor: pointer; color: white; font-weight: 700; font-size: 1.5rem; display: flex; align-items: center; justify-content: center; transition: transform 0.3s, box-shadow 0.3s; user-select: none; text-align: center; }
  .module-card:hover { transform: translateY(-8px); box-shadow: var(--shadow-lg); }
  .module-card.module1 { background-color: var(--color-module1); }
  .module-card.module2 { background-color: var(--color-module2); }
  .module-card.module3 { background-color: var(--color-module3); }

  /* Full-Screen Video Overlays */
  #module-video-page, #demos-section.active {
      display: none; /* Hide by default */
  }
  #module-video-page.active, #demos-section.active {
      display: flex; /* Show when active */
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: var(--dark-bg);
      z-index: 1000;
      padding: 30px;
  }
  #module-video-page .video-container { max-width: 900px; width:100%; background: rgba(0,0,0,0.7); border-radius: 15px; padding: 20px; }
  #module-video-page video,
  #module-video-page .video-placeholder,
  #demos-section .video-placeholder {
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
  #demos-section .video-placeholder { height: 100%; border-radius: 0; }
  #module-video-page .back-btn { position: absolute; top: 30px; left: 30px; background: rgba(0,0,0,0.6); border: none; color: white; padding: 10px 15px; border-radius: 8px; cursor: pointer; font-weight: 600; transition: background 0.3s; }
  #module-video-page .back-btn:hover { background: rgba(0,0,0,0.9); }

  /* Reports Section */
  #reports-section { max-width: 900px; }
  #reports-section .report-controls { display: flex; justify-content: space-between; margin-bottom: 20px; flex-wrap: wrap; gap: 10px; }
  #reports-section select { padding: 8px 12px; border-radius: 8px; border: 1px solid var(--border); font-size: 1rem; }
  #reports-section button { background: var(--primary); color: white; border: none; padding: 10px 18px; border-radius: 8px; cursor: pointer; font-weight: 600; transition: background 0.3s; }
  #reports-section button:hover { background: var(--primary-dark); }

  /* Settings Section */
  #settings-section { max-width: 700px; }
  #settings-section h3 { margin-top: 25px; margin-bottom: 15px; }
  #settings-section label { display: block; margin-bottom: 6px; font-weight: 600; }
  #settings-section input, #settings-section textarea, #settings-section select { width: 100%; padding: 12px 15px; margin-bottom: 20px; border-radius: 10px; border: 1px solid var(--border); font-size: 1rem; }
  #settings-section input:focus, #settings-section textarea:focus, #settings-section select:focus { outline: none; border-color: var(--primary); box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.2); }
  #settings-section button { background: var(--primary); color: white; border: none; padding: 12px 20px; border-radius: 10px; cursor: pointer; font-weight: 600; transition: background 0.3s; }
  #settings-section button:hover { background: var(--primary-dark); }
  #settings-section .toggle-switch { display: flex; align-items: center; gap: 10px; margin-bottom: 20px; }
  #settings-section .toggle-switch input[type="checkbox"] { width: 40px; height: 20px; position: relative; appearance: none; background: var(--border); outline: none; border-radius: 20px; transition: background 0.3s; cursor: pointer; }
  #settings-section .toggle-switch input[type="checkbox"]:checked { background: var(--primary); }
  #settings-section .toggle-switch input[type="checkbox"]::before { content: ""; position: absolute; width: 18px; height: 18px; border-radius: 50%; top: 1px; left: 1px; background: white; transition: 0.3s; }
  #settings-section .toggle-switch input[type="checkbox"]:checked::before { left: 21px; }

  /* Responsive */
  @media (max-width: 992px) {
    .dashboard-container { flex-direction: column; }
    .sidebar { width: 100%; height: auto; border-right: none; border-bottom: 1px solid var(--border); }
    .dashboard-content { height: auto; }
  }
  @media (max-width: 768px) {
    .stats-grid, .content-grid { grid-template-columns: 1fr; }
    .login-container { padding: 30px 20px; }
  }
</style>
</head>
<body>
  <div id="login-screen">
    <div class="login-container">
      <div class="login-logo">
        <h1>ImmersiLearn VR</h1>
        <p>Transforming Learning for Children with ASD &amp; ID</p>
      </div>
      <div class="user-type-selector">
        <div class="user-type active" data-type="user"><i class="fas fa-user"></i> User</div>
        <div class="user-type" data-type="supervisor"><i class="fas fa-user-shield"></i> Supervisor</div>
      </div>
      <div class="login-form">
        <div class="input-group"><label for="email">Email Address</label><input type="email" id="email" placeholder="name@example.com" /></div>
        <div class="input-group"><label for="password">Password</label><input type="password" id="password" placeholder="Enter your password" /></div>
        <button class="btn btn-primary" id="login-btn">Login to Dashboard</button>
      </div>
      <div class="login-extra"><a href="#" id="forgot-password-link">Forgot Password?</a> | <a href="#" id="sign-up-link">Sign Up</a></div>
    </div>
  </div>

  <div id="signup-screen" style="display:none;">
    <div class="login-container">
      <div class="login-logo"><h1>Sign Up</h1><p>Create a new account</p></div>
      <div class="login-form">
        <div class="input-group"><label for="signup-name">Full Name</label><input type="text" id="signup-name" placeholder="Your full name" /></div>
        <div class="input-group"><label for="signup-email">Email Address</label><input type="email" id="signup-email" placeholder="name@example.com" /></div>
        <div class="input-group"><label for="signup-password">Password</label><input type="password" id="signup-password" placeholder="Create a password" /></div>
        <div class="input-group">
          <label for="signup-type">Account Type</label>
          <select id="signup-type">
            <option value="user">User</option>
            <option value="supervisor">Supervisor</option>
          </select>
        </div>
        <button class="btn btn-primary" id="signup-btn">Create Account</button>
      </div>
      <div class="login-extra" style="margin-top: 10px;"><a href="#" id="back-to-login-link">Back to Login</a></div>
    </div>
  </div>

  <div id="forgot-password-screen" style="display:none;">
    <div class="login-container">
      <div class="login-logo"><h1>Forgot Password</h1><p>Enter your email to reset password</p></div>
      <div class="login-form">
        <div class="input-group"><label for="forgot-email">Email Address</label><input type="email" id="forgot-email" placeholder="name@example.com" /></div>
        <button class="btn btn-primary" id="reset-password-btn">Reset Password</button>
      </div>
      <div class="login-extra" style="margin-top: 10px;"><a href="#" id="back-to-login-link2">Back to Login</a></div>
    </div>
  </div>

  <div id="main-dashboard">
    <div class="dashboard-header">
      <div class="header-logo"><h2>ImmersiLearn VR Dashboard</h2></div>
      <div class="user-profile">
        <div class="user-avatar" id="user-avatar">JD</div>
        <div class="user-info">
          <div class="user-name" id="user-name">Dr. Jane Doe</div>
          <div class="user-role" id="user-role">User</div>
        </div>
      </div>
    </div>

    <div class="dashboard-container">
      <div class="sidebar" id="sidebar">
        <a href="#" class="nav-item active" data-section="overview"><i class="fas fa-home"></i> Overview</a>
        <a href="#" class="nav-item" data-section="patients" id="nav-patients"><i class="fas fa-users"></i> Patients</a>
        <a href="#" class="nav-item" data-section="progress"><i class="fas fa-chart-line"></i> Progress Tracking</a>
        <a href="#" class="nav-item" data-section="modules"><i class="fas fa-cube"></i> Learning Modules</a>
        <a href="#" class="nav-item" data-section="demos" id="nav-demos"><i class="fas fa-video"></i> Demo Videos</a>
        <a href="#" class="nav-item" data-section="reports"><i class="fas fa-file-alt"></i> Reports</a>
        <a href="#" class="nav-item" data-section="settings"><i class="fas fa-cog"></i> Settings</a>
        <a href="#" class="nav-item" id="logout-btn"><i class="fas fa-sign-out-alt"></i> Logout</a>
      </div>

      <div class="dashboard-content">
        <div class="dashboard-section active" id="overview-section">
          <h2>Dashboard Overview</h2>
          <div class="stats-grid">
            <div class="stat-card"><div class="stat-icon blue"><i class="fas fa-users"></i></div><div class="stat-value" id="stat-active-patients">24</div><div class="stat-label">Active Patients</div></div>
            <div class="stat-card"><div class="stat-icon green"><i class="fas fa-check-circle"></i></div><div class="stat-value" id="stat-completion-rate">83%</div><div class="stat-label">Average Completion Rate</div></div>
            <div class="stat-card"><div class="stat-icon orange"><i class="fas fa-clock"></i></div><div class="stat-value" id="stat-avg-session-time">7.5</div><div class="stat-label">Avg. Session Time (mins)</div></div>
          </div>
          <div class="content-grid">
            <div class="content-card"><h3>Recent Activity</h3><div class="progress-list" id="recent-activity-list"></div></div>
            <div class="content-card"><h3>Latest Demo Video</h3><p>Morning Routine Module - v2.3 updated with improved interaction feedback</p></div>
          </div>
        </div>
        <div class="dashboard-section" id="patients-section"><h2>Patient Management</h2><table id="patients-table" aria-label="Patient Management Table"><thead><tr><th>Name</th><th>Age</th><th>Diagnosis</th><th>Last Session</th><th>Status</th></tr></thead><tbody></tbody></table></div>
        <div class="dashboard-section" id="progress-section"><h2>Progress Tracking</h2><p>Comparison of user progress over the last 7 sessions:</p><div id="progress-comparison"></div></div>
        <div class="dashboard-section" id="modules-section">
            <h2>Learning Modules</h2>
            <div class="modules-list" id="modules-list">
                <div class="module-card module1" data-module="Module 1">Module 1</div>
                <div class="module-card module2" data-module="Module 2">Module 2</div>
                <div class="module-card module3" data-module="Module 3">Module 3</div>
            </div>
        </div>
        <div class="dashboard-section" id="demos-section">
            <div class="video-placeholder">Demo video will cover the whole screen here</div>
        </div>
        <div class="dashboard-section" id="reports-section"><h2>Reports</h2><div class="report-controls"><label for="sort-reports">Sort by:</label><select id="sort-reports"><option value="date-desc">Date (Newest First)</option><option value="date-asc">Date (Oldest First)</option><option value="name-asc">Name (A-Z)</option><option value="name-desc">Name (Z-A)</option></select><button id="download-report-btn">Download Report</button></div><table id="reports-table" aria-label="Reports Table"><thead><tr><th>Patient Name</th><th>Report Date</th><th>Summary</th></tr></thead><tbody></tbody></table></div>
        <div class="dashboard-section" id="settings-section">
            <h2>Settings</h2>
            <h3>Edit Profile</h3><label for="profile-name">Name</label><input type="text" id="profile-name" /><label for="profile-email">Email</label><input type="email" id="profile-email" /><button id="save-profile-btn">Save Profile</button>
            <h3>Change Password</h3><label for="current-password">Current Password</label><input type="password" id="current-password" /><label for="new-password">New Password</label><input type="password" id="new-password" /><label for="confirm-password">Confirm New Password</label><input type="password" id="confirm-password" /><button id="change-password-btn">Change Password</button>
            <h3>Contact Us</h3><p>Phone: +91 9115207977</p><p>Email: dratexinclusion@gmail.com</p>
            <h3>Dark Mode</h3><div class="toggle-switch"><input type="checkbox" id="dark-mode-toggle" /><label for="dark-mode-toggle">Enable Dark Mode</label></div>
            <h3>Report an Issue</h3><label for="issue-select">Select a problem:</label><select id="issue-select"><option value="">-- Select an issue --</option><option value="navigation">Navigation issues</option><option value="login">Login issues</option><option value="video">Video playback problems</option><option value="other">Other</option></select><label for="issue-description">Describe your issue:</label><textarea id="issue-description" rows="4" placeholder="Provide more details here..."></textarea><button id="submit-issue-btn">Submit Issue</button><div id="issue-feedback" style="margin-top:10px; font-weight:600;"></div>
        </div>
      </div>
    </div>
  </div>

    <div id="module-video-page">
      <button class="back-btn" id="module-back-btn"><i class="fas fa-arrow-left"></i> Back</button>
      <div class="video-container">
        <div class="video-placeholder" id="module-video-placeholder">Video will be uploaded here later</div>
      </div>
    </div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  // Simulated Data
  const patientsData = [
    { name: "Michael Smith", age: 8, diagnosis: "ASD", lastSession: "2025-09-16", status: "Active" },
    { name: "Sarah Johnson", age: 10, diagnosis: "ID", lastSession: "2025-09-15", status: "Active" },
    { name: "Alex Lee", age: 7, diagnosis: "ASD", lastSession: "2025-09-14", status: "In Progress" },
    { name: "Emily Davis", age: 9, diagnosis: "ID", lastSession: "2025-09-12", status: "Active" },
  ];
  const reportsData = patientsData.map(p => ({
    name: p.name,
    date: new Date(p.lastSession),
    summary: `Report summary for ${p.name} with diagnosis ${p.diagnosis}.`
  }));
  const recentActivityData = [
      { name: 'Michael', task: 'Morning Routine', date: 'Today, 10:24 AM', value: '92%' },
      { name: 'Sarah', task: 'Social Greetings', date: 'Yesterday, 3:45 PM', value: '78%' },
      { name: 'Alex', task: 'Emotional Regulation', date: 'Sept 14, 9:15 AM', value: 'In Progress' }
  ];

  let currentUser = {};

  // DOM Elements
  const loginScreen = document.getElementById('login-screen');
  const signupScreen = document.getElementById('signup-screen');
  const forgotPasswordScreen = document.getElementById('forgot-password-screen');
  const mainDashboard = document.getElementById('main-dashboard');
  const navItems = document.querySelectorAll('.nav-item');
  const sections = document.querySelectorAll('.dashboard-section');
  const moduleVideoPage = document.getElementById('module-video-page');

  // --- UI Population Functions ---
  function populateRecentActivity() {
      const list = document.getElementById('recent-activity-list');
      list.innerHTML = recentActivityData.map(item => `
        <div class="progress-item">
          <div class="progress-info">
            <div class="progress-name">${item.name} completed ${item.task}</div>
            <div class="progress-date">${item.date}</div>
          </div>
          <div class="progress-value">${item.value}</div>
        </div>`).join('');
  }

  function populatePatients() {
    const tbody = document.querySelector("#patients-table tbody");
    tbody.innerHTML = patientsData.map(p => `
      <tr>
        <td>${p.name}</td><td>${p.age}</td><td>${p.diagnosis}</td>
        <td>${p.lastSession}</td><td>${p.status}</td>
      </tr>`).join('');
  }

  function populateReports(sortBy = "date-desc") {
    const tbody = document.querySelector("#reports-table tbody");
    let sortedReports = [...reportsData];
    const compare = (a, b, key, asc = true) => {
        const valA = a[key], valB = b[key];
        if (valA < valB) return asc ? -1 : 1;
        if (valA > valB) return asc ? 1 : -1;
        return 0;
    };
    if (sortBy === 'date-desc') sortedReports.sort((a,b) => b.date - a.date);
    else if (sortBy === 'date-asc') sortedReports.sort((a,b) => a.date - b.date);
    else if (sortBy === 'name-asc') sortedReports.sort((a,b) => a.name.localeCompare(b.name));
    else if (sortBy === 'name-desc') sortedReports.sort((a,b) => b.name.localeCompare(a.name));

    tbody.innerHTML = sortedReports.map(r => `
      <tr>
        <td>${r.name}</td><td>${r.date.toLocaleDateString()}</td><td>${r.summary}</td>
      </tr>`).join('');
  }

  function generateProgressTracking() {
    const container = document.getElementById("progress-comparison");
    container.innerHTML = "";
    patientsData.forEach(p => {
      const days = 7;
      const pastData = Array.from({length: days}, () => Math.floor(Math.random() * 50) + 30);
      const presentData = pastData.map(val => Math.min(100, val + Math.floor(Math.random() * 30) - 5));
      const svgWidth = 300, svgHeight = 150, padding = 30;
      const scaleY = val => svgHeight - padding - (val / 100) * (svgHeight - 2 * padding);
      const scaleX = i => padding + (i * (svgWidth - 2 * padding)) / (days - 1);
      const createPoints = data => data.map((val, i) => `${scaleX(i)},${scaleY(val)}`).join(" ");

      const wrapper = document.createElement("div");
      wrapper.className = "progress-graph-wrapper";
      wrapper.innerHTML = `
        <div class="progress-graph-label">${p.name} (${p.diagnosis})</div>
        <div class="progress-graph-legend">
          <div><span style="display:inline-block;width:15px;height:15px;background:var(--accent);margin-right:6px;vertical-align:middle;"></span>Past</div>
          <div><span style="display:inline-block;width:15px;height:15px;background:var(--success);margin-right:6px;vertical-align:middle;"></span>Present</div>
        </div>
        <svg width="${svgWidth}" height="${svgHeight}" class="progress-graph-svg" xmlns="http://www.w3.org/2000/svg">
          <line class="axis-line" x1="${padding}" y1="${svgHeight-padding}" x2="${svgWidth-padding}" y2="${svgHeight-padding}"></line>
          <line class="axis-line" x1="${padding}" y1="${padding}" x2="${padding}" y2="${svgHeight - padding}"></line>
          <polyline class="past-line" points="${createPoints(pastData)}"></polyline>
          <polyline class="present-line" points="${createPoints(presentData)}"></polyline>
        </svg>
      `;
      container.appendChild(wrapper);
    });
  }

  // --- UI Update Functions ---
  function updateNavForRole(role) {
    const patientsNav = document.getElementById("nav-patients");
    patientsNav.style.display = (role === "supervisor") ? "flex" : "none";
  }

  function showScreen(screen) {
    [loginScreen, signupScreen, forgotPasswordScreen, mainDashboard].forEach(s => s.style.display = 'none');
    screen.style.display = 'flex';
    if(screen === mainDashboard) mainDashboard.style.display = 'block';
    if(screen === loginScreen) loginScreen.style.display = 'flex';
  }

  function showSection(sectionId) {
    sections.forEach(s => s.classList.remove('active'));
    moduleVideoPage.classList.remove('active');

    const targetSection = document.getElementById(sectionId + '-section');
    if (targetSection) targetSection.classList.add('active');
  }

  function initProfileFields() {
    document.getElementById('profile-name').value = currentUser.name;
    document.getElementById('profile-email').value = currentUser.email;
  }

  // --- Event Listeners ---
  // Login & Screen Navigation
  document.getElementById('login-btn').addEventListener('click', () => {
    const selectedType = document.querySelector('.user-type.active').getAttribute('data-type');
    currentUser = {
      role: selectedType,
      name: selectedType === 'user' ? 'John Doe' : 'Dr. Jane Doe',
      email: selectedType === 'user' ? 'john.doe@example.com' : 'dr.jane.doe@example.com',
      get initials() { return this.name.split(' ').map(n => n[0]).join('').toUpperCase(); }
    };
    
    document.getElementById('user-name').textContent = currentUser.name;
    document.getElementById('user-role').textContent = currentUser.role.charAt(0).toUpperCase() + currentUser.role.slice(1);
    document.getElementById('user-avatar').textContent = currentUser.initials;

    updateNavForRole(currentUser.role);
    populateRecentActivity();
    populatePatients();
    populateReports();
    generateProgressTracking();
    initProfileFields();
    
    showScreen(mainDashboard);
    showSection('overview');
    document.querySelector('.nav-item.active').classList.remove('active');
    document.querySelector('.nav-item[data-section="overview"]').classList.add('active');
  });

  document.getElementById('logout-btn').addEventListener('click', e => {
    e.preventDefault();
    showScreen(loginScreen);
    document.getElementById('email').value = '';
    document.getElementById('password').value = '';
  });

  document.querySelectorAll('.user-type').forEach(type => {
    type.addEventListener('click', () => {
      document.querySelector('.user-type.active').classList.remove('active');
      type.classList.add('active');
    });
  });

  // Auth screen toggles
  document.getElementById('sign-up-link').addEventListener('click', e => { e.preventDefault(); showScreen(signupScreen); });
  document.getElementById('forgot-password-link').addEventListener('click', e => { e.preventDefault(); showScreen(forgotPasswordScreen); });
  document.getElementById('back-to-login-link').addEventListener('click', e => { e.preventDefault(); showScreen(loginScreen); });
  document.getElementById('back-to-login-link2').addEventListener('click', e => { e.preventDefault(); showScreen(loginScreen); });
  document.getElementById('signup-btn').addEventListener('click', () => { alert('Account created successfully! Please login.'); showScreen(loginScreen); });
  document.getElementById('reset-password-btn').addEventListener('click', () => { alert('Password reset link sent to your email.'); showScreen(loginScreen); });

  // Dashboard Navigation
  navItems.forEach(item => {
    item.addEventListener('click', e => {
      e.preventDefault();
      if (item.id === 'logout-btn') return;
      
      const targetSection = item.getAttribute('data-section');
      if (!targetSection) return;

      document.querySelector('.nav-item.active').classList.remove('active');
      item.classList.add('active');
      showSection(targetSection);
    });
  });

  // Module Navigation
  document.querySelectorAll('.module-card').forEach(card => {
    card.addEventListener('click', () => {
      const moduleName = card.getAttribute('data-module');
      document.getElementById('module-video-placeholder').textContent = `${moduleName} video will be uploaded here later`;
      moduleVideoPage.classList.add('active');
    });
  });

  document.getElementById('module-back-btn').addEventListener('click', () => {
    moduleVideoPage.classList.remove('active');
  });

  // Reports Page
  document.getElementById('sort-reports').addEventListener('change', e => populateReports(e.target.value));
  document.getElementById('download-report-btn').addEventListener('click', () => {
    let content = 'ImmersiLearn VR - Patient Reports\n\n';
    reportsData.forEach(r => {
      content += `Name: ${r.name}\nDate: ${r.date.toLocaleDateString()}\nSummary: ${r.summary}\n\n`;
    });
    const blob = new Blob([content], { type: 'text/plain' });
    const link = document.createElement('a');
    link.href = URL.createObjectURL(blob);
    link.download = 'patient_reports.txt';
    link.click();
    URL.revokeObjectURL(link.href);
  });

  // Settings Page
  document.getElementById('save-profile-btn').addEventListener('click', () => {
    const newName = document.getElementById('profile-name').value.trim();
    if(newName) {
      currentUser.name = newName;
      document.getElementById('user-name').textContent = currentUser.name;
      document.getElementById('user-avatar').textContent = currentUser.initials;
      alert('Profile updated successfully!');
    } else {
      alert('Name cannot be empty.');
    }
  });

  document.getElementById('change-password-btn').addEventListener('click', () => alert('Password changed successfully! (Simulated)'));
  
  document.getElementById('dark-mode-toggle').addEventListener('change', (e) => {
    document.body.classList.toggle('dark-mode', e.target.checked);
  });
  
  document.getElementById('submit-issue-btn').addEventListener('click', () => {
    const feedback = document.getElementById('issue-feedback');
    feedback.style.color = 'green';
    feedback.textContent = 'Thank you for reporting the issue. We will look into it.';
    setTimeout(() => feedback.textContent = '', 3000);
  });
});
</script>
</body>
</html>
