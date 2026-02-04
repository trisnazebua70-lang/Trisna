<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Website Identitas Diri</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: linear-gradient(to right, #141E30, #243B55);
            color: #333;
        }

        /* TEKS BERJALAN */
        marquee {
            background: #000;
            color: #fff;
            padding: 12px;
            font-size: 18px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        /* CONTAINER */
        .container {
            max-width: 1000px;
            margin: 40px auto;
            background: #fff;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0,0,0,0.4);
        }

        /* HEADER */
        .header {
            background: linear-gradient(90deg, #6a11cb, #2575fc);
            color: white;
            text-align: center;
            padding: 30px;
        }

        /* SECTION */
        .section {
            padding: 30px;
        }

        .section h2 {
            color: #2575fc;
            border-bottom: 3px solid #2575fc;
            display: inline-block;
            padding-bottom: 5px;
            margin-bottom: 20px;
        }

        /* DESAIN 1 - PROFIL MODERN */
        .profile {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        .profile img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 5px solid #2575fc;
            object-fit: cover;
        }

        /* UPLOAD FOTO */
        input[type="file"] {
            margin-top: 10px;
        }

        /* DESAIN 2 - TABEL BIODATA */
        table {
            width: 100%;
            border-collapse: collapse;
        }

        td {
            padding: 10px;
            border-bottom: 1px solid #ccc;
        }

        td:first-child {
            font-weight: bold;
            width: 35%;
        }

        /* DESAIN 3 - CARD */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .card {
            background: linear-gradient(135deg, #43cea2, #185a9d);
            color: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 8px 15px rgba(0,0,0,0.3);
        }

        /* FOOTER */
        .footer {
            background: #2575fc;
            color: white;
            text-align: center;
            padding: 15px;
        }
    </style>
</head>
<body>

    <!-- TEKS BERJALAN -->
    <marquee>
        ✨ WEBSITE IDENTITAS DIRI ✨ PROFIL PRIBADI SISWA ✨ DESAIN MODERN & KEREN ✨
    </marquee>

    <div class="container">

        <!-- HEADER -->
        <div class="header">
            <h1>Identitas Diri</h1>
            <p>Website Profil Pribadi</p>
        </div>

        <!-- DESAIN 1 -->
        <div class="section">
            <h2>Profil Singkat</h2>
            <div class="profile">
                <div>
                    <img id="foto" src="foto saya.jpg" alt="Foto saya.jpg">
                    <br>
                    <!-- PERINTAH TAMBAH FOTO -->
                    <input type="file" accept="image/*" onchange="loadFoto(event)">
                </div>
                <div>
                    <p><b>Nama:</b> Trisnawati Zebua</p>
                    <p><b>Status:</b> Pelajar SMK</p>
                    <p><b>Jurusan:</b> Teknik komputer dan jaringan</p>
                </div>
            </div>
        </div>

        <!-- DESAIN 2 -->
        <div class="section">
            <h2>Biodata Lengkap</h2>
            <table>
                <tr>
                    <td>Nama Lengkap</td>
                    <td>Trisnawati Zebua</td>
                </tr>
                <tr>
                    <td>Tempat Tinggal</td>
                    <td>Desa Gada</td>
                </tr>
                <tr>
                    <td>Jenis Kelamin</td>
                    <td>Perempuan</td>
                </tr>
                <tr>
                    <td>Alamat</td>
                    <td>Gunungsitoli, Sumatera Utara</td>
                </tr>
                <tr>
                    <td>Sekolah</td>
                    <td>SMK Negeri 3 Gunungsitoli</td>
                </tr>
            </table>
        </div>

        <!-- DESAIN 3 -->
        <div class="section">
            <h2>Informasi Tambahan</h2>
            <div class="cards">
                <div class="card">
                    <h3>Hobi</h3>
                    <p>Membaca</p>
                </div>
                <div class="card">
                    <h3>Cita-cita</h3>
                    <p>Guru</p>
                </div>
                <div class="card">
                    <h3>Keahlian</h3>
                    <p>HTML<br>CSS<br>Dasar</p>
                </div>
            </div>
        </div>

        <!-- FOOTER -->
        <div class="footer">
            © 2026 | Website Identitas Diri
        </div>

    </div>

    <!-- SCRIPT FOTO -->
    <script>
        function loadFoto(event) {
            const foto = document.getElementById('foto');
            foto.src = URL.createObjectURL(event.target.files[0]);
        }
    </script>

</body>
</html>