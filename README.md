# FC
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Form Pendaftaran</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      text-align: center;
      padding: 50px;
    }
    .form-box {
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    input {
      padding: 10px;
      margin: 10px;
      width: 200px;
    }
    button {
      padding: 10px 20px;
      background: #25D366;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #128C7E;
    }
  </style>
</head>
<body>

  <div class="form-box">
    <h2>Form Pendaftaran</h2>
    <input type="text" id="nama" placeholder="Masukkan nama kamu">
    <br>
    <button onclick="kirimWa()">Daftar via WhatsApp</button>
  </div>

  <script>
    function kirimWa() {
      const nama = document.getElementById('nama').value;
      const nomor = "6283823958674"; // Ganti dengan nomor WA kamu
      const pesan = `Halo teman, saya ${nama} apa kabar tuan.`;
      const url = `https://wa.me/${nomor}?text=${encodeURIComponent(pesan)}`;
      window.open(url, '_blank');
    }
  </script>

</body>
</html>
