<script>
	import { dev } from '$app/env';

	export let alt;
	export let src;
	export let align = 'none';
    export let style;

	let alignment = '';
	if (align === 'right') {
		alignment = `md:float-right`;
	} else if (align === 'left') {
		alignment = `md:float-left`;
	}

	const teaching = dev ? '' : '/teaching';
</script>

<img {alt} src="{teaching}{src}" class="mx-auto px-4 py-2 {alignment}" style={style} />
