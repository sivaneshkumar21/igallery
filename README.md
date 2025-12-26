# Ex.07 Design of Interactive Image Gallery
## Date:26-12-2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
```
gallery.html

<!DOCTYPE html>
<html>
<head>
  <title>Simple Image Gallery</title>
  <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>
  <h2> &#128247My Image Gallery</h2>

  <div class="gallery">
    <img src="{% static 'vj.1.jpg' %}" alt="Photo 1">
    <img src="{% static 'vj.2.jpg' %}" alt="Photo 2">
    <img src="{% static 'vj.3.jpeg' %}" alt="Photo 3">
    <img src="{% static 'vj.4.webp' %}" alt="Photo 4">
  </div>

  <div class="popup" id="popup">
    <span id="close">&times;</span>
    <img id="popupImg" src="">
  </div>
  <center>
    <h3>&copy;Image Gallery Designed by:</h3>
    <h2>SIVANESH KUMAR.N</h2>
  </center>

  <script src="{% static 'script.js' %}"></script>
</body>
</html>

style.css

body {
  background: #eee;
  font-family: Arial, sans-serif;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h2 {
  margin: 20px;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 15px;
  padding: 20px;
}

.gallery img {
  width: 200px;
  height: 250px;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.2s;
}

.gallery img:hover {
  transform: scale(1.05);
}


.popup {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: none;
  justify-content: center;
  align-items: center;
}

.popup img {
  width: 60%;
  max-width: 400px;
  border-radius: 12px;
  box-shadow: 0 0 20px #000;
}

.popup span {
  position: absolute;
  top: 20px;
  right: 40px;
  font-size: 30px;
  color: white;
  cursor: pointer;
  font-weight: bold;
}

script.js

const popup = document.getElementById('popup');
const popupImg = document.getElementById('popupImg');
const closeBtn = document.getElementById('close');

document.querySelectorAll('.gallery img').forEach(img => {
  img.addEventListener('click', () => {
    popup.style.display = 'flex';
    popupImg.src = img.src;
  });
});

closeBtn.addEventListener('click', () => {
  popup.style.display = 'none';
});

popup.addEventListener('click', e => {
  if (e.target === popup) popup.style.display = 'none';
});


```

## OUTPUT:
![alt text](<Screenshot (47).png>)
![alt text](<Screenshot (48).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
