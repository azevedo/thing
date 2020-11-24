Search

- Wrap search components in a parent element `role="search"` to increase their discoverability to assistive technologies
- Whenever possible, use the `label` element to explicitly associate text with form elements.
- Note that placeholders are not recognized by all assistive technologies, and thus are not adequate replacements for appropriate labeling. Additionally, assistive technologies that **do** announce placeholders will read the placeholder first, then the input's label and then type of input. So be sure not to repeat an input's label as its placeholder, otherwise it will be announced multiple times.
