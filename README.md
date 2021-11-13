<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>WEBカメラ</title>
  <style>
      #video{
          height: 100vh;
      }
  </style>
</head>
<body>
    <video id="video"></video>
    <script>
        const video = document.getElementById("video")
        navigator.mediaDevices.getUserMedia({
            video: true,
            audio: false,
        }).then(stream => {
            video.srcObject = stream;
            video.play()
        }).catch(e => {
          console.log(e)
        })
    </script>  
</body>
</html>
