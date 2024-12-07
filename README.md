
<h2 id="about-me">WCAG 2.2 Dolibarr app accessibility audit.</h2>

### Description:

This report details the findings of a comprehensive accessibility audit performed for the [Dolibarr](https://www.dolibarr.org/) Enterprise Resource Planning (ERP) web application, specifically tested on desktop PCs. The primary objective of this audit was to assess all core functionalities, including login, billing, product management, project management, and membership features, against the Web Content Accessibility Guidelines (WCAG) 2.2 Level A success criteria. This initial evaluation aims to establish a baseline for accessibility and identify areas for improvement. 


###  Login, registration, and reset password sections:

1. **Keyboard navigation**
   * **Issue:** Users experience a "keyboard trap" where navigation using the Tab key stops at certain points, preventing access to all interactive elements.
   * **WCAG 2.1.2 No keyboard trap** - Users can navigate through and away from any element using a keyboard without getting "trapped" in any part of the content.
   * **Possible solution:** Ensure that all interactive elements are reachable using the keyboard and implement a cyclic navigation system, allowing users to return to the beginning after reaching the end of the focusable elements.

2. **Form field descriptions**
   * **Issue:** Form fields lack descriptive labels and rely solely on icons, which may not be clear to all users.
   * **WCAG 1.3.1 Info and relationships** - Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.
   * **Possible solution:** Add descriptive labels for each form field to clearly indicate their purpose, ensuring that screen readers can identify them correctly.

3. **Aria labels and screen reader support**
   * **Issue:** There are no ARIA labels or appropriate attributes for form fields (e.g., login and password fields), making them inaccessible for screen readers.
   * **WCAG 4.1.2 Name, role, value** - For all user interface components (including form elements), the name and role can be programmatically determined.
   * **Possible solution:** Implement ARIA attributes for form fields to provide additional context for screen reader users.

4. **Clear error messages**
   * **Issue:** There are no clear and understandable error messages when users encounter issues.
   * **WCAG 3.3.1 Error identification** - If an input error is detected and suggestions for correction are known, then the suggestions are provided to the user.
   * **Possible solution:** Provide immediate feedback with clear error messages that are displayed near the relevant form fields, guiding users on how to correct their input.

5. **Link visibility**
   * **Issue:** Links are not visually distinguished (e.g., lack of underline) and have poor contrast against the background, making them hard to identify.
   * **WCAG 1.4.1 Use of color** - Color is not used as the only means of conveying information or distinguishing a visual element.
   * **Possible solution:** Ensure that links are visually distinct by underlining them and enhancing their color contrast against the background to meet accessibility standards.

6. **Alt text for images**
   * **Issue:** Images do not have appropriate alt text descriptions, which is essential for users relying on screen readers.
   * **WCAG 1.1.1 Non-text content** - All non-text content that is presented to the user has a text alternative that serves the equivalent purpose.
   * **Possible solution:** Assign meaningful alt text to all images using the alt attribute to convey their purpose or content effectively.

7. **Image-based buttons**
   * **Issue:** Buttons that consist solely of images (e.g., refresh button represented as a circular arrow) lack text alternatives.
   * **WCAG 4.1.2 Name, role, value** - For all user interface components (including buttons), the name can be programmatically determined.
   * **Possible solution:** Add text alternatives for image-based buttons using ARIA attributes or provide visible text labels alongside the images.

8. **Error messages during password reset**
   * **Issue:** Lack of error messages during the password reset process leaves users unaware of issues they may encounter.
   * **WCAG 3.3.3 Error suggestion** - If an input error is detected and suggestions for correction are known, then the suggestions are provided to the user.
   * **Possible solution:** Implement error messages that inform users of any issues encountered during password reset attempts, providing guidance on how to resolve them.

9. **Consistency in error messages**
   * **Issue:** Error messages during login are scattered throughout different areas of the page, leading to confusion for users trying to locate them.
   * **WCAG 3.2.4 Consistent identification** - Components that have the same functionality within a single set of web pages are identified in the same way.
   * **Possible solution:** Ensure that all error messages related to login are consistently placed near their respective fields and follow a uniform format across the application.



###  Main sections(billing, projects, members, payments etc.):

1. **Keyboard navigation**
   * **Issue:** Not all elements show focus after changes; some elements are inaccessible with keyboard navigation.
   * **WCAG 2.1.2 No keyboard trap** - Users can navigate through and away from any element using a keyboard without getting "trapped" in any part of the content.
   * **Possible solution:** Ensure that all interactive elements are properly focused and accessible via keyboard navigation, and implement visual indicators for focused elements.

2. **Menu navigation**
   * **Issue:** Keyboard navigation primarily works for the menu; transitioning to specific elements on the board is impossible.
   * **WCAG 2.1.2 No keyboard trap** - Users can navigate through and away from any element using a keyboard without getting "trapped" in any part of the content.
   * **Possible solution:** Review and adjust the focus order to ensure that users can navigate to all interactive elements in a logical sequence.

3. **Checkbox accessibility**
   * **Issue:** Checkboxes cannot be selected using Tab or Enter keys.
   * **WCAG 2.1.1 Keyboard accessible** - All functionalities must be operable through a keyboard interface.
   * **Possible solution:** Ensure that checkboxes are focusable and selectable using keyboard commands.

4. **Arrow key navigation**
   * **Issue:** Navigation through menu items does not work using arrow keys.
   * **WCAG 2.4.1 Bypass blocks** - Users should be able to navigate efficiently without excessive keystrokes.
   * **Possible solution:** Implement arrow key functionality to allow users to navigate through menu items seamlessly.

5. **Escape key functionality**
   * **Issue:** Users cannot close menus using the Escape key.
   * **WCAG 2.1.1 Keyboard accessible** - All functionalities must be operable through a keyboard interface.
   * **Possible solution:** Enable the Escape key to close menus, providing a consistent user experience.

6. **Focus visibility**
   * **Issue:** Focus on hover for buttons is very poorly visible/contrasted.
   * **WCAG 1.4.11 Non-text contrast** - Ensure that user interface components have sufficient contrast against their background.
   * **Possible solution:** Enhance the contrast of focus indicators for buttons to ensure they are clearly visible when focused.

7. **Input field descriptions**
   * **Issue:** Input fields lack descriptions; only images are present.
   * **WCAG 1.3.1 Info and relationships** - Information, structure, and relationships conveyed through presentation can be programmatically determined or are available in text.
   * **Possible solution:** Provide descriptive labels for all input fields, ensuring they are accessible to screen readers.

8. **Screen reader compatibility**
   * **Issue:** Most input fields do not function correctly with screen readers.
   * **WCAG 4.1.2 Name, role, value** - For all user interface components (including form elements), the name and role can be programmatically determined.
   * **Possible solution:** Ensure that all input fields have appropriate ARIA attributes and labels for compatibility with screen readers.

9. **Link understandability**
   * **Issue:** Lack of clarity regarding links (e.g., "List" and "List Entries" in one menu).
   * **WCAG 3.3.6 Identify purpose** - The purpose of each link must be clear to users.
   * **Possible solution:** Use descriptive link text that clearly indicates the purpose of each link.

10. **Timeout information**
    * **Issue:** No information or options for extending timeouts before they occur.
    * **WCAG 2.2.2 Pause, stop, hide** - Users should have control over time limits on content.
    * **Possible solution:** Provide users with clear notifications about timeouts and options to extend them.

11. **Hover actions indication**
    * **Issue:** Some elements have hover actions (small window popups) but lack visual indications that they are special (e.g., color or link).
    * **WCAG 4.1.2 Name, role, value** - For all user interface components (including form elements), the name and role can be programmatically determined.
    * **Possible solution:** Clearly indicate interactive elements with visual cues (e.g., changes in color or underlining) to inform users of their functionality.

12. **Popup notification timer**
    * **Issue:** Popup information notifications have a very short timer before they disappear.
    * **WCAG 2.2 Time limits** - Users should have control over time limits on content unless there is a valid reason for them not to.
    * **Possible solution:** Extend the duration of popup notifications or provide an option for users to pause or extend them.

13. **Input field visibility**
    * **Issue:** Input fields only have a small line at the bottom, making it hard to see how big they are or if they are even input fields.
    * **WCAG 4.1.2 Name, role, value** - For all user interface components (including form elements), the name and role can be programmatically determined.
    * **Possible solution:** Enhance the visibility of input fields by increasing their size and providing clearer borders.

14. **Popup error closure**
    * **Issue:** Unable to close popup errors for input fields using a keyboard.
    * **WCAG 2.1.1 Keyboard accessible** - All functionalities must be operable through a keyboard interface.
    * **Possible solution:** Ensure that users can close popup error messages with keyboard commands, such as pressing the Escape key.

15. **Inconsistency across pages**
    * **Issue:** Lack of consistency across pages; some elements refresh the page when selected from a list while others require clicking a "refresh" button.
    * **WCAG 3.2.4 Consistent identification** - Components that have the same functionality within a single set of web pages are identified in the same way.
    * **Possible solution:** Standardize interactions across all pages to ensure consistency in user experience.

16. **Interaction with charts**
    * **Issue:** Lack of interaction with charts using keyboard or screen readers.
    * **WCAG 2.4.3 Focus order** - The focus order must be logical and intuitive; all interactive elements should be accessible via keyboard navigation.
    * **Possible solution:** Implement keyboard accessibility for charts, allowing users to navigate and interact with chart data using assistive technologies.

17. **Image-based buttons**
    * **Issue:** Buttons consist solely of images (e.g., refresh represented as a circular arrow), lacking text alternatives.
    * **WCAG 4.1.2 Name, role, value** - For all user interface components (including buttons), the name can be programmatically determined.
    * **Possible solution:** Add text alternatives for image-based buttons using ARIA attributes or provide visible text labels alongside the images.

 
### Accessibility audit summary for the DoliBarr:

This accessibility audit has identified several critical issues within the web application, focusing on compliance with the Web Content Accessibility Guidelines (WCAG) 2.2. The following summary encapsulates the key findings and recommendations based on the assessment:

1. **Keyboard navigation**: Users experience "keyboard traps" where navigation using the Tab key stops at certain points, preventing access to all interactive elements. It is essential to ensure that all interactive elements are reachable via keyboard and that a cyclic navigation system is implemented.

2. **Menu navigation**: Keyboard navigation primarily works for the menu, but transitioning to specific elements on the board is impossible. The focus order must be logical, allowing users to navigate through all interactive elements seamlessly.

3. **Checkbox accessibility**: Checkboxes are not selectable using Tab or Enter keys, which hinders usability for keyboard users. Ensuring that checkboxes are focusable and selectable is crucial.

4. **Arrow key navigation**: Navigation through menu items does not function with arrow keys, making it difficult for users to explore options efficiently. Implementing arrow key functionality will enhance user experience.

5. **Escape key functionality**: Users cannot close menus using the Escape key, which limits their ability to navigate effectively. Enabling this functionality will provide a more intuitive user experience.

6. **Focus visibility**: The focus on hover for buttons is poorly visible and lacks sufficient contrast. Enhancing focus indicators will help users identify which element is currently active.

7. **Input field descriptions**: Many input fields lack descriptive labels, relying solely on images, which may not be clear to all users. Providing clear labels for input fields is necessary for accessibility.

8. **Screen reader compatibility**: Most input fields do not function correctly with screen readers, making it challenging for visually impaired users to interact with the application. Ensuring that all input fields have appropriate ARIA attributes and labels is essential.

9. **Link understandability**: Links lack clarity regarding their purpose, which can confuse users navigating the site. Using descriptive link text will improve comprehension.

10. **Timeout information**: There is no information or options for extending timeouts before they occur, which can disrupt user tasks. Providing notifications about timeouts and options to extend them is important.

11. **Hover actions indication**: Some elements have hover actions (e.g., small window popups) but lack visual indications that they are interactive. Clear visual cues should be implemented to inform users of these functionalities.

12. **Popup notification timer**: Popup notifications disappear too quickly, leaving users without adequate time to read them. Extending the duration or providing options to pause notifications will enhance usability.

13. **Input field visibility**: Input fields are not clearly defined, making it difficult for users to identify them as interactive elements. Improving their visibility by increasing size and providing clearer borders is recommended.

14. **Popup error closure**: Users are unable to close popup error messages using a keyboard, which limits accessibility for keyboard-only users. Ensuring that these popups can be closed with keyboard commands is necessary.

15. **Inconsistency across pages**: There is a lack of consistency in interactions across pages; some elements refresh the page while others require clicking a "refresh" button. Standardizing these interactions will improve user experience.

16. **Interaction with charts**: The application lacks keyboard accessibility for charts, preventing users from interacting with data effectively. Implementing keyboard navigation for chart elements will enhance accessibility.

17. **Image-based buttons**: Buttons consisting solely of images lack text alternatives, making them inaccessible to screen readers. Adding text alternatives or visible labels alongside these buttons is essential.

### Conclusion

Addressing these identified issues will significantly enhance the accessibility of the web application for individuals with disabilities, ensuring compliance with WCAG 2.2 standards and fostering an inclusive digital environment. Implementing the recommended changes will not only improve usability but also create a more satisfying experience for all users interacting with the application.

