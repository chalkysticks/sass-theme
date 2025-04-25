# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build Commands
- `yarn build` - Compile SASS and copy assets to build directory
- `yarn clean` - Remove build directory
- `yarn serve` - Start HTTP server
- `yarn watch` - Watch SASS files for changes and recompile

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