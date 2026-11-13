# Project instructions

- The quiz is a standalone `index.html`: markup, styles, question data, and behavior live in that file. Open it directly in a browser; keep it usable without a server or build step.
- Each entry in `questions` has a question, four answers, a zero-based `correct` index, and a fact shown after answering. If changing the question count, also update the static total and progress bar's `aria-valuemax` in the markup, the introductory copy, and the perfect-score threshold in the results logic.
- `renderQuestion()` builds answer buttons; `selectAnswer()` locks them, updates the score and progress, and announces feedback. The next and restart handlers manage screen visibility and move focus to the new heading. Preserve this flow when changing quiz behavior.
- Theme colors are CSS custom properties switched by `data-theme` on the root element. The initial theme follows the system preference; the toggle updates its label and accessible name. Keep both themes legible and respect the reduced-motion rule.
- The feedback is a live region, the progress bar exposes answered-question count through ARIA, and keyboard focus is moved on question and results transitions. Preserve these behaviors when modifying the interface.
- For a manual browser check, answer both correctly and incorrectly, advance through all questions, check the score and results, restart, and exercise the theme toggle and keyboard navigation.
