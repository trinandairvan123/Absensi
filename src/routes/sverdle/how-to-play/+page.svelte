<script>
	export let attendances = [];
  
	let searchTerm = '';
	let filteredAttendances = [];
  
	$: filteredAttendances = attendances.filter(attendance => {
	  return (
		attendance.name.toLowerCase().includes(searchTerm.toLowerCase()) ||
		attendance.date.toLowerCase().includes(searchTerm.toLowerCase())
	  );
	});
  </script>
  
  <label for="search">Cari:</label>
  <input type="text" id="search" bind:value={searchTerm} />
  
  <AttendanceTable attendances={filteredAttendances} />
  