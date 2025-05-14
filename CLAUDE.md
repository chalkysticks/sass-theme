# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands
- `yarn build` - Compile SASS and copy assets to build directory
- `yarn clean` - Remove build directory
- `yarn serve` - Start HTTP server
- `yarn watch` - Watch SASS files for changes and recompile

## Project Overview
This is the SASS theme library for ChalkySticks, providing themed CSS classes and variables. It's built on Bootstrap 5 and uses a modular, component-based architecture. The library defines the visual language for ChalkySticks applications and components.

## Architecture

### Entry Points
- Main entry point: `src/app/boot.scss` - Imports Bootstrap and application styles
- Core styles assembled in: `src/app/core.scss` - Imports all application components in logical order

### Folder Structure
- `src/app/` - Main SASS source files organized by component type
  - `animation/` - Reusable animations (fade, pulse, spin)
  - `branding/` - Brand-specific elements (logos, icons)
  - `element/` - Basic UI elements (header, footer, buttons)
  - `page/` - Page-specific styles
  - `ui/` - Reusable UI components (badge, avatar, glass)
  - `utility/` - Helper classes (spacing, color, text, visibility)
- `src/asset/` - Static assets including images, SVGs, and icons

### Theming System
- Variables defined in `src/app/variables.scss` using CSS custom properties
- Variables are organized by function (sizes, colors, typography, etc.)
- Theme switching implemented via classes (`.theme-light`, `.theme-dark`) that override CSS variables
- Bootstrap variables are extended/overridden in `src/app/theme.scss`

## Code Style Guidelines
- SASS structure follows a modular approach with component-based architecture
- Variables use CSS custom properties with `--` prefix
- Indentation: Use tabs for SASS files
- Naming: Use kebab-case for class names, variables, and files
- Color naming follows a pattern (e.g., `--chalky-blue`, `--chalky-blue-2`)
- Imports should be grouped by category (variables, components, utilities)
- Component-based structure with separate files for UI elements, utilities, etc.
- Follow existing patterns for responsive design and color variations
- Maintain consistency with existing variable naming and component structure
- Bootstrap 5 is used as a foundation - follow its conventions where applicable

## Component Patterns
- Components generally follow this structure:
  1. Base styling/layout
  2. Variations (theme, size, type)
  3. Interaction states (hover, active, focus, disabled)
- Components often extend typography classes (e.g., `.badge` extends `.type-small-heading`)
- CSS custom properties are used to create variations without duplicating styles
- Z-index variables follow a defined hierarchy to manage stacking contexts
- Modified BEM-like naming convention for components and their children

## Key Utilities
- Utility classes provide consistent spacing, sizing, color, and text styling
- Responsive design based on Bootstrap's grid system and breakpoints
- Theming through variable overrides rather than direct property settings
- Animation utilities for common transitions and effects