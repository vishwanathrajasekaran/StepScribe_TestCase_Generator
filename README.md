# TestForge — Automation Code Generator

A client-side, deterministic test-code generator built with plain HTML, CSS, and JavaScript. It requires no server, package manager, API keys, or runtime dependencies. It can be committed to Git and deployed to Vercel as a static site.

## Run locally
- Open `index.html` directly in a modern browser, or
- Serve this directory with any static file server.

## Deploy to Vercel
1. Create a Git repository and commit `index.html` and `README.md`.
2. Import the repository into Vercel.
3. Framework preset: **Other**.
4. Build command: leave blank.
5. Output directory: `.` (the repository root).
6. Deploy.

No environment variables are required.

## Use
1. Select tool, language, and test framework.
2. Add test steps in the Steps tab.
3. Add key/value locator definitions in Locators.
4. Optionally map helper methods in Your methods.
5. Generate, review the trace panel, then copy or download the generated code.
6. Save setup exports all input and configuration values as JSON.

## Supported target stacks
- Selenium: C#, Java, Python, TypeScript
- Playwright: C#, TypeScript (other Playwright language selections are intentionally rejected)
- Cypress: TypeScript only

## Important notes
- This is a deterministic template-based generator. It does not call an LLM or send data over the network.
- Generated code is a starting point, not a guarantee of compiling in every project. Browser setup, package versions, project-specific helpers, and framework conventions can differ. Review generated code and install the appropriate dependencies before running it.
- Locator input is intentionally conservative. Use simple `key = locator-expression` entries or a JSON object. Missing locator keys are surfaced in the trace panel and are not guessed.
- Selenium C# wait examples may require Selenium.Support and SeleniumExtras.WaitHelpers in the consuming project.
- The tool does not bundle or install any test framework/browser driver.
