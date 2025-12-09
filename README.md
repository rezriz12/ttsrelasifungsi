[TTS RELASI FUNGSI.html](https://github.com/user-attachments/files/24046012/TTS.RELASI.FUNGSI.html)
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #FFC5D3;
      margin: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      min-height: 100vh;
      padding-top: 100px;
    }

    h1 {
      margin-bottom: 20px;
      color: #333;
      text-align: center;
    }

    /* Perbesar iframe Wordwall */
    iframe {
      border: none;
      width: 98vw;
      height: 80vh;
      border-radius: 16px;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
      margin-top: 10px;
    }

    .note {
      margin-top: 15px;
      color: #555;
      font-size: 15px;
      text-align: center;
    }

    /* Tombol Petunjuk, Alat Bantu, dan Penjelasan */
    #helpBtn, #toolBtn, #explainBtn {
      position: fixed;
      right: 15px;
      background-color: #0078d4;
      color: white;
      padding: 10px 18px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
      z-index: 999;
    }

    #helpBtn:hover, #toolBtn:hover, #explainBtn:hover { background-color: #005fa3; }

    #helpBtn { top: 15px; }
    #toolBtn { top: 65px; }
    #explainBtn { top: 115px; } /* posisi di bawah tombol alat bantu */

    /* Popup umum */
    .modal {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.3);
      padding: 25px;
      width: 380px;
      max-width: 90%;
      z-index: 1000;
      line-height: 1.6;
    }

    .modal h3 {
      margin-top: 0;
      color: #d6336c;
      text-align: center;
    }

    .modal ul {
      padding-left: 20px;
    }

    .closeBtn {
      background-color: #d6336c;
      color: white;
      border: none;
      padding: 8px 14px;
      border-radius: 6px;
      cursor: pointer;
      margin-top: 10px;
      display: block;
      margin-left: auto;
      margin-right: auto;
    }

    .closeBtn:hover { background-color: #b32057; }

    a.video-link {
      color: #0078d4;
      text-decoration: none;
      font-weight: bold;
    }

    a.video-link:hover {
      text-decoration: underline;
      color: #005fa3;
    }
  </style>
</head>
<body>
  <h1>🎀 Teka-Teki Relasi dan Fungsi 🎀</h1>

  <!-- Tombol Petunjuk -->
  <button id="helpBtn">📘 Petunjuk</button>

  <!-- Tombol Alat Bantu -->
  <button id="toolBtn" onclick="window.open('https://www.symbolab.com/solver/functions-calculator?utm_source=chatgpt.com', '_blank')">
    🧮 Alat Bantu
  </button>

  <!-- Tombol Penjelasan -->
  <button id="explainBtn">🔎 Penjelasan</button>

  <!-- Popup Petunjuk -->
  <div id="helpModal" class="modal">
    <h3>📘 Petunjuk Pengerjaan</h3>
    <ul>
      <li>Bacalah judul teka-teki dengan saksama. Tema kali ini adalah <b>Relasi dan Fungsi</b>.</li>
      <li>Klik kotak atau nomor pada permainan untuk mulai mengisi jawaban.</li>
      <li>Ketik huruf pada kotak. Huruf otomatis berubah menjadi <b>huruf besar</b>.</li>
      <li>Jika jawaban benar, kotak berubah <b>warna hijau</b> dan terkunci.</li>
      <li>Gunakan tombol <b>Cek Jawaban</b> di Wordwall untuk melihat hasil atau skor kamu.</li>
      <li>Gunakan tombol <b>Reset</b> untuk mengulang permainan.</li>
      <li>Jika soal berupa <b>fungsi atau perhitungan</b>, klik tombol <b>🧮 Alat Bantu</b> di kanan atas.</li>
      <li>Pastikan koneksi internet stabil agar permainan dapat dimuat dengan sempurna.</li>
    </ul>
    <button class="closeBtn" id="closeHelp">Tutup</button>
  </div>

  <!-- Popup Penjelasan -->
  <div id="explainModal" class="modal">
    <h3>🔎 Penjelasan Soal</h3>
    <ul>
      <li>📺 Nomor <b>4</b> dan <b>7</b>: <br>
        <a class="video-link" href="https://youtu.be/iBe7hvD5YiY?si=AQDe9bVPGqs8TV02" target="_blank">
          Klik di sini untuk menonton penjelasan →
        </a>
      </li>
      <li>📺 Nomor <b>8</b>, <b>9</b>, dan <b>10</b>: <br>
        <a class="video-link" href="https://youtu.be/lHFMKb-iDUw?si=twQK-S_pKAm-UA16" target="_blank">
          Klik di sini untuk menonton penjelasan →
        </a>
      </li>
    </ul>
    <button class="closeBtn" id="closeExplain">Tutup</button>
  </div>

  <!-- Embed Wordwall -->
  <iframe src="https://wordwall.net/id/embed/33d226d2d6c6477ba4395a7a8bd5b7cb?themeId=57&templateId=11&fontStackId=21" allowfullscreen></iframe>

  <p class="note">💡 Gunakan layar penuh untuk pengalaman terbaik.</p>

  <script>
    // Tombol Petunjuk
    const helpBtn = document.getElementById("helpBtn");
    const helpModal = document.getElementById("helpModal");
    const closeHelp = document.getElementById("closeHelp");

    helpBtn.onclick = () => helpModal.style.display = "block";
    closeHelp.onclick = () => helpModal.style.display = "none";

    // Tombol Penjelasan
    const explainBtn = document.getElementById("explainBtn");
    const explainModal = document.getElementById("explainModal");
    const closeExplain = document.getElementById("closeExplain");

    explainBtn.onclick = () => explainModal.style.display = "block";
    closeExplain.onclick = () => explainModal.style.display = "none";

    // Tutup modal jika klik di luar kotak
    window.onclick = (e) => {
      if (e.target === helpModal) helpModal.style.display = "none";
      if (e.target === explainModal) explainModal.style.display = "none";
    };
  </script>
</body>
</html>
