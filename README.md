<!DOCTYPE html>
<html>
<head>
  <title>Skill Showcase</title>
  <style>
    .box {
      width: 200px;
      height: 200px;
      background-size: cover;
      background-position: center;
      display: inline-block;
      margin: 10px;
      cursor: pointer;
      position: relative;
    }
    .box-text {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: rgba(0, 0, 0, 0.5);
      color: white;
      text-align: center;
      padding: 5px;
    }
    video {
      width: 100%;
      height: 100%;
    }
    .clear-button {
      width: 200px;
      height: 50px;
      background-color: #007bff;
      color: white;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="box" style="background-image: url('graphic_design.jpg');" onclick="playVideo('graphic_design.mp4')"> 
    <div class="box-text">Graphic Design</div>
  </div>
  <div class="box" style="background-image: url('skateboarding.jpg');" onclick="playVideo('skateboarding.mp4')"> 
    <div class="box-text">Skateboarding</div>
  </div>
  <div class="box" style="background-image: url('kendama.jpg');" onclick="playVideo('kendama.mp4')"> 
    <div class="box-text">Kendama</div>
  </div>

  <div id="video-container"></div>

  <button class="clear-button" onclick="clearVideo()">Clear</button>

  <script>
    function playVideo(videoFileName) {
      const videoContainer = document.getElementById('video-container');
      videoContainer.innerHTML = `
        <video controls autoplay>
          <source src="${videoFileName}" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      `;
    }

    function clearVideo() {
      const videoContainer = document.getElementById('video-container');
      videoContainer.innerHTML = ''; // Clear the video container
    }
  </script>
</body>
</html>
