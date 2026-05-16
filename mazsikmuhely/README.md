# Mazsikmuhely

## Project Overview

Mazsikmuhely is a Vue 3-based web application designed for showcasing precision braking systems and components. The project leverages modern tools and frameworks to ensure high performance and maintainability.

## Features

- **Vue 3**: Utilizes the latest Vue.js framework for building reactive user interfaces.
- **Vue Router**: Implements client-side routing for seamless navigation.
- **Vite**: A fast build tool for development and production.
- **Unit Testing**: Includes Vitest for unit testing.
- **Linting and Formatting**: Ensures code quality with ESLint and Oxlint.

## Project Structure

```
mazsikmuhely/
├── public/                # Static assets
├── src/                   # Source code
│   ├── assets/            # Styles and images
│   ├── components/        # Reusable Vue components
│   ├── router/            # Application routing
│   ├── views/             # Page-level components
│   ├── App.vue            # Root component
│   └── main.ts            # Application entry point
├── package.json           # Project metadata and dependencies
├── vite.config.ts         # Vite configuration
└── README.md              # Project documentation
```

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:

   ```bash
   cd mazsikmuhely
   ```

3. Install dependencies:
   ```bash
   pnpm install
   ```

## Development

To start the development server, run:

```bash
pnpm dev
```

This will launch the application at `http://localhost:5173/`.

## Build

To build the application for production, use:

```bash
pnpm build
```

The output will be in the `dist/` directory.

## Testing

Run unit tests with:

```bash
pnpm test:unit
```

## Linting and Formatting

Ensure code quality by running:

```bash
pnpm lint
pnpm format
```

## Dependencies

### Production

- **vue**: ^3.5.32
- **vue-router**: ^5.0.4
- **primeicons**: ^7.0.0

### Development

- **@vitejs/plugin-vue**: ^6.0.6
- **@vitejs/plugin-vue-jsx**: ^5.1.5
- **eslint**: ^10.2.1
- **vitest**: ^1.6.16

## License

This project is licensed under the MIT License.
