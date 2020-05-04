# Setting Up React / Webpack / Babel From Scratch

### Main Point of Reference:
https://www.valentinog.com/blog/babel/

#### Basically:
- Use packages listed in package.json
- Configure webpack accordingly
- Uses index.html, index.js as entry point by default so import components from there (or modify webpack config to support whatever you're doing)
- This is a good starting point - clone the repo, make some small modifications, and you should be ready to build a SPA

#### To add React Router to the dev server reference this:
https://dev-yakuza.github.io/en/react/react-router/
- Basically just configuring webpack dev server by adding this
```
devServer: {
	contentBase: './dist',
	port: 3000,
	historyApiFallback: true,
},
```

#### Why this works?
"historyApiFallback option returns index.html response instead of 404 response if the page does not exist corresponding to the URL. now, when we browser directly http://localhost:3000/page1 or http://localhost:3000/page2 again, we can see the page shown well."