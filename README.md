# CodeAlpha-project-name
app about random quote generator
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Random Quote App</title>
  <style>
    body {
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background: #f9f9f9;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background: #fff;
      padding: 2rem;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      text-align: center;
      max-width: 500px;
      width: 90%;
    }

    .quote {
      font-size: 1.3rem;
      font-style: italic;
      color: #333;
      margin-bottom: 1rem;
    }

    .author {
      font-size: 1rem;
      font-weight: bold;
      color: #555;
      margin-bottom: 2rem;
    }

    button {
      background: #007bff;
      color: #fff;
      border: none;
      padding: 0.7rem 1.5rem;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1rem;
      transition: background 0.3s ease;
    }

    button:hover {
      background: #0056b3;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="quote" id="quote">Loading quote...</div>
    <div class="author" id="author"></div>
    <button onclick="newQuote()">New Quote</button>
  </div>

  <script>
    const quotes = [
      { text: "The best way to predict the future is to create it.", author: "Peter Drucker" },
      { text: "In the middle of every difficulty lies opportunity.", author: "Albert Einstein" },
      { text: "Success is not final, failure is not fatal: It is the courage to continue that counts.", author: "Winston Churchill" },
      { text: "Do what you can, with what you have, where you are.", author: "Theodore Roosevelt" },
      { text: "Happiness depends upon ourselves.", author: "Aristotle" }
    ];

    function newQuote() {
      let randomIndex = Math.floor(Math.random() * quotes.length);
      let quoteObj = quotes[randomIndex];
      document.getElementById("quote").textContent = `"${quoteObj.text}"`;
      document.getElementById("author").textContent = `— ${quoteObj.author}`;
    }

    // Show a random quote when app loads
    window.onload = newQuote;
  </script>

</body>
</html>
