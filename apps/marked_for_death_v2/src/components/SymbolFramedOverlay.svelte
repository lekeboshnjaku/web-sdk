<script lang="ts">
	import { SpineProvider, SpineTrack } from 'pixi-svelte';

	import { SYMBOL_SIZE } from '../game/constants';

	type Props = {
		x?: number;
		y?: number;
	};

	const props: Props = $props();
	const frameSize = SYMBOL_SIZE * 0.92;
</script>

<!-- Template gold frame stand-in (M spine) until custom Wild Bandito art ships. -->
<SpineProvider x={props.x} y={props.y} key="M" width={frameSize} height={frameSize}>
	<SpineTrack trackIndex={0} animationName="low_multiplier_static" loop />
</SpineProvider>