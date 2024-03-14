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
