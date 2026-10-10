# Movie Search Application

A lightweight movie search web app built with HTML, CSS, and JavaScript. Users can search for movies using the OMDb API, view matching results, and save favorite movies in the browser using `localStorage`.

## Overview

This project is a simple front-end application that lets users:

- Search movies by title
- View movie cards with poster, title, and release year
- Add movies to a favorites list
- Remove favorites from the list
- Keep favorites saved locally in the browser

## Features

- Real-time movie search using the OMDb API
- Responsive movie card layout
- Favorite movies saved in browser storage
- Easy front-end setup with no backend required
- Works as a static web app

## Tech Stack

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- OMDb API

## Project Structure

```text
Movie Search Application/
├── index.html
├── style.css
├── script.js
└── README.md
```

## Getting Started

### 1. Get an OMDb API key

- Visit the OMDb API website: https://www.omdbapi.com/
- Sign up to obtain an API key

### 2. Update the API key in the app

Open `script.js` and replace:

```js
const API_URL = "http://www.omdbapi.com/?i=tt3896198&apikey=YOUR_API_KEY";
```

with your actual key:

```js
const API_URL = "http://www.omdbapi.com/?apikey=YOUR_API_KEY";
```

### 3. Run the app locally

Because this is a static front-end app, you can serve it using any local web server.

Example using Python:

```bash
cd "Movie Search Application"
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## How It Works

- The user enters a movie title in the search box
- The app sends a fetch request to the OMDb API using the query term
- Matching movie results are displayed as cards
- Each card includes:
  - Poster image
  - Movie title
  - Release year
  - Add to favorites button
- Favorites are saved using browser `localStorage`, so they persist across refreshes

## File Overview

### `index.html`
Defines the page layout, including:

- Search input
- Search button
- Movie results section
- Favorites section

### `style.css`
Contains the styling for the app layout, cards, buttons, and responsive sections.

### `script.js`
Handles:

- API requests
- Rendering movie results
- Adding/removing favorites
- Reading/writing favorites from `localStorage`
- Search button events

## Notes

- The app stores favorite movies in the browser, so the data is not shared across devices.
- The user must have a valid OMDb API key configured for searches to work.
- If the stylesheet does not load, verify that the file reference in `index.html` matches the actual CSS filename in the project.
- If the poster is unavailable, the app currently expects a placeholder image path (`placeholder.jpg`), which may need to be replaced with an actual image file if you want a fallback.

## Future Improvements

Possible enhancements include:

- Search on Enter key press
- Pagination or infinite scroll
- Detailed movie modal/pop-up
- Remove duplicates in search results
- Sorting and filtering favorites
- Better handling of missing poster images
