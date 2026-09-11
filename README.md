# Dot Zero

Dot Zero is a Vue 3 coming-soon homepage for a creative studio focused on helping new ideas take shape. The site uses a minimal editorial layout, custom visual treatment, responsive styling, and a simple email notification form.

## Tech Stack

- Vue 3 with `<script setup>`
- Vite
- Vue Router
- CSS with responsive layouts, custom properties, and animations
- Syne and DM Mono typography via Google Fonts

## Features

- Coming Soon homepage for Dot Zero
- Responsive desktop and mobile layout
- Reusable `BrandMark` component
- Reusable notification signup form
- Basic Vue Router setup with a home route
- Reduced-motion support for accessibility

## Getting Started

### Prerequisites

- Node.js 18 or newer
- npm

### Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/dot-zero.git
cd dot-zero
npm install
```

### Development

Start the Vite development server:

```bash
npm run dev
```

Open the local URL printed in your terminal, typically `http://localhost:5173/`.

### Production Build

Create an optimized production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## Project Structure

```text
src/
├── components/
│   ├── BrandMark.vue
│   └── NotifyForm.vue
├── router/
│   └── index.js
├── views/
│   └── HomeView.vue
├── App.vue
├── main.js
└── style.css
```

## Coming Soon Homepage

The homepage presents Dot Zero as a creative studio preparing to launch. It includes:

- Dot Zero branding and launch status
- A central “Make room for what’s next.” message
- Abstract orbital artwork built with CSS
- An email notification form
- Launch contact information in the footer

The notification form currently provides a local success state. Connect it to an email service or backend endpoint before using it in production.

## License

This project is currently private and does not include a public license.
