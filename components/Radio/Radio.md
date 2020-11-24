Radios Buttons

- The `<fieldset>` surrounds the entire grouping of checkboxes or radio buttons. The `<legend>` provides a description for the grouping.
- Some assistive technology reads the legend text for each fieldset, so it should be brief and descriptive. This helps someone using assistive technology to understand the question they are answering with the group of checkboxes.
- WAI-ARIA provides a grouping role that functions similarly to `fieldset` and `legend`. You can add a wrapper element which has `role=group` to indicate that the contained elements are members of a group and the `aria-labelledby` attribute references the id for text that will serve as the label for the group.
  Note: This method is not supported by all browser/AT devices.
