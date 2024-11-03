    # Lab5Web
    pratikum5
    <!DOCTYPE html>
    <html lang="en">
    <head>
    <title>Belajar JavaScript Dasar</title>
    <style>
        body { font-family: Arial, sans-serif; }
        button { margin: 5px; }
    </style>
    <script>
        function displayMessage(message) {
            const messageContainer = document.getElementById("messages");
            const newMessage = document.createElement("div");
            newMessage.textContent = message;
            messageContainer.appendChild(newMessage);
        }

        function helloWorld() {
            displayMessage("Hello World");
            console.log("Hello World");
        }

        function showAlert() {
            alert("Ini merupakan pesan untuk Anda.");
        }

        function cobaMenulis() {
            displayMessage("Selamat mencoba JavaScript. Semoga sukses!");
        }

        function tanyaNama() {
            var nama = prompt("Siapa nama Anda?", "Masukkan nama Anda");
            displayMessage("Hai, " + (nama || "Pengguna"));
        }

        function operasiAritmatika(val1, val2) {
            displayMessage("Perkalian: " + (val1 * val2));
            displayMessage("Pembagian: " + (val1 / val2));
            displayMessage("Penjumlahan: " + (val1 + val2));
            displayMessage("Pengurangan: " + (val1 - val2));
            displayMessage("Modulus: " + (val1 % val2));
        }

        function seleksiIfElse() {
            var nilai = prompt("Nilai (0-100):", 0);
            var hasil = (nilai >= 60) ? "Lulus" : "Tidak Lulus";
            displayMessage("Hasil: " + hasil);
        }

        function seleksiSwitch() {
            var val1 = prompt("Input nilai (1-5):");
            var output;
            switch (val1) {
                case "1": output = "Bilangan Satu"; break;
                case "2": output = "Bilangan Dua"; break;
                case "3": output = "Bilangan Tiga"; break;
                case "4": output = "Bilangan Empat"; break;
                case "5": output = "Bilangan Lima"; break;
                default: output = "Bilangan Lainnya";
            }
            displayMessage(output);
        }

        function cekBilangan() {
            var val1 = document.forms["kirim"].elements["T1"].value;
            document.forms["kirim"].elements["T2"].value = (val1 % 2 == 0) ? "Bilangan Genap" : "Bilangan Ganjil";
        }

        function ubahWarnaLB(warna) {
            document.body.style.backgroundColor = warna;
        }

        function hitung(ele) {
            var total = document.getElementById("total").value;
            total = (total ? parseInt(total) : 0);
            var harga = parseInt(ele.value);

            if (ele.checked) {
                total += harga;
            } else {
                if (total > 0) total -= harga;
            }
            document.getElementById('total').value = total;
        }
    </script>
    </head>
    <body onload="alert('Memanggil JavaScript lewat body onload')">
    <h1>Belajar JavaScript Dasar</h1>
    <div id="messages"></div>
![Cuplikan layar 2024-11-04 011629](https://github.com/user-attachments/assets/b49133fe-3082-48d4-a846-21c072d42e2a)

    <!-- Other sections remain unchanged -->
    <button onclick="helloWorld()">Tampilkan Hello World</button>
    <button onclick="showAlert()">Tampilkan Alert</button>
    <button onclick="cobaMenulis()">Tampilkan Pesan</button>
    <button onclick="tanyaNama()">Tanya Nama</button>
    <button onclick="operasiAritmatika(9, 2)">Hitung Aritmatika (9, 2)</button>
    <button onclick="seleksiIfElse()">Cek Kelulusan</button>
    <button onclick="seleksiSwitch()">Cek Bilangan</button>

    <form name="kirim" method="POST">
        <label>BIL <input type="text" name="T1" size="20"></label>
        <label>MERUPAKAN BIL <input type="text" name="T2" size="20" readonly></label>
        <button type="button" onclick="cekBilangan()">Tebak</button>
    </form>

    <button onclick="ubahWarnaLB('green')">Latar Belakang Hijau</button>
    <button onclick="ubahWarnaLB('white')">Latar Belakang Putih</button>

    <h3>Daftar Menu Makanan</h3>
    <label><input type="checkbox" value="5000" onclick="hitung(this);"> Ayam Goreng Rp.5.000</label><br>
    <label><input type="checkbox" value="500" onclick="hitung(this);"> Tempe Goreng Rp.500</label><br>
    <label><input type="checkbox" value="2500" onclick="hitung(this);"> Telur Dadar Rp.2.500</label><br>
    <strong>Total Bayar: Rp. <input id="total" type="text" readonly /></strong>

    <script>
        // Menampilkan tanggal modifikasi terakhir
        displayMessage("Dimodifikasi terakhir pada: " + document.lastModified);
    </script>
    </body>
    </html>
![Cuplikan layar 2024-11-04 011805](https://github.com/user-attachments/assets/dd63026d-217e-4b3c-96a2-53d469a36654)
