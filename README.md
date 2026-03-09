portfolio
 ├─ package.json
 ├─ pages/2
 ├─ components/
 ├─ public/yes
 └─ styles/

async function getGameStats() {
  const universeId = "1234567890"; // your game universe id

  const res = await fetch(`https://games.roblox.com/v1/games?universeIds=${universeId}`);
  const data = await res.json();

  const visits = data.data[0].visits;
  const playing = data.data[0].playing;

  document.getElementById("visits").innerText = visits.toLocaleString();
  document.getElementById("playing").innerText = playing;
}

getGameStats();
setInterval(getGameStats, 30000);
