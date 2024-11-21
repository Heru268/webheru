<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validasi Form</title>
    <link rel="stylesheet" href="validasi_form.css" type="text/css">
</head>
<body>
    <center>
        <h2>FORM PENDAFTARAN</h2>
    </center>
    <div class="Login">
        <form action="#" method="post" onsubmit="return validasi()">
            <div>
                <label>Nama Lengkap : </label>
                <input type="text" name="nama" id="nama">
            </div>
            <div>
                <label>Email : </label>
                <input type="email" name="email" id="email">
            </div>
            <div>
                <label>Nomor Telepon : </label>
                <input type="text" name="telepon" id="telepon">
            </div>
            <div>
                <label>Alamat :</label>
                <textarea name="alamat" id="alamat" cols="40" rows="5"></textarea>
            </div>
            <input type="submit" value="Daftar" class="tombol">
        </form>
    </div>

    <script type="text/javascript">
        function validasi() {
            var nama = document.getElementById("nama").value;
            var email = document.getElementById("email").value;
            var telepon = document.getElementById("telepon").value;
            var alamat = document.getElementById("alamat").value;

            if (nama == "" || email == "" || telepon == "" || alamat == "") {
                alert('Anda harus mengisi data dengan lengkap!');
                return false; // Menghentikan pengiriman form
            }

            // Validasi nomor telepon (hanya angka)
            if (!/^\d+$/.test(telepon)) {
                alert('Nomor telepon harus berupa angka!');
                return false;
            }

            return true; // Data valid, form bisa dikirim
        }
    </script>
</body>
</html>
