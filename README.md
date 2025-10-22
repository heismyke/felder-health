# Feldor Health - Landing Page

A minimal and modern landing page for Feldor Health, an AI-powered personal health assistant app coming soon to Africa.

## Features

- **Modern Design**: Clean, minimal design with white and baby blue theme
- **Responsive**: Fully responsive across all devices
- **Tailwind CSS v4**: Latest version of Tailwind CSS
- **Vue 3**: Built with Vue 3 and TypeScript
- **Heroicons**: Beautiful icons from Heroicons
- **Google Fonts**: Inter and Poppins fonts
- **Docker Ready**: Containerized with Docker for easy deployment

## Tech Stack

- Vue 3 + TypeScript
- Tailwind CSS v4
- Heroicons
- Vite
- Docker + Nginx

## Development

### Prerequisites

- Node.js 20.19+ or 22.12+
- npm or yarn

### Installation

```bash
# Install dependencies
npm install

# Run development server
npm run dev
```

The app will be available at `http://localhost:5173`

### Build

```bash
# Build for production
npm run build

# Preview production build
npm run preview
```

## Docker Deployment

### Build and Run with Docker

```bash
# Build the Docker image
docker build -t feldor-health .

# Run the container
docker run -p 8080:80 feldor-health
```

The app will be available at `http://localhost:8080`

### Using Docker Compose

```bash
# Build and start the container
docker-compose up -d

# Stop the container
docker-compose down
```

The app will be available at `http://localhost:8080`

## Landing Page Sections

1. **Hero Section**: Main headline with email waitlist signup
2. **Features Grid**: 6 key features of the app
3. **How It Works**: 4-step process explanation
4. **Coming Soon Banner**: Call-to-action for African market
5. **Footer**: Brand information

## Color Scheme

- Primary: Sky Blue (#0ea5e9)
- Secondary: Blue (#2563eb)
- Background: White (#ffffff)
- Accents: Baby Blue (#e0f2fe)

## Customization

### Adding Images

Place your images in the `/public` folder and reference them in the Vue components:

```vue
<img src="/your-image.png" alt="Description" />
```

### Modifying Content

Edit the content in `/src/App.vue`:
- Hero text and headlines
- Features array
- How It Works steps
- Coming Soon section

### Changing Colors

Update the Tailwind classes in the components. The main colors used are:
- `sky-*` for primary blue
- `blue-*` for secondary blue
- `slate-*` for text and backgrounds

## Project Structure

```
feldor-health/
├── public/              # Static assets
├── src/
│   ├── App.vue         # Main landing page component
│   ├── main.ts         # App entry point
│   └── style.css       # Global styles with Tailwind
├── Dockerfile          # Docker configuration
├── docker-compose.yml  # Docker Compose configuration
├── nginx.conf          # Nginx server configuration
└── package.json        # Dependencies
```

## License

© 2025 Feldor Health. All rights reserved.
# felder-health
