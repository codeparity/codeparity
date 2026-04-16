# AGENTS.md

This document outlines the expected commands, code style, and conventions for AI agents operating within the CodeParity repository. Adhering to these guidelines ensures consistency, maintainability, and efficiency.

## 1. Build, Lint, and Test Commands

The following commands are essential for maintaining code quality and ensuring functionality.

### General Commands
- **Install Dependencies:**
  - For Node.js projects (if applicable): `npm install` or `yarn install`
  - For Python projects (if applicable): `pip install -r requirements.txt` or `poetry install`

### Linting
- **JavaScript/TypeScript:** `npm run lint` or `eslint .` (specific command may vary)
- **Python:** `ruff check .` or `flake8` (specific command may vary)

### Testing
- **All Tests:** `npm test` or `pytest` (specific command may vary)
- **Single Test:**
  - **JavaScript/TypeScript (Jest):** `npm test -- path/to/your/test.spec.js` (replace with actual test file path)
  - **Python (pytest):** `pytest path/to/your/test_file.py::test_function_name` (replace with actual test file and function name)

*Note: Specific commands may be defined in `package.json` scripts, `pyproject.toml`, or other configuration files. Always refer to these for the most accurate commands.*

## 2. Code Style Guidelines

Adherence to these guidelines ensures a consistent and readable codebase.

### Imports
- **Order:** Group imports logically (e.g., standard library, third-party, local).
- **Clarity:** Use `from module import specific_item` for clarity when only a few items are needed.

### Formatting
- **Indentation:** Use spaces for indentation. The standard is 2 or 4 spaces (verify with project examples).
- **Line Length:** Aim for a maximum line length of 80-120 characters.

### Types
- **Strong Typing:** Utilize type hints (e.g., Python type hints, TypeScript) where applicable to improve code clarity and prevent runtime errors.

### Naming Conventions
- **Variables:** Use `camelCase` for JavaScript/TypeScript, `snake_case` for Python.
- **Functions/Methods:** `camelCase` for JavaScript/TypeScript, `snake_case` for Python.
- **Classes:** `PascalCase` for both JavaScript/TypeScript and Python.
- **Constants:** `UPPER_SNAKE_CASE` for languages that support it.

### Error Handling
- **Exceptions:** Use try-catch blocks (JavaScript/TypeScript) or try-except blocks (Python) for expected errors.
- **Error Messages:** Provide clear, concise, and informative error messages.
- **Return Values:** Clearly define error return values or exceptions for functions.

## 3. Cursor and Copilot Rules

### Cursor Rules
- **Location:** Check `.cursor/rules/` or `.cursorrules` for any project-specific rules enforced by Cursor. These may include specific formatting, linting, or structural requirements.

### Copilot Instructions
- **Location:** Refer to `.github/copilot-instructions.md` for guidance on how Copilot should interact with the codebase, including preferred coding patterns, security considerations, and specific instructions for code generation.

*Note: If these files are not present, assume standard best practices unless otherwise indicated by project examples.*

## Project Intents: Artwork and Theming

The following outlines the project's intents regarding artwork and theming, crucial for guiding AI agents in visual asset creation and application styling.

### Core Theme: Simplicity
- **Palette:** Primarily black, white, and shades of grey (10 shades specified).
- **Structure:** Nested, indented structure for artwork, CSS, and headlines, following a "9 choices" model.

### Logo Design
- **Symbol of 9 Choices:**
    - A square symbol representing a 3x3 matrix.
    - **Frame Cube:** A 2D flat cube with a 2% margin.
    - **Inner Frame:** A 3x3 matrix of 9 squares with no margin.
    - **Choices:** 9 circles centered within each of the 9 squares.
    - **Flow:** 3 symmetrical lines flowing from the central circle to adjacent squares.

### Typography
- **Fonts:** Three primary fonts are to be used:
    - Semi-formal
    - Formal
    - Monospace

### Branding
- **Renders:** The symbol should be rendered with "Code" in a formal text style and "Parity" in an informal text style, alongside the symbol.
- **Layouts:** Both horizontal and vertical branding variations should be supported.

### Output Templates
- **Templates:** Support for various output templates including:
    - Office
    - XLS
    - Letterhead
    - Legals
