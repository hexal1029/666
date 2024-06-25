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
    <title>Random Deer Image</title>
</head>
<body>
    <h1>Random Deer Image</h1>
    <button id="fetchDeerButton">Fetch a Deer Image</button>
    <br><br>
    <img id="deerImage" src="" alt="Random Deer" width="300">
    
    <script>
        document.getElementById('fetchDeerButton').addEventListener('click', function() {
            fetch('https://deer.ceo/api/breeds/image/random')
                .then(response => response.json())
                .then(data => {
                    document.getElementById('deerImage').src = data.message;
                })
                .catch(error => console.error('Error fetching deer image:', error));
        });
    </script>
</body>
</html>
