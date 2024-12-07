
<h2 id="about-me">WCAG 2.2 Dolibarr app accessibility audit.</h2>

### Description:

This report details the findings of a comprehensive accessibility audit performed for the [Dolibarr](https://www.dolibarr.org/) Enterprise Resource Planning (ERP) web application, specifically tested on desktop PCs. The primary objective of this audit was to assess all core functionalities, including login, billing, product management, project management, and membership features, against the Web Content Accessibility Guidelines (WCAG) 2.2 Level A success criteria. This initial evaluation aims to establish a baseline for accessibility and identify areas for improvement. 


###  Login, registration, and reset password sections:

- **1. Keyboard Navigation**
  * **Issue:** Users experience a "keyboard trap" where navigation using the Tab key stops at certain points, preventing access to all interactive elements.
  * **WCAG 2.1.2 No Keyboard Trap** - Users can navigate through and away from any element using a keyboard without getting "trapped" in any part of the content.
  * **Possible Solution:** Ensure that all interactive elements are reachable using the keyboard and implement a cyclic navigation system, allowing users to return to the beginning after reaching the end of the focusable elements.

- **2. Form Field Descriptions**
  * **Issue:** Form fields lack descriptive labels and rely solely on icons, which may not be clear to all users.
  * **WCAG 1.3.1 Info and Relationships** - Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.
  * **Possible Solution:** Add descriptive labels for each form field to clearly indicate their purpose, ensuring that screen readers can identify them correctly.

- **3. ARIA Labels and Screen Reader Support**
  * **Issue:** There are no ARIA labels or appropriate attributes for form fields (e.g., login and password fields), making them inaccessible for screen readers.
  * **WCAG 4.1.2 Name, Role, Value** - For all user interface components (including form elements), the name and role can be programmatically determined.
  * **Possible Solution:** Implement ARIA attributes for form fields to provide additional context for screen reader users.

- **4. Clear Error Messages**
  * **Issue:** There are no clear and understandable error messages when users encounter issues.
  * **WCAG 3.3.1 Error Identification** - If an input error is detected and suggestions for correction are known, then the suggestions are provided to the user.
  * **Possible Solution:** Provide immediate feedback with clear error messages that are displayed near the relevant form fields, guiding users on how to correct their input.

- **5. Link Visibility**
  * **Issue:** Links are not visually distinguished (e.g., lack of underline) and have poor contrast against the background, making them hard to identify.
  * **WCAG 1.4.1 Use of Color** - Color is not used as the only means of conveying information or distinguishing a visual element.
  * **Possible Solution:** Ensure that links are visually distinct by underlining them and enhancing their color contrast against the background to meet accessibility standards.

- **6. Alt Text for Images**
  * **Issue:** Images do not have appropriate alt text descriptions, which is essential for users relying on screen readers.
  * **WCAG 1.1.1 Non-text Content** - All non-text content that is presented to the user has a text alternative that serves the equivalent purpose.
  * **Possible Solution:** Assign meaningful alt text to all images using the alt attribute to convey their purpose or content effectively.

- **7. Image-Based Buttons**
  * **Issue:** Buttons that consist solely of images (e.g., refresh button represented as a circular arrow) lack text alternatives.
  * **WCAG 4.1.2 Name, Role, Value** - For all user interface components (including buttons), the name can be programmatically determined.
  * **Possible Solution:** Add text alternatives for image-based buttons using ARIA attributes or provide visible text labels alongside the images.

- **8. Error Messages During Password Reset**
  * **Issue:** Lack of error messages during the password reset process leaves users unaware of issues they may encounter.
  * **WCAG 3.3.3 Error Suggestion** - If an input error is detected and suggestions for correction are known, then the suggestions are provided to the user.
  * **Possible Solution:** Implement error messages that inform users of any issues encountered during password reset attempts, providing guidance on how to resolve them.

- **9. Consistency in Error Messages**
  * **Issue:** Error messages during login are scattered throughout different areas of the page, leading to confusion for users trying to locate them.
  * **WCAG 3.2.4 Consistent Identification** - Components that have the same functionality within a single set of web pages are identified in the same way.
  * **Possible Solution:** Ensure that all error messages related to login are consistently placed near their respective fields and follow a uniform format across the application.



###  Main sections(billing, projects, members, payments etc.):

 
- **1. Keyboard Navigation**
  * **Issue:** Not all elements show focus after changes; some elements are inaccessible with keyboard navigation.
  * **WCAG 2.1.2 No Keyboard Trap** - Users can navigate through and away from any element using a keyboard without getting "trapped" in any part of the content.
  * **Possible Solution:** Ensure that all interactive elements are properly focused and accessible via keyboard navigation, and implement visual indicators for focused elements.

- **2. Menu Navigation**
  * **Issue:** Keyboard navigation primarily works for the menu; transitioning to specific elements on the board is impossible.
  * **WCAG 2.1.2 No Keyboard Trap** - Users can navigate through and away from any element using a keyboard without getting "trapped" in any part of the content.
  * **Possible Solution:** Review and adjust the focus order to ensure that users can navigate to all interactive elements in a logical sequence.

- **3. Checkbox Accessibility**
  * **Issue:** Checkboxes cannot be selected using Tab or Enter keys.
  * **WCAG 2.1.1 Keyboard Accessible** - All functionalities must be operable through a keyboard interface.
  * **Possible Solution:** Ensure that checkboxes are focusable and selectable using keyboard commands.

- **4. Arrow Key Navigation**
  * **Issue:** Navigation through menu items does not work using arrow keys.
  * **WCAG 2.4.1 Bypass Blocks** - Users should be able to navigate efficiently without excessive keystrokes.
  * **Possible Solution:** Implement arrow key functionality to allow users to navigate through menu items seamlessly.

- **5. Escape Key Functionality**
  * **Issue:** Users cannot close menus using the Escape key.
  * **WCAG 2.1.1 Keyboard Accessible** - All functionalities must be operable through a keyboard interface.
  * **Possible Solution:** Enable the Escape key to close menus, providing a consistent user experience.

- **6. Focus Visibility**
  * **Issue:** Focus on hover for buttons is very poorly visible/contrasted.
  * **WCAG 1.4.11 Non-text Contrast** - Ensure that user interface components have sufficient contrast against their background.
  * **Possible Solution:** Enhance the contrast of focus indicators for buttons to ensure they are clearly visible when focused.

- **7. Input Field Descriptions**
  * **Issue:** Input fields lack descriptions; only images are present.
  * **WCAG 1.3.1 Info and Relationships** - Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.
  * **Possible Solution:** Provide descriptive labels for all input fields, ensuring they are accessible to screen readers.

- **8. Screen Reader Compatibility**
  * **Issue:** Most input fields do not function correctly with screen readers.
  * **WCAG 4.1.2 Name, Role, Value** - For all user interface components (including form elements), the name and role can be programmatically determined.
  * **Possible Solution:** Ensure that all input fields have appropriate ARIA attributes and labels for compatibility with screen readers.

- **9. Link Understandability**
  * **Issue:** Lack of clarity regarding links (e.g., "List" and "List Entries" in one menu).
  * **WCAG 3.3.6 Identify Purpose** - The purpose of each link must be clear to users.
  * **Possible Solution:** Use descriptive link text that clearly indicates the purpose of each link.

- **10. Timeout Information**
  * **Issue:** No information or options for extending timeouts before they occur.
  * **WCAG 2.2.2 Pause, Stop, Hide** - Users should have control over time limits on content.
  * **Possible Solution:** Provide users with clear notifications about timeouts and options to extend them.

- **11. Hover Actions Indication**
  * **Issue:** Some elements have hover actions (small window popups) but lack visual indications that they are special (e.g., color or link).
  * **WCAG 4.1.2 Name, Role, Value** - For all user interface components (including form elements), the name and role can be programmatically determined.
  * **Possible Solution:** Clearly indicate interactive elements with visual cues (e.g., changes in color or underlining) to inform users of their functionality.

- **12. Popup Notification Timer**
  * **Issue:** Popup information notifications have a very short timer before they disappear.
  * **WCAG 2.2 Time Limits** - Users should have control over time limits on content unless there is a valid reason for them not to.
  * **Possible Solution:** Extend the duration of popup notifications or provide an option for users to pause or extend them.

- **13. Input Field Visibility**
  * **Issue:** Input fields only have a small line at the bottom, making it hard to see how big they are or if they are even input fields.
  * **WCAG 4.1.2 Name, Role, Value** - For all user interface components (including form elements), the name and role can be programmatically determined.
  * **Possible Solution:** Enhance the visibility of input fields by increasing their size and providing clearer borders.

- **14. Popup Error Closure**
  * **Issue:** Unable to close popup errors for input fields using a keyboard.
  * **WCAG 2.1.1 Keyboard Accessible** - All functionalities must be operable through a keyboard interface.
  * **Possible Solution:** Ensure that users can close popup error messages with keyboard commands, such as pressing the Escape key.

- **15. Inconsistency Across Pages**
  * **Issue:** Lack of consistency across pages; some elements refresh the page when selected from a list while others require clicking a "refresh" button.
  * **WCAG 3.2.4 Consistent Identification** - Components that have the same functionality within a single set of web pages are identified in the same way.
  * **Possible Solution:** Standardize interactions across all pages to ensure consistency in user experience.

- **16. Interaction with Charts**
   * **Issue:** Lack of interaction with charts using keyboard or screen readers.
   * **WCAG 2.4.3 Focus Order** - The focus order must be logical and intuitive; all interactive elements should be accessible via keyboard navigation.
   * **Possible Solution:** Implement keyboard accessibility for charts, allowing users to navigate and interact with chart data using assistive technologies.

- **17. Image-Based Buttons**
   * **Issue:** Buttons consist solely of images (e.g., refresh represented as a circular arrow), lacking text alternatives.
   * **WCAG 4.1.2 Name, Role, Value** - For all user interface components (including buttons), the name can be programmatically determined.
   * **Possible Solution:** Add text alternatives for image-based buttons using ARIA attributes or provide visible text labels alongside the images.

