# React Foundations By Next Docs

this is my journey to learn and understand React

## Folder Structure:

```
|- chapter-03
    |- index.html
|- chapter-04
    |- index.html
```

## Code Explaining

- chapter-03/index.html
```
<html>
	<body>
		<div
			id="app"
		>			
		</div>
		<script
			type="text/javascript"
		>
			// Select the div element with 'app' id
			const app = document.getElementById('app');
		
			// Create a new H1 element
			const header = document.createElement('h1');

			// Create a new text node for the H1 Element
			const text = 'Develop. Preview. Ship.';
			const headerContent = document.createTextNode(text);

			// Append the text to H1 element
			header.appendChild(headerContent);

			// Place the H1 element inside the div
			app.appendChild(header);			
		</script>
	</body>
</html>
```

- chapter-04/index.html
```
<html>
	<body>
		<div
			id="app"
		></div>
		<!-- adding react -->
		<script 
			src="https://unpkg.com/react@18/umd/react.development.js"
		></script>
		<!-- adding react dom -->
		<script 
			src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"
		></script>
		<!-- adding babel -->
		<script 
			src="https://unpkg.com/@babel/standalone/babel.min.js"
		></script>
		<!-- react use jsx -->
		<script
			type="text/jsx"
		> 
				// Select the div element with 'app' id
				const app = document.getElementById('app');

				// react root using reactDOM
				const root = ReactDOM.createRoot(app);

				// you can render any jsx inside the render 
				root.render(<h1>Develop. Preview. Ship.</h1>);
		</script>
	</body>
</html>
```
