# Project Overview

## Purpose

@ver0/eslint-formatter-gha is an ESLint formatter designed specifically for GitHub Actions environments. It converts
ESLint linting results into GitHub Actions annotations, providing inline feedback directly within pull requests and
GitHub's interface.

## Architecture

### Core Components

- **GHAFormatter**: The main formatter function that processes ESLint results
- **Severity Mapping**: Maps ESLint severity levels (0, 1, 2) to GitHub Actions annotation types (notice, warning,
  error)
- **GitHub Actions Integration**: Uses @actions/core library to create properly formatted annotations

### Key Features

- Seamless ESLint integration via standard formatter interface
- Proper error positioning with line and column information
- Rule ID inclusion for better debugging context
- Grouped output for cleaner GitHub Actions logs

## Technical Stack

- **Language**: TypeScript
- **Runtime**: Node.js ≥18
- **Dependencies**: @actions/core for GitHub Actions integration
- **Build**: TypeScript compiler with declaration files
- **Package Management**: Yarn v4 with Corepack

## Usage Context

This formatter is primarily used in CI/CD pipelines where ESLint runs as part of GitHub Actions workflows. It provides
developers with immediate, contextual feedback about code quality issues directly in their pull requests.
