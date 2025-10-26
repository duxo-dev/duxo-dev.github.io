<!doctype html>
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
      background:linear-gradient(180deg,var(--primary),#2a7ed6);
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
  </style>
</head>
<body>
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
          <div class="avatar">DU</div>
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
          <a href="#" target="_blank" rel="noopener">Twitter / X (add link)</a>
          <a href="#" target="_blank" rel="noopener">Discord (add link)</a>
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
        <!-- LEFT: content feed -->
        <div>
          <div class="card">
            <h3 style="margin-top:0">Featured</h3>
            <p class="meta">Put your series, pinned video, or a welcome message here.</p>
            <div style="height:14px"></div>

            <div class="video-widget">
              <strong>Most recent video</strong>
              <div class="meta">Widget below will attempt to show the most recent upload.</div>
              <div class="video-embed card" id="video-embed">
                <!-- iframe inserted by JavaScript -->
                <div style="display:flex;align-items:center;justify-content:center;height:100%;color:var(--muted);">
                  Loading video widget...
                </div>
              </div>

              <div style="font-size:13px;color:var(--muted);">
                If you want the site to automatically fetch the latest video, add a YouTube Data API key (see the comments in the HTML). Otherwise paste a video ID into the <code>data-video-id</code> attribute on the <code>#video-embed</code> div.
              </div>
            </div>
          </div>

          <div class="card" style="margin-top:var(--gap);">
            <h3 style="margin-top:0">About Duxo</h3>
            <p class="meta">Short channel description goes here. Replace this with your real bio, upload schedule, or recent announcements.</p>
          </div>
        </div>

        <!-- RIGHT: sidebar -->
        <div>
          <div class="card">
            <strong>Subscribe & social</strong>
            <p class="meta">Stay in touch — add your other social links here.</p>
            <div style="height:14px"></div>
            <!-- YouTube Subscribe Button (works without API) -->
            <div>
              <div id="yt-subscribe" data-channel="Duxo" data-layout="default" data-count="default"></div>
            </div>
          </div>

          <div class="card" style="margin-top:var(--gap);">
            <strong>Contact</strong>
            <p class="meta">Business inquiries: <a href="mailto:you@domain.com" style="color:var(--muted)">you@domain.com</a></p>
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
    /**********************************************************************
     * VIDEO WIDGET LOGIC
     *
     * Two modes:
     * 1) Automatic (recommended): set `YOUTUBE_API_KEY` below to a valid
     *    YouTube Data API v3 key. The script will:
     *      - resolve the channel handle @Duxo._.W to a channel ID (if needed)
     *      - request the latest video via "search" endpoint and embed it.
     *
     * 2) Manual fallback:
     *    - If you do NOT want to use the API, paste a video ID into the
     *      data-video-id attribute on the #video-embed div, like:
     *      <div id="video-embed" data-video-id="PASTE_VIDEO_ID_HERE">...</div>
     *
     * Notes:
     * - To get a YouTube Data API key: go to Google Cloud Console -> APIs & Services -> enable YouTube Data API v3 -> create credentials.
     * - If you don't set an API key and don't set a video ID, the widget will show a friendly link to your channel.
     **********************************************************************/

    // ---- CONFIGURE HERE ----
    const YOUTUBE_API_KEY = ""; // <-- put your YouTube Data API v3 key here (optional)
    const CHANNEL_HANDLE = "@Duxo._.W"; // the handle you gave
    const CHANNEL_URL = "https://www.youtube.com/@Duxo._.W";
    // ------------------------

    const embedContainer = document.getElementById('video-embed');

    // If user manually set a data-video-id attribute, prefer that.
    const manualVideoId = embedContainer.getAttribute('data-video-id');

    function setEmbedByVideoId(videoId, title){
      embedContainer.innerHTML = '';
      const iframe = document.createElement('iframe');
      iframe.width = "100%";
      iframe.height = "360";
      iframe.allow = "accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture";
      iframe.allowFullscreen = true;
      iframe.src = `https://www.youtube.com/embed/${videoId}?rel=0`;
      embedContainer.appendChild(iframe);

      const caption = document.createElement('div');
      caption.style.marginTop = "8px";
      caption.style.fontSize = "13px";
      caption.style.color = "var(--muted)";
      caption.textContent = title ? title : ("https://youtu.be/" + videoId);
      embedContainer.appendChild(caption);
    }

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

      const note = document.createElement('div');
      note.style.marginTop = "10px";
      note.style.fontSize = "13px";
      note.style.color = "var(--muted)";
      note.innerHTML = 'Automatic latest-video fetching requires a YouTube Data API key. Or paste a video ID into <code>data-video-id</code>.';
      embedContainer.appendChild(note);
    }

    // If the user provided a manual video id attribute, use it immediately
    if(manualVideoId){
      setEmbedByVideoId(manualVideoId, "Manually specified video");
    } else if(!YOUTUBE_API_KEY){
      // no API key and no manual video -> show fallback
      setChannelFallback();
    } else {
      // We have an API key: attempt to fetch latest video
      (async function(){
        try {
          // Step 1: Try to resolve handle to channelId via search by forUsername or channels.list?
          // We'll attempt channels.list by forUsername (handles are not necessarily a username)
          // So instead use the "search" endpoint to find the channel first by the handle string.

          // Search for the channel resource by the handle string (safe fallback)
          const handleQuery = encodeURIComponent(CHANNEL_HANDLE);
          // 1) Try search for channel by query
          let resp = await fetch(`https://www.googleapis.com/youtube/v3/search?part=snippet&type=channel&q=${handleQuery}&key=${YOUTUBE_API_KEY}`);
          if(!resp.ok) throw new Error('Channel search failed: ' + resp.status);
          const searchJson = await resp.json();
          if(searchJson.items && searchJson.items.length){
            const channelId = searchJson.items[0].snippet.channelId;
            // 2) Get the latest upload via search endpoint limited to 1 result
            const videosResp = await fetch(`https://www.googleapis.com/youtube/v3/search?part=snippet&channelId=${channelId}&order=date&maxResults=1&type=video&key=${YOUTUBE_API_KEY}`);
            if(!videosResp.ok) throw new Error('Video fetch failed: ' + videosResp.status);
            const videosJson = await videosResp.json();
            if(videosJson.items && videosJson.items.length){
              const vid = videosJson.items[0].id.videoId;
              const title = videosJson.items[0].snippet.title;
              setEmbedByVideoId(vid, title);
              return;
            } else {
              throw new Error('No videos found for channel.');
            }
          } else {
            // if channel not found by search, try channels.list with the handle directly (handles are new)
            const chResp = await fetch(`https://www.googleapis.com/youtube/v3/channels?part=id&forUsername=${encodeURIComponent(CHANNEL_HANDLE.replace(/^@/,''))}&key=${YOUTUBE_API_KEY}`);
            if(chResp.ok){
              const chJson = await chResp.json();
              if(chJson.items && chJson.items.length){
                const channelId = chJson.items[0].id;
                // fetch latest video same as above
                const videosResp2 = await fetch(`https://www.googleapis.com/youtube/v3/search?part=snippet&channelId=${channelId}&order=date&maxResults=1&type=video&key=${YOUTUBE_API_KEY}`);
                const videosJson2 = await videosResp2.json();
                if(videosJson2.items && videosJson2.items.length){
                  const vid = videosJson2.items[0].id.videoId;
                  const title = videosJson2.items[0].snippet.title;
                  setEmbedByVideoId(vid, title);
                  return;
                }
              }
            }
            // fallback
            throw new Error('Could not resolve channel by handle.');
          }
        } catch(err){
          console.warn("Automatic fetch error:", err);
          setChannelFallback();
        }
      })();
    }

    /**********************************************************************
     * OPTIONAL: Insert YouTube's official subscribe button script.
     * (This adds a small subscribe widget if you want it.)
     **********************************************************************/
    (function addYtSubscribe(){
      const s = document.createElement('script');
      s.src = "https://apis.google.com/js/platform.js";
      s.async = true;
      s.defer = true;
      document.body.appendChild(s);

      // Create a small subscribe button target
      const container = document.getElementById('yt-subscribe');
      // Use the channel handle or channel name; for better results, replace with channel ID if known.
      container.innerHTML = '<div class="g-ytsubscribe" data-channel="' + encodeURIComponent('Duxo') + '" data-layout="default" data-count="default"></div>';
      // The platform.js script will render this automatically when loaded.
    })();
  </script>
</body>
</html>
