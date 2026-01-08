# Elearn Frontend

> A professional React-based frontend for the Elearn Portal. Provides a clean, responsive UI
> for displaying courses and lessons.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Node.js](https://img.shields.io/badge/node-%3E%3D16.0.0-brightgreen.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/react-18.0.0-61dafb.svg)](https://react.dev/)

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)
- [Architecture](#architecture)
- [Best Practices](#best-practices)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Responsive Design**: Mobile-first approach with modern UI/UX
- **Course Management**: Display and manage courses with detailed information
- **Component-Based Architecture**: Reusable and maintainable components
- **Optimized Performance**: Production-ready build optimization
- **SEO-Friendly**: Proper metadata and structured content

## Prerequisites

Before you begin, ensure you have the following installed on your system:

| Requirement | Version | Installation |
|---|---|---|
| Node.js | >= 16.0.0 (LTS) | [Download](https://nodejs.org/) |
| npm | >= 8.0.0 | Included with Node.js |
| yarn | >= 1.22.0 | [Install Guide](https://yarnpkg.com/) |
| git | Latest | [Download](https://git-scm.com/) |

## Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-organization/elearn-frontend.git
cd elearn-frontend
```

### Step 2: Install Dependencies

Using npm:

```bash
npm install
```

Or using yarn:

```bash
yarn install
```

### Step 3: Configure Environment Variables

Create a `.env` file in the root directory:

```bash
cp .env.example .env
```

Update the following variables:

```env
REACT_APP_API_BASE_URL=http://localhost:5000/api
REACT_APP_API_TIMEOUT=5000
REACT_APP_DEBUG_MODE=false
```

### Step 4: Start Development Server

```bash
npm start
```

The application will open at `http://localhost:3000`

## Configuration

### API Endpoint Configuration

Update API endpoints in the following files:

- `src/pages/Home.js` - Course listing API
- `src/pages/AddNewCourse.js` - Course creation API
- `src/components/Header.js` - Navigation and auth endpoints

Example configuration:

```javascript
const API_BASE_URL = process.env.REACT_APP_API_BASE_URL;

const courseAPI = {
  list: `${API_BASE_URL}/courses`,
  create: `${API_BASE_URL}/courses`,
  update: `${API_BASE_URL}/courses/:id`,
  delete: `${API_BASE_URL}/courses/:id`,
};
```

## Usage

### Development Mode

```bash
npm start
```

Starts the development server with hot-reload capability.

### Production Build

```bash
npm run build
```

Creates optimized production build in the `build/` directory.

### Run Tests

```bash
npm test
```

Runs test suite in interactive watch mode.

### Eject Configuration

```bash
npm run eject
```

**Note**: This is a one-way operation. Once you eject, you cannot go back.

## Project Structure

```
elearn-frontend/
├── public/                 # Static assets and index HTML
│   ├── index.html         # Main HTML file
│   ├── manifest.json      # PWA manifest
│   └── robots.txt         # SEO robots configuration
│
├── src/                    # Source code
│   ├── components/         # Reusable React components
│   │   ├── CourseCard.js  # Course card component
│   │   ├── Footer.js      # Footer component
│   │   └── Header.js      # Header component
│   │
│   ├── pages/             # Page components
│   │   ├── Home.js        # Home page
│   │   ├── AboutUs.js     # About us page
│   │   ├── AddNewCourse.js # Add course page
│   │   └── ContactUs.js   # Contact us page
│   │
│   ├── App.js             # Root component
│   ├── App.css            # App styles
│   ├── index.js           # Application entry point
│   ├── index.css          # Global styles
│   ├── setupTests.js      # Test configuration
│   └── reportWebVitals.js # Performance metrics
│
├── build/                 # Production build output
│   ├── static/           # Optimized assets
│   ├── index.html        # Compiled HTML
│   └── manifest.json     # Build manifest
│
├── package.json           # Project dependencies and scripts
├── README.md             # This file
├── .env.example          # Environment variables template
└── .gitignore           # Git ignore rules
```

## Available Scripts

### `npm start`

Runs the app in development mode. Opens [http://localhost:3000](http://localhost:3000) in the browser.
The page will reload when you make changes.

### `npm test`

Launches the test runner in interactive watch mode.

### `npm run build`

Builds the app for production to the `build` folder.
The build is minified and optimized for best performance.

### `npm run eject`

Ejects the React configuration (irreversible operation).

## Architecture

### Component Hierarchy

```
App
├── Header
│   └── Navigation
├── Router
│   ├── Home
│   │   └── CourseCard[]
│   ├── AboutUs
│   ├── AddNewCourse
│   └── ContactUs
└── Footer
```

### Data Flow

The application follows a unidirectional data flow pattern:

1. Components receive props from parent components
2. Event handlers trigger state updates
3. State changes trigger re-renders
4. API calls are made via fetch or axios
5. Responses update component state

## Best Practices

### Code Quality

- Use ESLint for code linting
- Format code with Prettier
- Write meaningful component names
- Keep components small and focused
- Avoid prop drilling with Context API when necessary

### Performance

- Lazy load components using `React.lazy()`
- Memoize expensive computations with `useMemo`
- Optimize re-renders with `React.memo`
- Use code splitting for route-based components

### Security

- Never commit `.env` files with sensitive data
- Validate user input on both client and server
- Sanitize API responses
- Use HTTPS in production
- Implement CORS appropriately

## Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Coding Standards

- Follow ESLint configuration
- Use meaningful variable names
- Write comments for complex logic
- Keep functions small and reusable
- Test your changes before submitting

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

For support, email: support@elearn.com
Or open an issue on [GitHub Issues](https://github.com/your-organization/elearn-frontend/issues)

---

**Last Updated**: January 2026
**Maintained By**: Development Team

