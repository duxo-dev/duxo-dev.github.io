# This is like my website or something idk

# SUBSCRIBER RACE
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>YouTube Live Leaderboard</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #0f0f0f;
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
      padding: 2rem;
    }
    .leaderboard {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      width: 400px;
    }
    .channel {
      display: flex;
      align-items: center;
      gap: 1rem;
      background: #181818;
      padding: 1rem;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(255,255,255,0.1);
    }
    .channel img {
      width: 64px;
      height: 64px;
      border-radius: 50%;
    }
    .channel-info {
      flex: 1;
    }
    .channel-info h2 {
      margin: 0;
      font-size: 1.2rem;
    }
    .channel-info p {
      margin: 0;
      color: #aaa;
    }
  </style>
</head>
<body>
  <h1>YouTube Subscriber Leaderboard</h1>
  <div class="leaderboard" id="leaderboard"></div>

  <script>
    const API_KEY = "AIzaSyBbV0i7Ma9SE1qiLfUqnzCESr1LM1Ny2Mk";
    const channels = [
      { id: "UCSI1_ltjUIvSxCbj4i8Svfw", name: "Duxo" },
      { id: "UCvc9Aun4GKXiHLWOlGhHzCg", name: "Alexory" },
      { id: "UCq-Fj5jknLsUf-MWSy4_brA", name: "MarioGames1" },
      { id: "UCq-Fj5jknLsUf-MWSy4_brA", name: "Cabbage838" },
      { id: "UCq-Fj5jknLsUf-MWSy4_brA", name: "ChickenGamer77" }
    ];

    async function fetchChannelData(channelId) {
      const url = `https://www.googleapis.com/youtube/v3/channels?part=snippet,statistics&id=${channelId}&key=${API_KEY}`;
      const res = await fetch(url);
      const data = await res.json();
      const item = data.items[0];
      return {
        name: item.snippet.title,
        pic: item.snippet.thumbnails.default.url,
        subs: parseInt(item.statistics.subscriberCount)
      };
    }

    async function updateLeaderboard() {
      const leaderboardDiv = document.getElementById("leaderboard");
      leaderboardDiv.innerHTML = "<p>Loading...</p>";

      const results = await Promise.all(channels.map(c => fetchChannelData(c.id)));
      results.sort((a, b) => b.subs - a.subs);

      leaderboardDiv.innerHTML = "";
      results.forEach((ch, i) => {
        leaderboardDiv.innerHTML += `
          <div class="channel">
            <img src="${ch.pic}" alt="${ch.name}" />
            <div class="channel-info">
              <h2>#${i + 1} ${ch.name}</h2>
              <p>${ch.subs.toLocaleString()} subscribers</p>
            </div>
          </div>
        `;
      });
    }

    updateLeaderboard();
    setInterval(updateLeaderboard, 60000); // refresh every 60 seconds
  </script>
</body>
</html>

