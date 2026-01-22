# Contributing to Maruq

Thanks for your interest in contributing to **Maruq** 🎉  
Before submitting anything, please read this carefully.

Maruq aims to be lightweight and working. Contributions are welcome - **half-finished features and untested changes are not**.

---

## General Rules

By opening a pull request, you agree that:

- Your code **works fully**, not partially
- Your code **has been tested**
- Your change either:
  - fixes a bug completely, **or**
  - fully implements a feature (no placeholders, no “future work”)
- Your pull request includes **clear instructions** on how to test the change

If any of the above are missing, the PR may be closed without review.

---

## No “Vibe Coding”

Please do **not** submit code that:
- “Mostly works”
- Is experimental without explanation
- Introduces unfinished APIs
- Adds features that require future PRs to function

Maruq does **not** accept half-releases.

If a feature cannot be finished properly, wait until it can.

---

## Testing Requirements

All contributions **must be tested**.

At minimum:
- Test in a real browser
- Test both:
  - `<maruq-element>`
  - legacy `.maruq` div usage (if applicable)
- Verify that existing behavior is not broken

If your change affects animation, timing, attributes, or events:
- Test multiple configurations
- Test edge cases (empty content, multiple children, etc.)

---

## Pull Request Requirements

Every pull request **must include**:

1. **What the change does**
   - Bug fix or feature
   - Short, clear description

2. **How to test it**
   - Step-by-step instructions
   - Example HTML if applicable

   Example:
   ```html
   <maruq-element behavior="alternate" speed="20">
     <span>Test content</span>
   </maruq-element>
   ```

3. Expected behavior
  - What should happen
  - What should not happen
