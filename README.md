# BreezyBuddy Beta Tester Survey

A lightweight, single-file onboarding survey for **BreezyBuddy** beta testers.
It collects the information needed to set each tester up: device and OS,
notification preferences (language, frequency, personality style), API-key
readiness, preferred feedback channel, and study interests.

## Features
- **Single HTML file** — vanilla JS, no build step.
- **Bilingual** — English and German, switchable at any time.
- **One-question-at-a-time** flow with progress bar, keyboard (Enter) support,
  and auto-advance for single-choice questions.
- **Informed-consent gate** — declining skips straight to the closing screen.
- **Appwrite backend** — responses are saved as documents in an Appwrite
  collection.

## Setup
1. Create an Appwrite project, database, and collection.
2. Add the collection attributes listed in the comment at the top of
   `index.html` (all strings except `phone_usage_hours` and `duration_secs`,
   which are integers).
3. Set the collection permissions to allow guest / anonymous document creates.
4. Paste your `AW_PROJECT_ID`, `AW_DATABASE_ID`, and `AW_COLLECTION` IDs into
   the config block at the top of `index.html`.

## Deployment
Host `index.html` on GitHub Pages or any static host and share the link with
testers.

## Related
Main app repo: `github.com/sasilab/BreezyBuddy` (private)
