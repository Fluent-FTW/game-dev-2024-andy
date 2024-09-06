<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Webcam Feed</title>
</head>
<body>
    <h1>Webcam Feed</h1>
    <video id="webcam" autoplay playsinline></video>

    <script>
        const video = document.getElementById('webcam');

        // Request access to the webcam
        navigator.mediaDevices.getUserMedia({ video: true })
            .then(stream => {
                video.srcObject = stream;
            })
            .catch(error => {
                console.error('Error accessing webcam:', error);
            });
    </script>
</body>
</html>
