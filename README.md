# React Foundations By Next Docs

this is my journey to learn and understand React

## Folder Structure:

```
|- chapter-03
    |- index.html
|- chapter-04
    |- index.html
|- chapter-05
    |- index.html
|- chapter-06
    |- index.html
|- chapter-07
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

- chapter-05/index.html
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

				function Header() { // component name should be in capatilized
					return <h1>Develop. Preview. Ship.</h1>;
				}

				function HomePage() {
					return (
						<div>
							<Header /> {/*  you can call other component inside a component */}
							<p>
								Welcome to home page.
							</p>
						</div>
					)
				}

				// react root using reactDOM
				const root = ReactDOM.createRoot(app);

				// you can render any jsx inside the render 
				root.render(<HomePage />);
		</script>
	</body>
</html>
```

- chapter-06/index.html
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

				function Header({ title }) { // component name should be in capatilized - you can assign all the props as function parameters
					return <h1>{title}</h1>;
				}

				function HomePage() {
					const names = ['Ada Lovelace', 'Grace Hopper', 'Margaret Hamilton'];
					return (
						<div>
							<Header title="Develop. Preview. Ship." /> {/*  you can call other component inside a component - you can use props in the component by passing the then utilize then inside the component as dynamic data */}
							{/*<p>
								Welcome to home page.
							</p>*/}
							{names.map((name) => ( // JSX only return in round brackets
								<li key={name}>{name}</li>
							))}
						</div>
					)
				}

				// react root using reactDOM
				const root = ReactDOM.createRoot(app);

				// you can render any jsx inside the render 
				root.render(<HomePage />);
		</script>
	</body>
</html>
```

- chapter-07/index.html
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

				function Header({ title }) { // component name should be in capatilized - you can assign all the props as function parameters
					return <h1>{title}</h1>;
				}

				function HomePage() {
					const names = ['Ada Lovelace', 'Grace Hopper', 'Margaret Hamilton'];
					const [like, setLike] = React.useState(0); // useState is a hook to manage state in functional component
					const handleClick = () => {
						setLike(like + 1); // set the state value
					}
					return (
						<div>
							<Header title="Develop. Preview. Ship." /> {/*  you can call other component inside a component - you can use props in the component by passing the then utilize then inside the component as dynamic data */}
							{/*<p>
								Welcome to home page.
							</p>*/}
							<ul>
								{names.map((name) => ( // JSX only return in round brackets
									<li key={name}>{name}</li>
								))}
							</ul>
							<button onClick={handleClick}>Like({like})</button> {/* you can add event listener in JSX */}
						</div>
					)
				}

				// react root using reactDOM
				const root = ReactDOM.createRoot(app);

				// you can render any jsx inside the render 
				root.render(<HomePage />);
		</script>
	</body>
</html>
```

## Resources
I start my journey using this cool stuff so shout to them:
- https://nextjs.org/learn/react-foundations
