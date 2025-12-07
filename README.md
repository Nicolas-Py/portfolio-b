# Portfolio - Nicolas Py

A Bauhaus-inspired portfolio website showcasing projects, writing, and about information.

## Features

- **Projects**: Displays projects with status badges (Live, Completed, Under Development)
- **Writing**: Shows essays and articles with publication dates
- **About**: Personal bio, skills, and contact information
- All data is fetched dynamically from the API at `https://nicolas-py.github.io/portfolio-provider/api/portfolio.json`

## Running Locally

Since this is a static website, you can run it locally using any simple HTTP server. Here are several options:

### Option 1: Python HTTP Server (Recommended)

If you have Python installed:

```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Then open your browser to `http://localhost:8000`

### Option 2: Node.js HTTP Server

If you have Node.js installed:

```bash
# Install http-server globally (one time)
npm install -g http-server

# Run the server
http-server -p 8000
```

Or using npx (no installation needed):

```bash
npx http-server -p 8000
```

### Option 3: PHP Built-in Server

If you have PHP installed:

```bash
php -S localhost:8000
```

### Option 4: VS Code Live Server

If you're using VS Code:

1. Install the "Live Server" extension
2. Right-click on `index.html`
3. Select "Open with Live Server"

### Option 5: WebStorm Built-in Server

If you're using WebStorm:

1. Right-click on `index.html`
2. Select "Open in Browser" or "Preview in Browser"
3. Or use the built-in preview feature

## Important Notes

- The website fetches data from an external API, so you need an internet connection for it to work properly
- CORS may be an issue if the API doesn't allow localhost origins - in that case, you may need to use a browser extension to disable CORS or configure a proxy

## Project Structure

```
portfolio-b/
├── index.html          # Main landing page
├── projects.html       # Projects page (fetches from API)
├── writing.html        # Writing page (fetches from API)
├── about.html          # About page (fetches from API)
├── index.css           # Styles for index page
├── project.css         # Styles for project pages
└── util/
    └── favicon.ico     # Site favicon
```

## API Endpoint

The website fetches data from:
`https://nicolas-py.github.io/portfolio-provider/api/portfolio.json`

The API returns:

- `projects`: Array of project objects
- `writing`: Array of writing/essay objects
- `about`: Object containing bio, skills, and contact information
