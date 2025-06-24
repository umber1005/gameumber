<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tebak Sopan atau Tidak?</title>
  <style>
    body {
      font-family: sans-serif;
      background-color: #f0f8ff;
      padding: 20px;
      max-width: 600px;
      margin: auto;
    }
    .question {
      margin-bottom: 20px;
      padding: 15px;
      background-color: #ffffff;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    .result {
      font-weight: bold;
      margin-top: 10px;
    }
    button {
      margin: 5px;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    .sopan { background-color: #4caf50; color: white; }
    .tidak { background-color: #f44336; color: white; }
  </style>
</head>
<body>
  <h1>Tebak Sopan atau Tidak?</h1>

  <div class="question" id="q1">
    <p>1. Kamu bilang "terima kasih" setelah diberi kue.</p>
    <button class="sopan" onclick="jawab(1, true)">Sopan</button>
    <button class="tidak" onclick="jawab(1, false)">Tidak Sopan</button>
    <div class="result" id="r1"></div>
  </div>

  <div class="question" id="q2">
    <p>2. Kamu memotong pembicaraan guru saat sedang menjelaskan.</p>
    <button class="sopan" onclick="jawab(2, false)">Sopan</button>
    <button class="tidak" onclick="jawab(2, true)">Tidak Sopan</button>
    <div class="result" id="r2"></div>
  </div>

  <div class="question" id="q3">
    <p>3. Kamu bilang "tolong dong" saat minta bantuan teman.</p>
    <button class="sopan" onclick="jawab(3, true)">Sopan</button>
    <button class="tidak" onclick="jawab(3, false)">Tidak Sopan</button>
    <div class="result" id="r3"></div>
  </div>

  <div class="question" id="q4">
    <p>4. Kamu menyuruh teman dengan nada tinggi: "Cepat ambilkan pensilku!"</p>
    <button class="sopan" onclick="jawab(4, false)">Sopan</button>
    <button class="tidak" onclick="jawab(4, true)">Tidak Sopan</button>
    <div class="result" id="r4"></div>
  </div>

  <div class="question" id="q5">
    <p>5. Saat lewat di depan orang tua, kamu berkata "permisi".</p>
    <button class="sopan" onclick="jawab(5, true)">Sopan</button>
    <button class="tidak" onclick="jawab(5, false)">Tidak Sopan</button>
    <div class="result" id="r5"></div>
  </div>

  <script>
    function jawab(no, benar) {
      const r = document.getElementById("r" + no);
      if (benar) {
        r.textContent = "✅ Benar! Itu adalah sikap sopan.";
        r.style.color = "green";
      } else {
        r.textContent = "❌ Ups! Itu tidak sopan. Yuk, belajar lebih baik lagi.";
        r.style.color = "red";
      }
    }
  </script>
</body>
</html>
