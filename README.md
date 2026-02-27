<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Canada 51st State Application</title>
<style>
  body {
    font-family: 'Arial', sans-serif;
    background: linear-gradient(to right, #002868, #ffffff, #bf0a30);
    color: #000;
    text-align: center;
    padding: 2rem;
  }
  h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
  }
  h2 {
    font-size: 1.5rem;
    margin-bottom: 2rem;
  }
  .ballot button {
    background: #ffcc00;
    border: none;
    padding: 1rem 2rem;
    margin: 1rem;
    font-size: 1.2rem;
    cursor: pointer;
    border-radius: 12px;
    transition: transform 0.2s;
  }
  .ballot button:hover {
    transform: scale(1.1);
  }
  .map {
    margin-top: 2rem;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  .province {
    width: 120px;
    height: 120px;
    margin: 0.5rem;
    background: #e0e0e0;
    border-radius: 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    font-weight: bold;
    transition: 0.3s;
  }
  .province:hover {
    background: #ffcc00;
    transform: scale(1.1);
  }
  .countdown {
    font-size: 1.5rem;
    margin-top: 2rem;
    color: #fff;
    font-weight: bold;
  }
  .meme {
    margin-top: 2rem;
    max-width: 400px;
    border: 3px solid #000;
    border-radius: 12px;
  }
</style>
</head>
<body>

<h1>🇨🇦 Canada 51st State Application 🇺🇸</h1>
<h2>Scan, vote, and see where your province lands!</h2>

<div class="ballot">
  <button onclick="vote('California-style Tech Paradise')">California-style Tech Paradise</button>
  <button onclick="vote('Texas-style Freedom Forever')">Texas-style Freedom Forever</button>
  <button onclick="vote('Florida-style Chaos')">Florida-style Chaos</button>
</div>

<div class="map">
  <div class="province" onclick="joinState(this)">Ontario</div>
  <div class="province" onclick="joinState(this)">Quebec</div>
  <div class="province" onclick="joinState(this)">BC</div>
  <div class="province" onclick="joinState(this)">Alberta</div>
  <div class="province" onclick="joinState(this)">Manitoba</div>
  <div class="province" onclick="joinState(this)">Saskatchewan</div>
  <div class="province" onclick="joinState(this)">Nova Scotia</div>
  <div class="province" onclick="joinState(this)">Newfoundland</div>
  <div class="province" onclick="joinState(this)">New Brunswick</div>
  <div class="province" onclick="joinState(this)">PEI</div>
  <div class="province" onclick="joinState(this)">NWT</div>
  <div class="province" onclick="joinState(this)">Yukon</div>
  <div class="province" onclick="joinState(this)">Nunavut</div>
</div>

<div class="countdown" id="countdown">
  Time until admission: 3...2...1... (Just kidding 😏)
</div>

<img class="meme" src="https://i.imgur.com/q9hUu2A.gif" alt="Trump & Trudeau Meme">

<script>
function vote(choice) {
  alert("You voted for: " + choice + " 🎉 Canada is almost ready!");
}

function joinState(provinceDiv) {
  provinceDiv.style.background = "#00ff00";
  provinceDiv.innerText = provinceDiv.innerText + " ✅ Joined!";
}

let countdownEl = document.getElementById('countdown');
let fakeTime = 3;
setInterval(() => {
  if(fakeTime > 0) {
    countdownEl.innerText = "Time until admission: " + fakeTime + "...";
    fakeTime--;
  } else {
    countdownEl.innerText = "Canada is now the 51st state! (Just trolling 😏)";
  }
}, 1000);
</script>

</body>
</html>
