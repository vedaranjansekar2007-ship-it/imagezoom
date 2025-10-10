# Ex04 Places Around Me
## Date: 10-10-2025

## AIM
To develop a website to display details about the places around my house.

## DESIGN STEPS

### STEP 1
Create a Django admin interface.

### STEP 2
Download your city map from Google.

### STEP 3
Using ```<map>``` tag name the map.

### STEP 4
Create clickable regions in the image using ```<area>``` tag.

### STEP 5
Write HTML programs for all the regions identified.

### STEP 6
Execute the programs and publish them.

## CODE
gallery.html
```
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Image Gallery</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="gallery">
    <img src="a2.jpg" id="image1" alt="Person 2">
    <img src="a3.jpg" id="image2" alt="Person 3">
    <img src="a4.jpg" id="image3" alt="Person 4">
    <img src="a5.jpg" id="image4" alt="Person 5">
  </div>

  <footer>
    <h1>&copy; DESIGNED BY:</h1>
    <h2> NKK</h2>
  </footer>

  <script src="script.js"></script>
</body>
</html>
```
script.js
```
const images = document.querySelectorAll('.gallery img');

images.forEach(image => {
  image.addEventListener('mouseover', () => {
    image.style.transform = 'scale(1.2) rotate(2deg)';
    image.style.boxShadow = '0 20px 40px rgba(0,0,0,0.6)';
  });

  image.addEventListener('mouseout', () => {
    image.style.transform = 'scale(1) rotate(0deg)';
    image.style.boxShadow = '';
  });
});
```
style.css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: linear-gradient(180deg, rgba(255, 0, 0, 0.6), #8e906f, #384043, #50565f);
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  color: white;
  text-align: center;
  padding: 40px 0;
}

.gallery {
  display: flex;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
  margin-top: 100px;
}

.gallery img {
  width: 200px;
  height: 250px;
  border: 8px solid rgb(255, 0, 0);
  border-radius: 10px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

footer {
  margin-top: 80px;
}

h1 {
  font-size: 25px;
}

h2 {
  font-size: 22px;
  color: #fff;
}
```
## OUTPUT
![Uploading Screenshot 2025-10-10 165658.png…]()






## RESULT
The program for implementing image maps using HTML is executed successfully.
