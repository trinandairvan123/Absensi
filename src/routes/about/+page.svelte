<script>
	export let attendances = [];
  
	function deleteAttendance(attendance) {
	  // hapus data absensi dari database atau sistem penyimpanan lainnya
	}
  </script>
  
  <table>
	<thead>
	  <tr>
		<th>Nama</th>
		<th>Tanggal</th>
		<th>Waktu Masuk</th>
		<th>Waktu Keluar</th>
		<th>Aksi</th>
	  </tr>
	</thead>
	<tbody>
	  {#each attendances as attendance}
		<tr>
		  <td>{attendance.name}</td>
		  <td>{attendance.date}</td>
		  <td>{attendance.timeIn}</td>
		  <td>{attendance.timeOut}</td>
		  <td>
			<button on:click={() => deleteAttendance(attendance)}>Hapus</button>
		  </td>
		</tr>
	  {/each}
	</tbody>
  </table>
  