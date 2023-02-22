<script>
	import { onMount } from 'svelte';
  
	export let attendances = [];
  
	let chart;
  
	onMount(() => {
	  // buat chart menggunakan pustaka grafik seperti Chart.js
	  chart = new Chart(document.getElementById('attendance-chart'), {
		type: 'bar',
		data: {
		  labels: attendances.map(a => a.name),
		  datasets: [
			{
			  label: 'Waktu Masuk',
			  data: attendances.map(a => a.timeIn),
			  backgroundColor: 'rgba(255, 99, 132, 0.2)',
			  borderColor: 'rgba(255, 99, 132, 1)',
			  borderWidth: 1
			},
			{
			  label: 'Waktu Keluar',
			  data: attendances.map(a => a.timeOut),
			  backgroundColor: 'rgba(54, 162, 235, 0.2)',
			  borderColor: 'rgba(54, 162, 235, 1)',
			  borderWidth: 1
			}
		  ]
		},
		options: {
		  scales: {
			y: {
			  beginAtZero: true
			}
		  }
		}
	  });
	});
  </script>
  
  <h2>Grafik Absensi</h2>
  
  <canvas id="attendance-chart"></canvas>
  