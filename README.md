# Useful CLI commands for NODEJS/NPM and Playwright that I used.

# Installs node_modules from package-lock.json
npm install

# Opens the tests from the tests folder in the Playwright UI.
npx playwright test --ui

# Opens up a debug window. Very useful for finding locators for your tests.
npx playwright test --debug

# Runs the tests.
npx playwright test

# Runs the tests in a specific browser. Here it is Chromium.
npx playwright test --project=chromium

# Runs the tests in headed mode, in which you are able to see what the tests are doing.
npx playwright test --headed

# Shows a report of the outcomes of the tests.
npx playwright show-report

# Installs types/node as a dev dependency.
npm install @types/node --save-dev

# Shows which browsers Playwright has downloaded.
npx playwright install --dry-run

# Installs the Playwright browsers: chromium, firefox and webkit.
npx playwright install

# Installs playwright/test version 1.34.3 as a dev dependency.
npm install --save-dev @playwright/test@1.34.3

# Initialises a new NodeJS project and says yes to all configurations.
npm init -y

# Starts the Playwright code generator.
npx playwright codegen https://playwright.dev/

# Starts the Playwright code generator and outputs the generated code to a specific file.
npx playwright codegen https://playwright.dev/ --output=tests/firsttry.spec.ts

# Runs the tests with trace on.
npx playwright test --trace on

# Specific CLI command to run based on configurations from the playwright.config.ts file. This one makes sure that the tests are only running with 1 worker for all tests instead of 1 worker for every test, when testing locally.
$env:LOCAL_TEST = "true"; npx playwright test