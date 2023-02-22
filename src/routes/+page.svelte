<script>
  let name = '';
  let date = '';
  let timeIn = '';
  let timeOut = '';

  function handleSubmit() {
    const attendance = { name, date, timeIn, timeOut };
    // simpan data absensi ke database atau sistem penyimpanan lainnya
  }
</script>

<form on:submit|preventDefault={handleSubmit}>
  <label for="name">Nama:</label>
  <input type="text" id="name" bind:value={name} />

  <label for="date">Tanggal:</label>
  <input type="date" id="date" bind:value={date} />

  <label for="timeIn">Waktu Masuk:</label>
  <input type="time" id="timeIn" bind:value={timeIn} />

  <label for="timeOut">Waktu Keluar:</label>
  <input type="time" id="timeOut" bind:value={timeOut} />

  <button type="submit">Simpan</button>
</form>
