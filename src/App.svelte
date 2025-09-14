<script>
	let count = $state(0)
	let factor = $state(0)
	let result = $derived(count * factor)
</script>

<fieldset>
	<legend>Derived State</legend>
	<label role="group"><input type="range" min="0" step="1" max="100" value="{count}" onchange="{() => count++}">&nbsp;{count}</label>
	<label role="group"><input type="range" min="0" step="1" max={count*100}  value="{factor}" onchange="{() => factor++}">&nbsp;{factor}</label>
	<p><span class="count">{count}</span> * <span class="factor">{factor}</span> = <span class="result">{result}</span></p>
</fieldset>

<style>
	.count{
		color: orangered;
	}
	.factor{
		color: cyan;
	}
	.result{
		color: black;
	}
</style>
