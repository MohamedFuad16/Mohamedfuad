# Mohamedfuad
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Search Japanese Words</title>
</head>
<body>
  <input type="text" id="searchInput" placeholder="Enter search query">
  <ul id="wordList">
    <li>日本語 - Japanese</li>
    <li>こんにちは - Hello</li>
    <li>ありがとう - Thank you</li>
    <!-- Add more list items here -->
  </ul>

  <script>
    document.getElementById('searchInput').addEventListener('input', function(e) {
      const query = e.target.value.toLowerCase();
      const wordList = document.getElementById('wordList');
      const words = wordList.getElementsByTagName('li');

      Array.from(words).forEach(word => {
        const text = word.textContent.toLowerCase();
        if (text.includes(query)) {
          word.style.display = 'block';
        } else {
          word.style.display = 'none';
        }
      });
    });
  </script>
</body>
</html>
