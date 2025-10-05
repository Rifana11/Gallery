# Ex.08 Design of Interactive Image Gallery
# Date:05.10.25
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
photo.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Photo Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>My  Photo Gallery</h1>

    <div class="gallery">
        <img src="A.P.J.jpg" alt="Photo 1"  onclick="showImage(this)">
        <img src="Gandhiji.jpg" alt="Photo 2" onclick="showImage(this)">
        <img src="indra.jpg" alt="Photo 3" onclick="showImage(this)">
        <img src="nehru.jpg" alt="Photo 4" onclick="showImage(this)">
        <img src="rani.jpg" alt="Photo 5" onclick="showImage(this)">
    </div>

    <!-- Popup to show enlarged image -->
    <div id="popup" class="popup" onclick="closePopup()">
        <img id="popup-img" src="" alt="Enlarged Photo">
    </div>

    <script src="script.js"></script>
</body>
</html>

style.css

body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f2f2f2;
    margin: 0;
    padding: 0;
}

h1 {
    color: #333;
    margin-top: 20px;
}

.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
    margin: 30px;
}

.gallery img {
    width: 200px;
    height: 400px;
    object-fit: cover;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.3);
    transition: transform 0.3s;
    cursor: pointer;
}

.gallery img:hover {
    transform: scale(1.1);
}

.popup {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.8);
    justify-content: center;
    align-items: center;
}

.popup img {
    width: 60%;
    max-width: 700px;
    border-radius: 10px;
    box-shadow: 0 0 15px #fff;
}

script.js

function showImage(imgElement) {
    const popup = document.getElementById("popup");
    const popupImg = document.getElementById("popup-img");

    popupImg.src = imgElement.src;
    popup.style.display = "flex";
}

function closePopup() {
    document.getElementById("popup").style.display = "none";
}

```
# OUTPUT:
![alt text](<Screenshot 2025-10-05 132051.png>)
![alt text](<Screenshot 2025-10-05 132113.png>)
![alt text](<Screenshot 2025-10-05 132140.png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
