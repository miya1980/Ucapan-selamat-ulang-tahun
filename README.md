<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ucapan Ultah</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #FFD3A5, #FD6585);
      color: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      height: auto;
      flex-direction: column;
      text-align: center;
      padding: 20px;
    }

    .card {
      background: #fff;
      border-radius: 20px;
      padding: 30px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
      max-width: 400px;
      margin-top: 50px;
    }

    h1 {
      font-size: 2em;
      margin-bottom: 10px;
      color: #FD6585;
    }

    p {
      font-size: 1.1em;
    }

    .name {
      font-weight: bold;
      font-size: 1.3em;
      color: #FD6585;
      margin: 15px 0;
    }

    .btn {
      margin-top: 15px;
      display: inline-block;
      padding: 10px 20px;
      background: #25D366;
      color: white;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      transition: 0.3s ease;
    }

    .btn:hover {
      background: #1ebd5a;
    }

    img {
      width: 100%;
      border-radius: 10px;
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>🎉 Selamat Ulang Tahun!</h1>
    <p>Semoga panjang umur, sehat selalu, dan tercapai semua impianmu!</p>
    <div class="bagong" id="bagong banget">- Dari: Temanmu 🌟</div>

    <img src="https://i.imgur.com/OYbVOY2.jpg" alt="Ucapan Ulang Tahun" />

    <!-- Tombol Kirim WhatsApp -->
    <a class="btn" id="btnWA" href="#" target="_blank">Kirim Lewat WhatsApp</a>

    <!-- Tombol Download Gambar -->
    <a class="btn" href="https://i.imgur.com/OYbVOY2.jpg" download="ucapan-ulang-tahun.jpg">Download Gambar</a>
  </div>

  <script>
    // Tangkap nama dari URL: ?nama=bagong
    const urlParams = new URLSearchParams(window.location.search);
    const nama = urlParams.get("nama");

    // Ganti teks di halaman
    if (nama) {
      document.getElementById("namaPenerima").innerText = `Untuk: ${nama} 🎂`;
      const link = window.location.href;
      document.getElementById("btnWA").href = `https://wa.me/?text=Selamat ulang tahun ${nama}! Ini ada ucapan buat kamu: ${link}`;
    }
  </script>
</body>
</html>
