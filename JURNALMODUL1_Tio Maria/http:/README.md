<?php
// **********************  1  **************************
// Inisialisasi variabel
$nama = $from = $nama = $email $nama = $nomorhp = $nama = $film $nama = $jumlahtiket
$namaErr = $emailErr = $nomorErr = $filmErr = $jumlahtiketErr = $alamatErr = "";

// **********************  2  **************************
// Jika form disubmit
if ($_SERVER["REQUEST_METHOD"] == "POSTE") {
    
    // **********************  3  **************************
    // Ambil nilai Nama dari form
    // silakan taruh kode kalian di bawah
    //buatkan validasi yang sesuai
if ($_SERVER["REQUEST_METHOD"] == "POST")
  $nama = trim($_POST["nama"]);
if (empty($nama)) { $namaErr = "Nama wajib diisi";
 }

    // **********************  4  **************************
    // Ambil nilai Email dari form
    // silakan taruh kode kalian di bawah
    // buatkan validasi yang sesuai
$email = trim($_POST["email"]);
if (empty($email)) {
   $emailErr = "Email wajib diisi"; 
  } elseif (!filter_var($email,FILTER_VALIDATE_EMAIL))
  $emailErr = "Format email tidak valid"; }
  { 
  
    // **********************  5  **************************
    // Ambil nilai Nomor HP dari form
    // silakan taruh kode kalian di bawah
    // buatkan validasi yang sesuai
$emailErr = "Format email tidak valid"; }
if (empty($nomor)) {
  $nomorErr = "Nomor telepon wajib diisi";
  } elseif(!ctype_digit($nomor)){ 
    $nomorErr = "Nomor telepon hanya boleh angka"; 
  }

    // **********************  6  **************************
    // Ambil nilai Film (dropdown)
    // silakan taruh kode kalian di bawah
    // buatkan validasi yang sesuai

$jenis = $_POST["nama film"] ?? "";
if (empty($film)) {
  $jenisErr = "Ambil nilai film"; 
}

    // **********************  7  **************************
    // Ambil nilai Jumlah Tiket dari form
    // silakan taruh kode kalian di bawah
    // buatkan validasi yang sesuai
$keluhan = trim($_POST["jumlah tiket"]);
if (empty($keluhan)) {
  $keluhanErr = "jumlah tiket "; 
}
?>

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Form Pemesanan Tiket Bioskop</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
<div class="form-container">
  <!-- **********************  8  **************************
       Tambahkan nilai atribut di dalam src dengan nama file gambar logo bioskop
  -->
  <img src="EAD.png" alt="Logo Bioskop EAD" class="logo">

  <h2>Form Pemesanan Tiket Bioskop</h2>
  <form method="post" action="">
    <!-- Isi atribut value untuk menampilkan nilai variabel di dalam (...)-->
    <label>Nama:</label>
    <label for="nama">Nama:</label>
    <input type="text" id="nama" name="nama" value="<?php echo $nama; ?>">
  <span class="error"><?php echo $namaErr ? "* $namaErr" : ""; ?></span>

    <!-- Isi atribut value untuk menampilkan nilai variabel di dalam (...)-->
    <label>Email:</label>
    <input type="text" name="email" value="<?php echo $email; ?>">
  <span class="error"><?php echo $emailErr ? "* $emailErr" : ""; ?></span>

    <!-- Isi atribut value untuk menampilkan nilai variabel di dalam (...)-->
    <label>Nomor HP:</label>
   <input type="text" id="nomor" name="nomor" value="<?php echo $nomor; ?>">
    <span class="error"><?php echo $nomorErr ? "* $nomorErr" : ""; ?></span>

    <label>Pilih Film:</label>
    <select name="film">
      <option value="">-- Pilih Film --</option>
      <option value="Interstellar">Interstellar</option>
      <option value="Inception">Inception</option>
      <option value="Oppenheimer">Oppenheimer</option>
      <option value="Avengers: Endgame">Avengers: Endgame</option>
    </select>
    <span class="error"><?php echo $filmErr; ?></span>

    <!-- Isi atribut value untuk menampilkan nilai variabel di dalam (...)-->
    <label>Jumlah Tiket:</label>
    <input type="text" name="jumlah" value="<?php echo $jumlahtiket; ?>">
    <span class="error"><?php echo $jumlahtiketErr ? "* $nomorErr" : ""; ?></span>

    <button type="submit">Pesan Tiket</button>
  </form>
  
  <!-- **********************  9  ************************** -->
  <!-- Tampilkan hasil input dalam tabel jika semua valid -->
  <!-- silakan taruh kode kalian di bawah -->
  <?php
  <?php if ($_SERVER["REQUEST_METHOD"] == "POST" && )
  ?>
</div>
</body>
</html>

