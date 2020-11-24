Text Inputs and Textareas

- Keep it simple - screen readers do not support multiple labels that are linked to the same form element.
- Use labels for every input. If using the `for=""` and `id=""` values, make them match, also remember that IDs must be unique on each page, only one label can be associated to each unique form element.
- Make required fields obvious by using an indicator - border color change, asterisk, description text, etc.
- Fields with error validation should have `aria-describedby` to insure that the associated field level error message is read by assistive technology. If the error message has an `id="my-error-message"`, then the input should have `aria-describedby="my-error-message"`.
