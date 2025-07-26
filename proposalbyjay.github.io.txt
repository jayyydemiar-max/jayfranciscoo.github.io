<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Will You Marry Me?</title>
  <style>
    body {
      font-family: "Segoe UI", sans-serif;
      background: #fff0f6;
      text-align: center;
      padding: 50px;
    }

    h1 {
      font-size: 2.5rem;
      color: #d63384;
    }

    .btn {
      margin: 20px 10px;
      padding: 15px 30px;
      font-size: 1.2rem;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }

    .yes {
      background-color: #28a745;
      color: white;
    }

    .yes:hover {
      background-color: #218838;
    }

    .no {
      background-color: #dc3545;
      color: white;
    }

    .no:hover {
      background-color: #c82333;
    }

    #memeContainer {
      margin-top: 30px;
    }

    video {
      width: 100%;
      max-width: 500px;
      margin-top: 20px;
    }

    #romanticMusic {
      display: none;
    }
  </style>
</head>
<body>

  <h1>I have a crush on you... 💕</h1>
  <h1>Can I marry you? 💍</h1>

  <button class="btn yes" onclick="sayYes()">Yes 💖</button>
  <button class="btn no" onclick="sayNo()">No 💔</button>

  <div id="response"></div>
  <div id="memeContainer"></div>

  <audio id="romanticMusic" src="your-romantic-music.mp3" autoplay loop></audio>

  <script>
    const memes = [
      "meme1.mp4", // replace with actual meme video links or files
      "meme2.mp4",
      "meme3.mp4",
      "meme4.mp4"
    ];

    let memeIndex = 0;

    function sayYes() {
      document.getElementById('response').innerHTML = `
        <h2>Yay!! 💍 I knew it!!! I love youuuu!!! 🥹</h2>
        <p>Let’s plan our wedding now 😭💒</p>
      `;
      document.getElementById('romanticMusic').style.display = "block";
      document.getElementById('romanticMusic').play();
    }

    function sayNo() {
      if (memeIndex < memes.length) {
        const video = document.createElement("video");
        video.src = memes[memeIndex];
        video.controls = true;
        document.getElementById("memeContainer").innerHTML = "";
        document.getElementById("memeContainer").appendChild(video);
        memeIndex++;
      } else {
        document.getElementById("memeContainer").innerHTML = `
          <h3>Okay... I get it. I’ll cry in the corner now 😭</h3>
        `;
      }
    }
  </script>

</body>
</html>
