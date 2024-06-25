---
title: Home
layout: home
---

# Houlin Website
## Someone 

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Dog Image</title>
</head>
<body>
    <h1>Random Dog Image</h1>
    <button id="fetchDogButton">Fetch a Dog Image</button>
    <br><br>
    <img id="dogImage" src="" alt="Random Dog" width="300">
    
    <script>
        document.getElementById('fetchDogButton').addEventListener('click', function() {
            fetch('https://dog.ceo/api/breeds/image/random')
                .then(response => response.json())
                .then(data => {
                    document.getElementById('dogImage').src = data.message;
                })
                .catch(error => console.error('Error fetching dog image:', error));
        });
    </script>
</body>
</html>
