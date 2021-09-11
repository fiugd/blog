At some point, I'd like to tackle themes.  Here are some thoughts on that.



An example of switching user preference for color scheme:
from [web.dev color scheme](https://web.dev/color-scheme/)

<script>
	const meta = document.querySelector('meta[name="color-scheme"]');
	let colorScheme = 'light';
	meta.content = colorScheme
	if (!window.frameElement) {  
		window.setInterval(() => {    
			colorScheme = colorScheme === 'light' ? 'dark' : 'light';
			document.documentElement.style.colorScheme = colorScheme; 
			meta.content = colorScheme;
			const root = window.frames[0].document.documentElement;
			root.style.colorScheme = colorScheme;
			root.querySelector('meta[name="color-scheme"]').content = colorScheme;
		}, 3000);
	}
</script>


