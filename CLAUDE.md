# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Common Commands

- **Development**: `npm run dev` - Starts the Vite development server
- **Build**: `npm run build` - Creates production-optimized build
- **Preview**: `npm run preview` - Previews the production build locally
- **Lint**: `npm run lint` - Runs ESLint to check for code issues
- **Install Dependencies**: `npm install` - Installs all project dependencies

## Project Structure

This is a modern Todo Dashboard web application built with:

- **React 19** - Frontend library for building user interfaces
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework for styling
- **ESLint** - Code quality and linting

### Key Directories:
- `src/` - Contains all source code
  - `src/App.jsx` - Main application component with todo logic
  - `src/index.css` - Tailwind CSS imports and base styles
  - `src/assets/` - Static assets (logos, images)
  - `src/main.jsx` - Entry point that renders the React app

### Architecture Overview:
The application follows a simple component architecture:
- Single `TodoApp` component manages all state and logic
- State managed with React `useState` hooks for:
  - Todo items array
  - Input field value
  - Active filter (all/active/completed)
- UI consists of:
  - Header with title and description
  - Add todo form with input and button
  - Stats panel showing item count and filter buttons
  - Todo list with checkboxes, text, and delete buttons
  - Clear completed button (conditionally rendered)
  - Footer with copyright information

### Features:
- Add new todos with Enter key or button click
- Toggle todo completion status
- Delete individual todos
- Filter todos (all/active/completed)
- Clear completed todos
- Persistent client-side state (resets on page refresh)
- Responsive design with Tailwind CSS
- Dark/light mode support via Tailwind's dark variant
- Todo completion timestamps