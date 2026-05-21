name: Build and Test

on:
push:
branches:
- main
pull_request:
branches:
- main

jobs:
build:
runs-on: ubuntu-latest

steps:
  # Step 1: Check out your repository code
  - name: Checkout Code
    uses: actions/checkout@v4

  # Step 2: Set up Node.js environment
  - name: Setup Node.js
    uses: actions/setup-node@v4
    with:
      node-version: '20' # You can change this to match your older app's version (e.g., '16' or '18')
      cache: 'npm'

  # Step 3: Install dependencies
  - name: Install Dependencies
    run: npm ci # Using 'npm ci' is safer for CI/CD as it respects your package-lock.json strictly

  # Step 4: Run the build script
  - name: Build Project
    run: npm run build
