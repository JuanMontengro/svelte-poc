<script lang="ts">
	import Card from '../components/Card/index.svelte';
	const details = {
		title: 'Universal key value',
		description:
			'Universal DBMS for Docs • Graphs • Blobs • Vectors × in Local • Remote × RocksDB • LevelDB • UMem • UDisk × from C • C++ • Python • Java • GoLang',
		status: 'public',
		lang: 'C++',
		stars: 64,
		shares: 5
	};
</script>

<Card {details} />
