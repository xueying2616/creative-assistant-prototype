# Creative Assistant Front-end Prototype

## Repository and report details

- Public GitHub repository: https://github.com/xueying2616/creative-assistant-prototype
- README link: https://github.com/xueying2616/creative-assistant-prototype/blob/main/README.md
- Current GitHub commit: 56247838d8a35e4149eaceea889014b3e95ce076 (5624783)
- Project scope: IIS Lab2 and Lab3 creative-writing assistant prototype

This project explores a writing assistant that offers one optional suggestion without taking control of the writer's draft. The user selects a passage and chooses a goal such as clarity, grammar or tone. The assistant checks the request, shows one possible rewrite and waits for the user to edit, accept or dismiss it.

## How to run

Open index.html in a modern browser. No installation, API key or external service is required.

Normal path:

1. Select the first sentence in the draft.
2. Choose a goal.
3. Continue to review the selected text and goal.
4. Generate one optional suggestion.
5. Edit, review, accept or dismiss it.

The original text remains unchanged until Accept and replace is selected.

## Status and boundaries

Implemented in this prototype:

- A focused draft workspace with a non-blocking assistant panel.
- A selected passage and a clear improvement goal.
- An input-confirmation step before generation.
- A simulated suggestion with a short explanation.
- Editable suggestion text and a final review step.
- Accept and dismiss controls, with the original unchanged before acceptance.
- A recovery path when the user cancels or has not selected text.

Simulated or planned:

- The language-model response is a fixed local example. There is no live model call.
- The editor uses one demonstration passage rather than a full writing application.
- Future work could add real text selection, a model adapter, session-level preference learning and a user study.

## Development record

The project began with the Lab2 interaction model: the assistant senses a possible need for help, presents one optional suggestion in a side panel and lets the writer accept, edit, ignore or dismiss it. A secondary-user check led to clearer labels such as Optional suggestion and Why this suggestion?.

The Lab3 specification then narrowed the request. The user selects text and chooses clarity, grammar or tone. The system sends only the selected text, a small surrounding context and the goal to the model boundary. Before generation, the user can check the request. This was added after the vague-request test case showed that Make it better should not directly trigger generation.

The prototype was implemented as one self-contained HTML file. The interface was reviewed through the normal flow, the edit and dismiss paths, and the unchanged-draft condition. The layout was also checked at a smaller viewport. Static screenshots in the repository document the main states.

## AI assistance and authorship

AI tools were used for suggestions about interface wording, state organisation and test cases. The suggestions were reviewed and adapted to the Lab2/Lab3 design. The final project decisions, scope boundaries, checks and submission materials remain the author's responsibility. No private credentials or API keys are included.

## Files

- index.html — self-contained HTML, CSS and JavaScript prototype.
- 01_focused_workspace.png — starting workspace.
- 02_suggestion_panel.png — optional suggestion state.
- 03_review_and_confirm.png — review and confirmation state.
- 04_recovery_message.png — recovery state.
