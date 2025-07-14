<!DOCTYPE html>
<html>
<head>
  <title>Pesan Cinta</title>
</head>
<body style="text-align:center; padding-top: 100px; background-color: #ffe6f0; font-family: sans-serif;">

  <h1 id="pesan" style="color: #d6336c; font-size: 2em;"></h1>

  <!-- Pemutar Musik Otomatis -->
  <audio id="musik" autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mpeg">
    Browser kamu tidak mendukung audio.
  </audio>

  <script>
    // Teks pesan cinta
    let pesan = "Aku sayang kamu Ranty Limaya Pangestu";

    // Tampilkan ke halaman
    document.getElementById("pesan").innerText = pesan;

    // Musik mulai otomatis (kadang butuh interaksi pengguna tergantung browser)
    let musik = document.getElementById("musik");
    musik.play().catch(() => {
      // Kalau gagal autoplay, tampilkan tombol
      let btn = document.createElement("button");
      btn.innerText = "Putar Musik";
      btn.style.padding = "10px 20px";
      btn.style.fontSize = "18px";
      btn.onclick = () => musik.play();
      document.body.appendChild(btn);
    });
  </script>

</body>
</html>
