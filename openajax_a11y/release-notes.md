Version 1.2 Overview
=============================

* Updated Widget rule references to use ARIA 1.2 spec, ARIA Authoring Practices, MDN resources for ARIA and Web Foundation references for ARIA.
* Updated references to remove references to iCITA website
* Updated references to include W3C WAI Web Accessibility Tutorials
* Updated regression tests based on ARIA 1.2 changes
* Fixed bugs in CONTROL 11 rule on unique names for submit and reset buttons when there are multiple forms
* Fixed bugs in WIDGET 7 rule on owned elements
* Fixed bugs in WIDGET 8 rule related to being owned by another element
* Fixed bugs in WIDGET 9 rule related to having required parent roles
* Fixed bugs in WIDGET 10 rule related to range control attributes
* Changed WIDGET 13 to test for name prohibitied requirement (from prohibiting any ARIA markup and this original rule was not included in any rulesets)
* Added HTML 3 rule to support W3C ARIA in HTML specification
* Added WIDGET 15 rule to test for use of deprecated ARIA states and properties on selected roles
* Added WIDGET 16 rule to raise awareness of web components being user on a page and the need for manual checking


Version 1.1.2 Overview
=============================

toCSV and toHTML
-----
* FILE: evaluation_result.js
* FILE: evaluation_export.js
* FILE: element_result.js
* FILES: nls/en-US/ directory

* Moved toCSV and toHTML methods from evaluation_result.js to evaluation_export.js
* Updated links from ARIA 1.0 references to ARIA 1.1 references
* Added getAccessibleName to element result object
* Cleaned source code files to remove DOS line breaks, tabs and spaces at the ends of lines

Version 1.1.1 Overview
=============================

toCSV and toHTML
-----
* FILE: evaluation_result.js
* FILE: element_result.js
* FILE: cache_dom_element.js

* Added toCSV function for exporting evaluation results to a CSV format
* Added toHTML function for exporting evaluation results to a HTML format
* This included creating a DOM element property text_content

Landmark Rule NLS References
----------------------------
* FILE: rules_nls_landmarks.js

* Fixed some references to the wrong HTML elements in INFORMATIONAL_LINKS section of several rules


Version 1.1.0 Overview
=============================

Computed Style
---------------
* FILE: cache_style.js

* Added "rgba(0, 0, 0, 0)" as a definition of a transparent background-color

HTML
----
* FILE: wcag20_aria_strict_ruleset.js (from Revision 2,926)
* FILE: wcag20_aria_transitional_ruleset.js (from Revision 2,926)

### HTML 1: Verify semantics @b@ and @i@ elements
* Removed rule from rulesets


KEYBOARD
--------
* FILE: rules_keyboard.js (from Revision 2,926)
* FILE: rules_nls_keyboard.js (from Revision 2,926)

### Keyboard 1: Widgets must have keyboard support required by their roles
* Has been changed to only generate manual checks


LAYOUT
------
* FILE: rules_layout.js (from Revision 2,926)
* FILE: rules_nls_layout.js (from Revision 2,926)

### Layout 1: Layout tables must have meaningful sequence
* Updated purpose messaging to help make rule requirements clearer

### Layout 3: Verify aria-flowto supports reading order
* Added new rule


LANDMARK
--------
* FILE: cache_headings_landmark.js (from Revision 2,926)

### Landmark 2: All content must be contained in landmarks
* Updated he cached array of elements with renderable content to not include imput[type="hidden"]


WIDGET
------
* FILE: rules_widget.js (from Revision 2,926)
* FILE: rules_nls_widget.js (from Revision 2,926)

### Widget 14: Verify live region is appropriate
* Added new rule, included



Version 1.0.0 Overview
=============================
* Changed version from 1.0.0-beta.6 to 1.0.0
* Updated copyright information to 2011-2017

Version 1.0.0-beta.6 Overview
=============================

KEYBOARD
--------
* FILE: rules_keyboard.js (from Revision 2891)
* FILE: rules_nls_keyboard.js (from Revision 2869)

### KEYBOARD 1: Widgets must have keyboard support required by their roles
* Updated the rule to remove any pass and improved rule logic
* Updated rule messaging to improve information about rule and rule results


LANDMARKS
---------
* FILE: cache_nls_landmarks.js (from Revision 2868)

### LANDMARK 4: banner landmark: identifies branding content
* Updated summary
* Updated technique 1

### LANDMARK 6: contentinfo landmark: identifies admin content
* Updated summary
* Updated technique 1

### LANDMARK 9: banner landmark: restrictions
* Updated technique 1

### LANDMARK 10: navigation landmark: restrictions
* Updated technique 1

### LANDMARK 13: contentinfo landmark: restrictions
* Updated technique 1


WIDGETS
-------
* FILE: rules_nls_widget.js (from Revision 2,869)
* FILE: aria.js (from Revision 2,744)
* FILE: cache_dom_elements.js (from Revision 2,867)
* FILE: cache_dom_element.js (from Revision 2875)
* FILE: cache_dom_traversal.js (from Revision 2848)

### Added support events on the document object
* Modified function "OpenAjax.a11y.cache.DOMCache.prototype.updateDOMElements" in cache_dom_traversal.js to pass in the document object to the DOMElement constructor
* Modified function "OpenAjax.a11y.cache.DOMElement.prototype.EnumerateFirefoxEvents" in cache_dom_element.js to add event information to the body element
* Added support for identifying document object based events, which appears to be how JQuery.js adds some events effects the following ruls:
* Widget 11: Keyboard/Mouse/drag events must have roles
* Keyboard 1:  Widgets must support keyboard

### Widget 11: Elements with event handlers must have roles
* Updated rule result messages for failure and manual checks

### Added roles to support ARIA 1.1 specfication
* cell
* figure
* none
* searchbox
* switch
* table
* term
* text

### Added properties and states to support ARIA 1.1 specfication
* aria-colcount
* aria-colindex
* aria-colspan
* aria-current
* aria-details
* aria-errormessage
* aria-modal
* aria-placeholder
* aria-roledescription
* aria-rowcount
* aria-rowindex
* aria-rowspan
* Added "type=positive" to "propertyDataTypes" indicate integer values that need to be greater than 0 (in aria.js)
* Added switch to test for "type=positive" in value validation (in cache_dom_element.js)

### Rules using this aria.js information on roles, properties and states
* Widget 3: role must be valid
* Widget 4: ARIA values must be valid
* Widget 5: ARIA attribute must be defined
* Widget 6: Widgets must have properties
* Widget 7: Widgets must have child roles
* Widget 8: Widgets must have parent


Version 1.0.0-beta.5 Overview
=============================

LANDMARKS
---------
* FILE: cache_nls_landmarks.js
* FILE: rules_landmarks.js

### LANDMARK 9: BANNER landmark: restrictions
* Updated messaging to improve feedback to users on banner landmark restrictions

### LANDMARK 10: NAVIGATION landmark: restrictions
* Updated messaging to improve feedback to users on navigation landmark restrictions

### LANDMARK 19: COMPLEMENTARY landmark: must be top level
* Moved LANDMARK_13 to new LANDMARK_19 and added to rulesets
* Changed the COMPLEMENTARY landmark to "top-level landmark" from "top-level landmark or a child of a MAIN landmark".

### LANDMARK 13: CONTENTINFO landmark: restrictions
* Added new LANDMARK_13 for contentinfo landmark restrictions (similar to banner restrictions rule)

### Minor updates "top level" landmark messages
* Landmark 8:  BANNER landmark: must be top-level
* Landmark 11: MAIN landmark: must be top-level
* Landmark 12: CONTENTINFO landmark: must be top-level
* Landmark 13: COMPLEMENTARY landmark: must be top-level


STYLES/CONTENT
--------------
* FILE: cache_nls_color.js
* FILE: rules_color.js

### COLOR 1: Text must exceed CCR of 4.5
* Updated messaging to have separate messaging for large text


IMAGES
------
* FILE: cache_nls_images.js
* FILE: rules_images.js

### IMAGE 6: Long description for complex images
* Updated to test for TITLE attribute being a sub-string of ALT attribute
* Added new message for TITLE attribute being a sub-string of ALT attribute


FORMS
-----
* FILE: cache_nls_controls.js
* FILE: rules_controls.js
* FILE: cache_nls_roles.js
* FILE: rules_roles.js

### CONTROL 3: Radio buttons must have grouping label
* Updated messaging to explain why grouping labels are different than standard labels

### CONTROL 6: LABEL must reference control
* Updated rule to report a manual check if more than one way is being used to label a form control

### CONTROL 9: Verify TITLE is label
* Updated messaging to make it clearer title is not a preferred labeling technique

### ROLE 13: SELECT element role semantics
* Added new ROLE_13 rule for select element role semantics

### ROLE 14: TEXTAREA element role semantics
* Added new ROLE_14 rule for textarea element role semantics


KEYBOARD SUPPORT
----------------
* FILE: cache_nls_focus.js
* FILE: rules_focus.js

### FOCUS 4: SELECT must not change context
* Updated primary success criterion to 3.2.2


WIDGETS/SCRIPTS
---------------
* FILE: cache_nls_widgets.js
* FILE: rules_widgets.js

### WIDGET 11
* Updated rule to result in manual checks for widget roles and improved definition and messaging

RULE INFORMATION FORMATTING CONSISTENCY
----------------------------------
* rules_nls_audio.js
* rules_nls_bypass.js
* rules_nls_color.js
* rules_nls_common.js
* rules_nls_error_feedback.js
* rules_nls_focus.js
* rules_nls_form_controls.js
* rules_nls_frames.js
* rules_nls_headings.js
* rules_nls_html.js
* rules_nls_images.js
* rules_nls_keyboard.js
* rules_nls_landmarks.js
* rules_nls_language.js
* rules_nls_layout.js
* rules_nls_links.js
* rules_nls_lists.js
* rules_nls_navigation.js
* rules_nls_reading_order.js
* rules_nls_resize.js
* rules_nls_roles.js
* rules_nls_sensory.js
* rules_nls_tables.js
* rules_nls_timing.js
* rules_nls_title.js
* rules_nls_video.js
* rules_nls_widgets.js

### Edited files for periods at the end of definitions, result messages, purpose and techniques

HEADINGS AND LANDMARKS IDENTIFICATION
-------------------------------------
* File: cache_headings_landmarks.js

### Identification of default landmark roles HTML5 elements
* Updated identification of a FORM element with an accessible name defining a FORM landmark
* Updated identification of a HEADER element defining a BANNER landmark
* Updated identification of a FOOTER element defining a CONTENTINFO landmark


EVALUATION RESULTS
------------------
* File: evaluation_result.js

### Fixed JSON export bug for element identifiers for images


UTILS
-----
* File: cache_util.js

### Fixed bug in normalizeSpace utility to trimm off trailing spaces from a string, and affects the following rules:
* Landmark 17: Landmarks must be uniquely identifiable
* Heading 3: Sibling headings must be unique
* Link 2: Link text must be unique
* Table 4: Data tables must have unique names
* Control 10: Labels must be unique
* Control 11  submit and reset buttons must be unique


Version 1.0.0-beta.4
--------------------
### Overview
* Fixed json formatting issue for element results
* Change DOM node processing to discard input[type=“hidden”], since there are no accessibility techniques or issues with this element
* Changed OpenAjax.a11y.util.normalizeSpace to filter out any control characters and any character greater than ‘~’, for compatibility with fad-util
* Added class and id information to element results



Version 1.0.0-beta.3
--------------------
### Rule Additions and Changes
* Frame 1: frame must have accessible name (new)
* Frame 2: iframe must have accessible name (new)
* Image 1: Images must have alt text (Not new, but extensively modified)
* Image 2: Alt text must summarize purpose (Not new, but extensively modified)
* Image 5: Verify image is decorative (Not new, but extensively modified)
* Image 6: Long description for complex images (Not new, but extensively modified)
* Image 7: Use MathML for mathematical expressions (new)
* Keyboard 2: Behaviors supported by keyboard (Not new, but extensively modified)
* Landmark 2: All content must be contained in landmarks (Not new, but extensively modified)
* Landmark 16: region landmark must have accessible name (Not new, but extensively modified)
* Landmark 17: Landmarks must be uniquely identifiable (Not new, but extensively modified)
* Landmark 18: Landmarks must identify content regions (Not new, but extensively modified)
* Link 1: Link text must be descriptive (extensively modified)
* List 1: Use list markup semantically (new)
* List 2: Labeling lists (new)
* Order 1: Reading order: CSS positioning (new)

### Overview
* Changed heading rule 5 to be required in ARIA + HTML5 ruleset
* Fixed grammar in summaries for VIDEO 8 and 9 rules
* Changed heading rule 5 to have primary relationship with WCAG SC 1.3.1 (was 2.4.6)
* Updated visibility calculation to include test on the height of the text (e.g. text with 0 height does not need to be tested for color contrast)
* Moved role semantic restriction rules from landmark to style/content rule category
* Added rules for frame and iframe having accessible names
* Updated copyright information in some files to use 2011-2017
* Fixed bug in incorrectly identifying header and footer elements inside sectioning elements as landmarks
* Updated landmark messaging to improve the identification of techniques to create landmarks
* Added landmark 19 rule: landmarks must be descriptive of the sections they identify
* Updated widget rule 1 to use "label" instead of "accessible name", reference WCAG 2.0 ARAI techniques and element messaging uses XXX element with YYY widget role
* Added widget rule 12 to verify labels for elements with widget roles are descriptive
* Fixed Table Rule 1 to also allow the use of the headers attribute to define headers in simple data tables
* Reimplementation of Keyboard Rule 3 on page being keyboard operable, basically identifying any elements with events or tab index values other than 0
* Updated keyboard rule 1 to correctly test for the potential of keyboard event handlers on owned children
* Removed keyboard 2 rule since HTML5 requires a default value of tabindex=-1, basically any element can receive focus
* Moved keyboard rule 3 -> keyboard rule 2 since keyboard rule 2 was removed
* Moved keyboard rule 4 -> keyboard rule 3 since keyboard rule 3 was removed
* Added list rule 1 for using semantically meaningful list markup on the page
* Added list rule 2 about manual tests for labeling a list container
* Added reading order rule 1 to evaluation library
* Added 'area' property to computed styles that maybe be used in future rules, add using Math.round on computed styles for height and width properties
* Updated media element and textarea element toString function
* Updated toString function for image objects to include "offscreen" in addition to "hidden" for the additional image information

Version 0.9.9.1a
----------------
### Overview
* Updated HTML5 element role restriction rules not to result in PASS, only FAIL or MANUAL checks
* Updated HTML5 element role restriction rule messaging to emphasize the correct us of
  semantics and overriding default HTML5 sectioning rules
* Updated data table rule (TABLE 2) to support complex data tables from rules
* Updated audio NLS to include element level HIDDEN message for audio rules 2 and 3
* In aria strict ruleset changed heading 5 rule to be recommended (header nesting page) to recommended and changed heading rule 8 to required (header nesting in landmarks) to be required.
* Added form element to Landmark rule 18 landmark role restrictions
* Fixed messaging bugs with LANDMARK 8 rule
* Added feature to detect HTML DOM, if not HTML DOM the evaluation function will not execute (in 0.9.9.1a patch)
* Fixed bug for marking 'a' elements as having a default onclick event (in 0.9.9.1a patch)


Version 0.9.9
-------------

### Overview
* Removed "typeof X === 'object'" tests, since null evaluates as an 'object' (e.g. ~24 instances)
* Fixed bug in calculating accessible name when LABEL elements are empty and multiple LABEL references
* Added "landmark" property to represent the computed landmark value for an element
* Updated all landmark rules to use the computed "landmark" value instead or role value
  and heading rules that are dependent on landmark information
* Support HTML5 sectioning elements for their default landmark roles in landmark rules
* Improved consistency of landmark rule messaging
* Fixed data table naming rule (TABLE_2) that was only testing simple data tables, now also
  tests complex data tables


Version 0.9.8.3
---------------

### Overview
* Changed NAVIGATION 2 in HTML4 ruleset from required to recommended rule
* Included NAVIGATION 4 in HTML4 ruleset as a recommended rule
* Updated NAVIGATION 4 to be not applicable if no landmarks are found on the page
* Updated HEADING 5 to not fail empty headers, just ignore for the purpose of structure
* Added ERROR 5 rule to prevent errors for legal and financial transactions

Version 0.9.8.2
---------------

### Overview
* Fixed bug with CONTROL 10 rule to allow TAB and associated TABPANEL to share the same accessible name
* Fixed bug with NAVIGATION 2 to only be applicable when there are landmarks on the page,
  does not fail a page for missing MAIN landmark
* Included NAVIGATION 2 in HTML4 ruleset as a recommended rule
* Removed heading rules 7 and 8 from HTML4 ruleset
* Updated "Skipto" messaging to separate use of id and name attributes as target, and discourage use of name attribute
* Changed TABLE 5 to recommended in HTML4 ruleset, since it requires the use of ARIA
* Updated TABLE 3 to only require a manual check for adding a summary to simple and complex data tables


Version 0.9.8.1
---------------

### Overview
* Fixed undeclared variable in LANDMARK RULE 3
* Fixed undefined function error with Link Cache calculation by testing for type String
* Fixed bug with button element accessible name calculation, now supports aria-label, aria-labelledby and title attributes
* Added accessible name to "toString" functions for form controls and widgets, to harmonize with "a" element "toString" functions
* Fixed alt text bug in generating accessible name for form control in function "getElementTextContent"
* Improved accessible name calculation for form controls inside fieldset/legend elements
* Updated "toString" function for link cache elements

Version 0.9.8
-------------

### Overview
* Added BYPASS_1 rule that supports "SkipTo" script and internal linking
* Updated table cache to provide better support for CAPTION element and SUMMARY attribute
  for naming and describing tables and table titling rules now use this information in
  rule evaluation and results
* Updated TABLE_5 to result in manual check for tables that contain only one row or column
* Removed the concept of "large" data table from library and rules
* Added two rules to table data rules for:
  * Split simple and complex data table heading requirements out of TABLE 1 rule
  * TABLE 1 is just about headings for simple data tables and updated messaging to reflect changes
  * New TABLE 7 is just about headings for complex data tables
  * New TABLE 8 is about accessible name beting different from accesible description
* Updated for CONTROL_3 to include title attribute as another group titling technqiue
* Updated labeling references for form control labeling rules to include references to
  ARIA labeling specifications
* Fixed bug with name calculation for links includes TITLE attribute
* Updated LANDMARK_3 rule to be not applicable if no or less than 4 links found on a page
* Updated CONTROL_5 to fail form controls with duplicate IDs when they are hidden, improved messaging

### Change details
1. Fixed bug with link accessible name calculation, now supports the TITLE attribute

2. Added BYPASS_1 that evaluates for "SkipTo" script or an internal link to main content.
   The internal link must be the first or second link on a page

3. Updated TABLE 3 and 4 rules to improve the support for calculating the accessible name
   (i.e. caption) and accessible description (i.e summary)


Version 0.9.7.4
---------------

### Overview
* Removed basic ruleset
* updated the title and descriptions of the remaining 2 rulesets;
* removed Title rule 2
* fixed bugs with rules and updated test cases

### Change details

1. Edited Widget Rule 11 target resource information

2. Edited Widget Rule 11 to include identification of interactive elements (a, input, select, textarea)

3. fixed bug in Widget rule 11 to ignore 'objet', 'embed' and 'applet' elements

4. Fixed bug in initEvents menthod

5. Improved code for initializing event information, by adding an initEvents method to the DOMElement object

6. Fixed bug in widget rule 2 for elements with on click events to have role, removed requirements for tabIndex, because untestable and updated test suite

7. Fixed bug in inline event detection, missed initializing some properties, now properties are initialized

8. Fixed bug in DOM element function for determining if a numerical value was valid

9. Fixed Role Restriction Rule 10, it was not catching H1-H6 that had role values

10. Added support for identifying inline events, these are most useful for the test suite that does not have the capability to test events added through addEventListener

11. Removed Title Rule 2 from rulesets, the rule has problems when more than 2 H1 elements

12. Updated Keyboard Rule 1 to support A element being overridden by widget roles that can use onClickEvents, A element has keyboard support for on click events

13. Updated color rule 2 to fix message reference to PAGE_MC_1 message

14. Updated NAVIGATION 1, 3 and 5 and Heading 1 rules to use just "page" to identify the page result message(s)

15. Updated TITLE rule 2, it had a number of issues including not being very forgiving for more than 2 visible H1 elements

16. updated messaging for checking title with up to 2 H1 elements for consistency of H1 content with TITLE content

17. If more than 2 visible H1 elements the rule returns a manual check for verifying the H1 elements identify and describe a major section of the page, this clause though creates a mismatch with the rule summary and description

18. Updated control rule 10 to ignore duplicate label testing for controls with no label

19. Fixed bug in IMAGE rule 4 updated N_F to N_MC in rule results message

20. Fixed image rules that did not have HIDDEN_S and HIDDEN_P messages in the NLS

21. Fixed LINK 4 bug reference a bad variable

22. Fixed FOCUS_5 rule reference to undefined de.role property

23. Updated title and descriptions for both rulesets

24. Updated rule mappings for conditional landmark related rules to be recommended in HTML4 Legacy ruleset

25. Changed FOCUS 2 to be part of Keyboard Support rule category

26. Changed NAVIGATION 3 and 5 to be required in both rulesets

27. Moved HEADING 6 to be recommended and updated descriptions of rulesets

28. Removed Basic ruleset
