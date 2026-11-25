# Creative Assistant Front-end Prototype

## Repository and report details

- Public GitHub repository: **[TO BE REPLACED WITH YOUR REAL GITHUB URL]**
- README: `README.md` in the repository root
- Local commit prepared for upload: `f2221e3` (`Create interactive creative assistant prototype`)
- Reported commit/release after GitHub upload: **[replace with the GitHub commit hash or release tag]**

This project is a small front-end prototype for an intelligent creative-writing assistant. It demonstrates how the assistant can offer help while keeping the writer in control. The original draft is not changed automatically.

## How to run

Open `index.html` in a browser. No installation, API key or external service is needed.

Interaction path:

1. Click **Select passage**.
2. Choose a goal such as clarity, grammar or tone.
3. Click **Generate suggestion**.
4. Review the suggested rewrite.
5. Accept, dismiss or review the change.

## Current status

Implemented in this prototype:

- Select a passage and choose an improvement goal.
- Show an optional suggestion in a side panel.
- Explain why the suggestion was made.
- Let the user review the change before applying it.
- Keep the original draft unchanged until confirmation.
- Show a recovery message when no passage is selected.

Simulated or planned:

- The language-model generation is represented by a fixed example response.
- The text editor is a simplified demonstration rather than a complete writing application.
- Future work could connect a real model, add editable suggestion text and test the design with users.

## Development record

### Initial prototype

The first version focused on the main writing screen and a side panel. The purpose was to show the normal interaction: a user selects text, chooses a goal and requests help. The assistant was designed as an optional adviser rather than an automatic editor.

### Control and confirmation added

A review stage was added before changing the draft. This was an important design decision because accepting a suggestion should be an explicit user action. The interface also includes **Edit**, **Accept** and **Dismiss** choices so that the user can reject or adapt the output.

### Recovery behaviour added

A missing-selection state was added after checking the failure case. If the user has not selected a passage, the assistant explains what is needed and leaves the draft unchanged. This makes the system boundary clearer and avoids generating an unrelated suggestion.

### Checks completed

- Opened the HTML file in a browser.
- Tested the normal path from selection to suggestion and confirmation.
- Tested the dismiss path and checked that the draft remains unchanged.
- Tested the missing-selection path and checked that a clear instruction is shown.
- Checked that the layout remains usable on a smaller screen through the responsive CSS rule.
- Confirmed that the project contains no API key or private credential.

## AI assistance

AI tools were used for suggestions about the structure of the interface, wording of the interaction messages and code organisation. The resulting code was reviewed and adapted to match the project design. The author is responsible for checking the behaviour, screenshots, references and final repository history.

## Files

- `index.html` — HTML, CSS and JavaScript for the interactive prototype.
- `01_focused_workspace.png` — static view of the starting state.
- `02_suggestion_panel.png` — static view of the suggestion state.
- `03_review_and_confirm.png` — static view of the confirmation state.
- `04_recovery_message.png` — static view of the recovery state.
