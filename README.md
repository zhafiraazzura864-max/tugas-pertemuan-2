<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>AR Kelompok 5 - Minggu 2 (Scene v1)</title>

  <!-- Memanggil A-Frame -->
  <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>

  <!-- Memanggil AR.js -->
  <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar.js"></script>
</head>

<body style="margin:0; overflow:hidden;">

  <!-- SCENE AR -->
  <a-scene embedded arjs="sourceType: webcam; debugUIEnabled: false;">

    <!-- PENCAHAYAAN -->
    <a-light
      type="ambient"
      color="#ffffff"
      intensity="0.6">
    </a-light>

    <a-light
      type="directional"
      color="#ffffff"
      intensity="0.8"
      position="1 3 2">
    </a-light>

    <!-- MARKER HIRO -->
    <a-marker preset="hiro">

      <!-- ALAS -->
      <a-plane
        position="0 0 0"
        rotation="-90 0 0"
        width="2"
        height="2"
        color="#e9e5fa"
        opacity="0.7"
        transparent="true">
      </a-plane>

      <!-- OBJEK 1: KUBUS BIRU -->
      <a-box
        position="-0.6 0.25 0"
        width="0.5"
        height="0.5"
        depth="0.5"
        color="#4C6EF5">
      </a-box>

      <!-- OBJEK 2: BOLA ORANYE -->
      <a-sphere
        position="0 0.3 0"
        radius="0.3"
        color="#D9531E"
        metalness="0.3"
        roughness="0.4">
      </a-sphere>

      <!-- OBJEK 3: SILINDER HIJAU BERPUTAR -->
      <a-cylinder
        position="0.6 0.3 0"
        radius="0.2"
        height="0.6"
        color="#0B7F73"
        animation="
          property: rotation;
          to: 0 360 0;
          dur: 4000;
          loop: true;
          easing: linear">
      </a-cylinder>

      <!-- OBJEK 4: KOTAK BERTEKSTUR JPG BERGERAK NAIK-TURUN -->
      <a-box
        position="0 0.15 0.7"
        width="0.5"
        height="0.3"
        depth="0.5"
        src="assets/tekstur.jpg"
        animation="
          property: position;
          to: 0 0.6 0.7;
          dir: alternate;
          dur: 1500;
          loop: true;
          easing: easeInOutSine">
      </a-box>

    </a-marker>

    <!-- KAMERA -->
    <a-entity camera></a-entity>

  </a-scene>

</body>
</html>