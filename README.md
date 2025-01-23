<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awesome Blossom</title>
    <style>
        /* Add your existing styles here */
        body {
            font-family: 'Arial', sans-serif;
        }
        #cameraSection {
            display: none;
            margin: 20px 0;
            text-align: center;
        }
        video {
            border: 3px solid #ffc952;
            border-radius: 10px;
            max-width: 100%;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            background: #ff5181;
            color: #fff;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background: #ffc952;
        }
    </style>
</head>
<body>
    <header>
        <h1>Awesome Blossom</h1>
    </header>
    <div>
        <button id="accessCamera">Access Camera</button>
    </div>
    <div id="cameraSection">
        <video id="camera" autoplay></video>
        <br>
        <button id="stopCamera">Stop Camera</button>
    </div>

    <script>
        const accessCameraBtn = document.getElementById("accessCamera");
        const cameraSection = document.getElementById("cameraSection");
        const cameraVideo = document.getElementById("camera");
        const stopCameraBtn = document.getElementById("stopCamera");
        let stream;

        accessCameraBtn.addEventListener("click", () => {
            const password = prompt("Enter the password to access the camera:");
            if (password === "Awesomeblossom785") {
                navigator.mediaDevices.getUserMedia({ video: true })
                    .then((mediaStream) => {
                        stream = mediaStream;
                        cameraVideo.srcObject = stream;
                        cameraSection.style.display = "block";
                    })
                    .catch((error) => {
                        alert("Camera access denied or unavailable.");
                        console.error(error);
                    });
            } else {
                alert("Incorrect password!");
            }
        });

        stopCameraBtn.addEventListener("click", () => {
            if (stream) {
                const tracks = stream.getTracks();
                tracks.forEach(track => track.stop());
                cameraVideo.srcObject = null;
                cameraSection.style.display = "none";
            }
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awesome Blossom - Home</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #fffcf2, #fff2e5);
        }
        nav {
            background: #ff5181;
            padding: 1rem;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
            font-size: 1.2rem;
        }
        nav a:hover {
            color: #ffc952;
        }
        header, section {
            text-align: center;
            margin: 20px auto;
        }
        header h1 {
            color: #ff518
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awesome Blossom - About Us</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #fffcf2, #fff2e5);
        }
        nav {
            background: #ff5181;
            padding: 1rem;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
            font-size: 1.2rem;
        }
        nav a:hover {
            color: #ffc952;
        }
        header, section {
            text-align: center;
            margin: 20px auto;
        }
        header h1 {
            color: #ff5181;
            font-size: 2.5rem;
        }
    </style>
</head>
<body>
    <header>
        <h1>About Us</h1>
    </header>
    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About Us</a>
        <a href="
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awesome Blossom - Gallery</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to bottom, #fffcf2, #fff2e5);
        }
        nav {
            background: #ff5181;
            padding: 1rem;
            text-align: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
            font-size: 1.2rem;
        }
        nav a:hover {
            color: #ffc952;
        }
        header, section {
            text-align: center;
            margin: 20px auto;
        }
        header h1 {
            color: #ff5181;
            font-size: 2.5rem;
        }
        .gallery img {
            max-width: 200px;
            margin: 10px;
            border: 3px solid #ff518
