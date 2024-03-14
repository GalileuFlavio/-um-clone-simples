# -um-clone-simples
Projeto é um Clone básico da Página de Resultados de Pesquisa do Google.

|-- index.html
|-- styles.css
|-- script.js


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Search Clone</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="search-container">
        <input type="text" id="search-input" placeholder="Search...">
        <button onclick="search()">Search</button>
    </div>
    <div id="results-container">
        <!-- Search results will be displayed here -->
    </div>
    <script src="script.js"></script>
</body>
</html>

styles.css:

body {
    font-family: Arial, sans-serif;
}

.search-container {
    margin: 20px auto;
    text-align: center;
}

#results-container {
    margin: 20px auto;
    width: 80%;
}

.result {
    margin-bottom: 10px;
}

.result h3 {
    margin: 5px 0;
}

.result a {
    color: blue;
}

script.js:

function search() {
    const query = document.getElementById('search-input').value;
    // Simulated search results
    const results = [
        { title: 'Result 1', link: 'https://example.com/result1' },
        { title: 'Result 2', link: 'https://example.com/result2' },
        { title: 'Result 3', link: 'https://example.com/result3' },
    ];
    displayResults(results);
}

function displayResults(results) {
    const resultsContainer = document.getElementById('results-container');
    resultsContainer.innerHTML = '';
    results.forEach(result => {
        const resultDiv = document.createElement('div');
        resultDiv.classList.add('result');
        const titleElement = document.createElement('h3');
        const linkElement = document.createElement('a');
        linkElement.setAttribute('href', result.link);
        linkElement.textContent = result.title;
        titleElement.appendChild(linkElement);
        resultDiv.appendChild(titleElement);
        resultsContainer.appendChild(resultDiv);
    });
}
