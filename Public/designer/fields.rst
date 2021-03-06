Fields
==================================================

.. contents:: Contents:
 :local:
 :depth: 1

General Info
-------------------------------------------------------------
Fields are primary input elements on the Form. 
Fields are being filled by the user and store their data in user's session storage and once the form is submitter, their contents are handled by Microsoft Flow.

Basic properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Most fields have following settings:

SETTINGS

.. list-table::
    :widths: 10 40

    *   - InternalName
        - Setting utilized by many elements. InternalName is similar to ID, it's a unique identifier for the element.
    *   - Required
        - Select if the field is required to submit the form or not.
    *   - Orientation
        - Select if the title is displayed on the left from field or on top of it, to the left. Might automatically switch if not enough space.
    *   - CSS Class
        - Give CSS Class to the element, in order to apply JavaScript or CSS Style to it. Can give multiple classes separated by spaces to one element.
    *   - Style
        - Allows you to give specific element certain style. No need to use selectors, simply add CSS rules to this setting.

TITLE

.. list-table::
    :widths: 10 40

    *   - Text
        - Select the displayed title for the field.
    *   - Visible
        - Select if the title is visible or not.
    *   - Width
        - Select the width of the title.
    *   - FontSize
        - Select font size of the title.
    *   - FontColor
        - Select font color of the title. Can be either selected or manually entered.
    *   - FontStyle
        - Select if the title is in italics or not.
    *   - FontWeight
        - Select if the title is bold or not.
    *   - Wrap
        - Select if the title will wrap if it has not enough space or not.

CONTROL

.. list-table::
    :widths: 10 40

    *   - Width
        - Allows you to set the width of the input field manually. Only takes number in pixels, no additional symbols required.
    *   - Placeholder
        - Allows you to set placeholder value for the text input. Can be used as an example for the users.
    *   - FontSize
        - Select font size for the input.
    *   - FontColor
        - Select font color for the input. Can be either selected or manually entered.
    *   - FontStyle
        - Select if the input is in italics or not.
    *   - FontWeight
        - Select if the input is bold or not.

TextBox
-------------------------------------------------------------
TextBox is the basic text input field. It doesn't support multiple lines of text and doesn't include an editor, but it's well-suited for short and simple inputs.

.. image:: ../images/designer/fields/TextBox.png
   :alt: TextBox

TextBox unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
TextBox field has the following unique settings:

PATTERN

.. list-table::
    :widths: 10 40

    *   - Type
        - Select the Type of the Textbox, this will automatically apply a pattern to it. Several types are available, such as Email, Phone, Numeric, etc. This will determine what type of text can be input, and will give field a validator to make sure that the input is correct. You can alter any of the settings, this will automatically switch Type to Custom.
    *   - Pattern
        - A regex pattern which the field has to follow. You can either input your own, or select one of the available Types and it will be automatically set for you.
    *   - Flags
        - Regex flags, more on that |Regex flags|.
    *   - Error
        - The error message shown when the input text doesn't match the pattern.

.. |Regex flags| raw:: html

   <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp#Parameters" target="_blank">here</a>

.. _designer-maskedtextbox:

MaskedTextBox
-------------------------------------------------------------
MaskedTextBox is similar to a regular TextBox, but you can restrict what the user can input. It's not validation, user simply won't be able to enter any text that doesn't match the mask.

.. image:: ../images/designer/fields/MaskedTextBox.png
   :alt: MaskedTextBox

MaskedTextBox unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
MaskedTextBox field has the following unique settings:

CONTROL

.. list-table::
    :widths: 10 30
        
    *   -   **mask**
        -   Specifies the input mask. The following mask rules are supported:

            0 - Digit. Accepts any digit between 0 and 9.

            9 - Digit or space. Accepts any digit between 0 and 9, plus space.

            # - Digit or space. Like 9 rule, but allows also (+) and (-) signs.

            L - Letter. Restricts input to letters a-z and A-Z. This rule is equivalent to [a-zA-Z] in regular expressions.

            ? - Letter or space. Restricts input to letters a-z and A-Z. This rule is equivalent to [a-zA-Z] in regular expressions.

            & - Character. Accepts any character. The rule is equivalent to \S in regular expressions.

            C - Character or space. Accepts any character. The rule is equivalent to . in regular expressions.

            A - Alphanumeric. Accepts letters and digits only.

            a - Alphanumeric or space. Accepts letters, digits and space only.

            . - Decimal placeholder. The decimal separator will be gotten from the current culture.

            , - Thousands placeholder. The display character will be gotten from the current culture.
            
            $ - Currency symbol. The display character will be gotten from the current culture.

            For more information and examples, please, checkout |KendoUI MaskedTextBox|.


.. |KendoUI MaskedTextBox| raw:: html

   <a href="https://demos.telerik.com/kendo-ui/maskedtextbox/index" target="_blank">KendoUI MaskedTextBox</a>


Numeric
-------------------------------------------------------------
Numeric is the basic number input field.

.. image:: ../images/designer/fields/Numeric.png
   :alt: Numeric

MultilineTextBox
-------------------------------------------------------------
Advanced text input, allows input of multiple lines and includes basic text editor.

.. image:: ../images/designer/fields/MultilineTextBox.png
   :alt: MultilineTextBox

DropDown
-------------------------------------------------------------
DropDown field gives user a choice which is displayed in a dropdown menu.

.. image:: ../images/designer/fields/DropDown.png
   :alt: DropDown

DropDown unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
DropDown field has the following unique settings:

CONTROL

.. list-table::
    :widths: 10 40

    *   - Items
        - Specify items users can choose from.
    *   - MultiChoice
        - Select if user can choose more than one item from dropdown or not.

Toggle
-------------------------------------------------------------
Toggle field gives user a choice between Yes or No. By default has False value.

.. image:: ../images/designer/fields/Toggle.png
   :alt: Toggle

Toggle unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Toggle field has the following unique settings:

CONTROL

.. list-table::
    :widths: 10 40

    *   - OnLabel
        - Select displayed text for the True value.
    *   - OffLabel
        - Select displayed text for the False value.

Checkboxes
-------------------------------------------------------------
Checkboxes field gives user a choice which is presented as a number of checkboxes.

.. image:: ../images/designer/fields/Checkboxes.png
   :alt: Checkboxes

Checkboxes unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Checkboxes field has the following unique settings:

CONTROL

.. list-table::
    :widths: 10 40

    *   - Items
        - Specify items users can choose from.
    *   - Columns
        - Number of columns items are grouped by.

Radios
-------------------------------------------------------------
Radios field gives user a choice which is presented as a number of radio buttons. Unlike checkboxes, only one option can be selected.

.. image:: ../images/designer/fields/Radios.png
   :alt: Radios

Radios unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Radios field has the following unique settings:

CONTROL

.. list-table::
    :widths: 10 40

    *   - Items
        - Specify items users can choose from.
    *   - Columns
        - Number of columns items are grouped by.

Date
-------------------------------------------------------------
Date field allows users to input date.

.. image:: ../images/designer/fields/Date.png
   :alt: Date

DateTime
-------------------------------------------------------------
DateTime field allows users to input date and time.

.. image:: ../images/designer/fields/DateTime.png
   :alt: DateTime

Attachments
-------------------------------------------------------------
Attachments field allows users to attach files to the form. It's possible to do it by either uploading files manually or dragging and dropping them into the field.
Possible to drag and drop multiple files at once.

.. image:: ../images/designer/fields/Attachments.png
   :alt: Attachments

Attachments unique properties
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Attachments field has the following unique settings:

SETTINGS

.. list-table::
    :widths: 10 40

    *   - MaxSize (Kb)
        - Maximum file size each uploaded file can be. Maximum file size is 10240, but you can restrict it down.
    *   - AllowedExtensions
        - Choose what files should be allowed to upload. Extensions should have a dot in front of them, can be separated by a comma, a semicolon or placed on different lines. If empty, all extensions are allowed.