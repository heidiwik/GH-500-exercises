# GH-500 Exercises

Hands-on exercises for **GH-500: GitHub Advanced Security** training. Each folder has a small, deliberately vulnerable code sample from a React/TypeScript (Material UI) web app. Add it to your own project to see how GitHub's security features find and report the problem.

> ⚠️ **For educational use only.** This code contains known vulnerabilities on purpose. Do not deploy it or use it in production.

## Exercises

- **`code-scanning-exercise/`**: `AboutUs.tsx` reads a `url` query parameter and redirects the browser to it without checking it. This open redirect should raise the CodeQL alert `js/client-side-unvalidated-url-redirection` when code scanning runs.
- **`dependabot-exercise/`**: `FrontPage.txt` is a photo-gallery page that uses `lodash`. Follow `instructions.md` to replace your `FrontPage.tsx` with it and install the vulnerable `lodash@4.17.20`, which should cause Dependabot to raise alerts for known lodash CVEs.

## Usage

These files aren't a standalone app. Copy them into a React + Vite project where GitHub code scanning (CodeQL) and Dependabot are turned on. Then commit the changes and look at the alerts under the repository's **Security** tab.
