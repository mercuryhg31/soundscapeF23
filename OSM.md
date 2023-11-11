# Installation And Integration for Mapbox

## Table of Contents

- [Installation](#istallation)

## Installation

1. Create a Mapbox account and find your access token.
2. Change to the main frontend directory in `soundscape-authoring/frontend`
3. Add to `/package.json` in `"dependencies"`
    `"mapbox-gl": "^2.14.1",`
    Run `npm install`
4. Add to `src/app.js`
    * In header imports
        `import mapboxgl from '!mapbox-gl'; // eslint-disable-line import/no-webpack-loader-syntax`
        `mapboxgl.accessToken = 'your access token';`
    * In `constructor()` function, add the following to its `state` object
        `lng: -70.9,`
        `lat: 42.35,`
        `zoom: 9,`
    * In `componentDidMount()`, add
        `const map = new mapboxgl.Map({`
            `container: this.mapContainer.current,`
            `style: 'mapbox://styles/mapbox/streets-v12',`
            `center: [this.state.lng, this.state.lat],`
            `zoom: this.state.zoom`
        `});`
    * In `render()`, add between any `<div></div>`
        `<div ref={this.mapContainer} className="map-container" />`
5. Add import statement to `src/index.js`
    `import 'mapbox-gl/dist/mapbox-gl.css';`
6. Add display height to `src/index.css`
    `.map-container {`
        `height: 400px;`
    `}`
7. Build and run on backend with `npm run build` and in backend directory `python manage.py runserver`
8. These steps follow this [guide](https://docs.mapbox.com/help/tutorials/use-mapbox-gl-js-with-react/) with slight modifications.