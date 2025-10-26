<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Duxo — Home</title>

  <!-- Colors: primary #3399ff, secondary #ff9933 -->
  <style>
    :root{
      --primary: #3399ff;
      --secondary: #ff9933;
      --bg: #0b1220;
      --card: rgba(255,255,255,0.04);
      --glass: rgba(255,255,255,0.03);
      --text: #e9f2ff;
      --muted: #cfe6ff66;
      --radius: 14px;
      --maxw: 1100px;
      --gap: 18px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    html,body{height:100%; margin:0; background: linear-gradient(180deg,var(--bg) 0%, #071426 100%); color:var(--text);}
    .wrap{
      max-width:var(--maxw);
      margin:36px auto;
      padding:28px;
      display:grid;
      grid-template-columns: 360px 1fr;
      gap:var(--gap);
    }

    /* header / left column */
    .brand {
      display:flex;
      gap:12px;
      align-items:center;
    }
    .logo {
      width:76px; height:76px;
      border-radius:18px;
      background: linear-gradient(135deg,var(--primary), var(--secondary));
      display:flex; align-items:center; justify-content:center;
      box-shadow: 0 6px 18px rgba(51,153,255,0.12), inset 0 -6px 12px rgba(255,153,51,0.06);
      font-weight:800; color:#fff; font-size:28px;
    }
    .title h1{ margin:0; font-size:20px; letter-spacing:0.4px; }
    .title p{ margin:4px 0 0 0; color:var(--muted); font-size:13px; }

    .card {
      background: linear-gradient(180deg, var(--card), rgba(255,255,255,0.01));
      padding:16px;
      border-radius:var(--radius);
      box-shadow: 0 8px 24px rgba(2,6,23,0.6);
      border: 1px solid rgba(255,255,255,0.03);
    }

    /* Left column */
    .left {
      display:flex; flex-direction:column; gap:var(--gap);
      position:sticky; top:28px;
      align-self:start;
    }
    .profile {
      display:flex; gap:12px; align-items:center;
    }
    .avatar {
      width:88px; height:88px; border-radius:12px;
      background-size: cover;
      background-position: center;
      background-image: url('https://yt3.googleusercontent.com/ytc/AIdro_m-1f6S0wL_ynNfq5zTfTyI2XH5ZrdoPCDWj5z6=s176-c-k-c0x00ffffff-no-rj');
      display:flex; align-items:center; justify-content:center; font-weight:700; color: #fff;
      font-size:32px;
    }
    .sub-btn {
      margin-top:10px;
      display:inline-flex; gap:8px; align-items:center;
      background: linear-gradient(90deg,var(--primary),#2bb0ff);
      color:white; padding:10px 14px; border-radius:10px; font-weight:700;
      text-decoration:none; border:0;
      box-shadow: 0 6px 14px rgba(51,153,255,0.18);
    }
    .link-list { display:flex; flex-direction:column; gap:8px; margin-top:4px;}
    .link-list a { color:var(--muted); text-decoration:none; font-size:14px; padding:8px; border-radius:8px; }
    .link-list a:hover { background:var(--glass); color:var(--text); }

    /* Main column */
    .main {
      display:flex; flex-direction:column; gap:var(--gap);
    }
    .hero {
      display:flex; gap:18px; align-items:center; justify-content:space-between;
    }
    .hero-left h2 { margin:0 0 6px 0; font-size:22px; }
    .hero-left p { margin:0; color:var(--muted); }

    .grid {
      display:grid;
      grid-template-columns: 1fr 420px;
      gap:var(--gap);
      align-items:start;
    }

    /* video widget */
    .video-widget {
      min-height:260px;
      display:flex; flex-direction:column; gap:12px;
    }
    .video-embed {
      border-radius:12px;
      overflow:hidden;
      background:#000;
      min-height:200px;
    }

    .meta { color:var(--muted); font-size:14px; }

    /* responsive */
    @media (max-width:980px){
      .wrap{ grid-template-columns: 1fr; padding:18px; }
      .grid { grid-template-columns: 1fr; }
      .left { position:static; }
    }

    /* footer */
    footer { text-align:center; color:var(--muted); margin:30px 0 8px 0; font-size:13px; }

    /* Notification bell */
    .notification {
      position: fixed;
      top: 22px;
      right: 22px;
      background: var(--secondary);
      color: white;
      width: 48px;
      height: 48px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 22px;
      cursor: pointer;
      box-shadow: 0 0 14px rgba(255,153,51,0.4);
      transition: all 0.25s ease;
      z-index: 999;
    }

    .notification:hover {
      transform: scale(1.1);
      box-shadow: 0 0 18px rgba(255,153,51,0.6);
      background: linear-gradient(90deg,var(--secondary), #ff7a1a);
    }
  </style>
</head>
<body>
  <!-- Notification bell -->
  <div class="notification" id="notif-bell" title="Go to Subscriber Race!">🔔</div>

  <div class="wrap">
    <!-- LEFT -->
    <div class="left">
      <div class="card">
        <div class="brand">
          <div class="logo">D</div>
          <div class="title">
            <h1>Duxo</h1>
            <p>Channel homepage — welcome!</p>
          </div>
        </div>

        <hr style="border:none; height:12px; background:transparent">

        <div class="profile">
          <div class="avatar"></div>
          <div>
            <strong>Duxo</strong>
            <div style="color:var(--muted); font-size:13px; margin-top:6px;">Gaming • Uploads & streams</div>
            <a class="sub-btn" href="https://www.youtube.com/@Duxo._.W" target="_blank" rel="noopener noreferrer">
              ▶ Subscribe
            </a>
          </div>
        </div>

        <div style="margin-top:12px" class="link-list">
          <a href="https://www.youtube.com/@Duxo._.W" target="_blank" rel="noopener">YouTube Channel</a>
          <a href="https://discord.gg/ftqBjDv8NV" target="_blank" rel="noopener">Discord Server!</a>
        </div>
      </div>

      <div class="card" style="margin-top:var(--gap);">
        <strong>About</strong>
        <p class="meta" style="margin-top:8px;">Welcome to Duxo's channel homepage. Replace or edit content here to match your channel bio, socials, and schedule.</p>
      </div>
    </div>

    <!-- MAIN -->
    <div class="main">
      <div class="card hero">
        <div class="hero-left">
          <h2>Latest from Duxo</h2>
          <p class="meta">Newest uploads, latest stream snippets and highlights live here.</p>
        </div>
        <div style="display:flex; gap:10px; align-items:center;">
          <div style="padding:8px 12px; border-radius:10px; background:linear-gradient(90deg,var(--secondary), #ff7a1a); color:#fff; font-weight:700;">Live: Off</div>
        </div>
      </div>

      <div class="grid">
        <div>
          <div class="card">
            <h3 style="margin-top:0">Featured</h3>
            <p class="meta">Put your series, pinned video, or a welcome message here.</p>
            <div style="height:14px"></div>

            <div class="video-widget">
              <strong>Most recent video</strong>
              <div class="meta">Widget below will attempt to show the most recent upload.</div>
              <div class="video-embed card" id="video-embed">
                <div style="display:flex;align-items:center;justify-content:center;height:100%;color:var(--muted);">
                  Loading video widget...
                </div>
              </div>
            </div>
          </div>

          <div class="card" style="margin-top:var(--gap);">
            <h3 style="margin-top:0">About Me</h3>
            <p class="meta">I am just a silly guy, who loves to be silly.. did I mention I am silly?</p>
          </div>
        </div>

        <div>
          <div class="card" style="margin-top:var(--gap);">
            <strong>Contact</strong>
            <p class="meta">Business inquiries: <a href="mailto:duxos101@gmail.com" style="color:var(--muted)">you@domain.com</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <footer>
    Made with ♥ by Duxo — theme colors: <span style="color:var(--primary)">#3399ff</span> &amp; <span style="color:var(--secondary)">#ff9933</span>
  </footer>

  <!-- SCRIPTS -->
  <script>
    // Notification bell click
    document.getElementById('notif-bell').addEventListener('click', () => {
      window.location.href = "subrace.html";
    });

    // Video embed logic (from before)
    const YOUTUBE_API_KEY = "";
    const CHANNEL_URL = "https://www.youtube.com/@Duxo._.W";
    const embedContainer = document.getElementById('video-embed');
    const manualVideoId = embedContainer.getAttribute('data-video-id');

    function setChannelFallback(){
      embedContainer.innerHTML = '';
      const link = document.createElement('a');
      link.href = CHANNEL_URL;
      link.target = "_blank";
      link.rel = "noopener noreferrer";
      link.style.display = "flex";
      link.style.alignItems = "center";
      link.style.justifyContent = "center";
      link.style.height = "200px";
      link.style.textDecoration = "none";
      link.style.color = "var(--muted)";
      link.style.fontSize = "15px";
      link.textContent = "Open Duxo's YouTube channel";
      embedContainer.appendChild(link);
    }

    setChannelFallback();
  </script>
</body>
</html>
