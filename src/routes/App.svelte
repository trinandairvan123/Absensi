<script>
    let isPresent = false;
  
    function togglePresence() {
      isPresent = !isPresent;
    }
  </script>
  
  <h1>Selamat Datang!</h1>
  <p>Status Presensi: {isPresent ? "Hadir" : "Tidak Hadir"}</p>
  
  <button on:click={togglePresence}>
    {isPresent ? "Tidak Hadir" : "Hadir"}
  </button>
  