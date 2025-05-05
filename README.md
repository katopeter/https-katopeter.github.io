index.html

<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Katopeter Utility</title>

    <link rel="stylesheet" href="styles.css">

</head>

<body>

    <h1>Katopeter Utility</h1>

    <div class="container">

        <form id="save-form">

            <label for="data">Data:</label>

            <textarea id="data" name="data"></textarea>

            <button id="save-btn">Save</button>

        </form>

        <button id="load-btn">Load</button>

        <div id="loaded-data"></div>

    </div>

    <script src="script.js"></script>

</body>

</html>



styles.css

body {

    font-family: Arial, sans-serif;

}



.container {

    max-width: 800px;

    margin: 40px auto;

    padding: 20px;

    background-color: #f9f9f9;

    border: 1px solid #ddd;

    border-radius: 10px;

    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);

}



#save-form {

    margin-bottom: 20px;

}



#data {

    width: 100%;

    height: 200px;

    padding: 10px;

    font-size: 16px;

}



#save-btn, #load-btn {

    background-color: #4CAF50;

    color: #fff;

    padding: 10px 20px;

    border: none;

    border-radius: 5px;

    cursor: pointer;

}



#save-btn:hover, #load-btn:hover {

    background-color: #3e8e41;

}



#loaded-data {

    margin-top: 20px;

    padding: 10px;

    background-color: #f0f0f0;

    border: 1px solid #ddd;

}



script.js

const saveForm = document.getElementById('save-form');

const saveBtn = document.getElementById('save-btn');

const loadBtn = document.getElementById('load-btn');

const loadedData = document.getElementById('loaded-data');



saveBtn.addEventListener('click', (e) => {

    e.preventDefault();

    const data = document.getElementById('data').value;

    localStorage.setItem('katopeter-data', data);

    alert('Data saved successfully!');

});



loadBtn.addEventListener('click', () => {

    const data = localStorage.getItem('katopeter-data');

    if (data) {

        loadedData.innerText = data;

    } else {

        alert('No data found!');

    }

});
<!--
**katopeter/katopeter** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
