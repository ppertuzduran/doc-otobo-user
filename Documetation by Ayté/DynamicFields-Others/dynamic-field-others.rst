Script Dynamic Field Settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This dynamic field 'Script' allows you to calculate expressions based on the Toolkit Template language, as long as the conditions defined during the field creation are met.

.. figure:: images/dynamic-field-script.png
   :alt: Script Dynamic Field Settings

   Script Dynamic Field Settings

Expression Field
   In the ``Expression field``, the function to be evaluated will be defined. Example:

   ::

      [% Data.QueueID * 5 %]

Requirements 
   List of attributes that function as conditions. If one or more attributes are chosen, the function will only be executed if the attributes have valid values ​​set.

Preview Triggers 
   If configured, the function will be re-evaluated via AJAX every time the value of the selected attribute or attributes is updated.

Storage Triggers (Events) 
   If one or more events from the list are selected, the expression will be re-evaluated every time the event or events occur.

Show link 
   Here you can specify an optional HTTP link for the field value in overviews and zoom screens. Example:

   ::

      http://some.example.com/handle?query=[% Data.Field1 | uri %]

Link for preview
   If filled in, this URL will be used for a preview which is shown when this link is hovered in ticket zoom. Please note that for this to work, the regular URL field above needs to be filled in, too.

Check RegEx
   Here you can specify a regular expression to check the value. The regex will be executed with the modifiers ``xms``. Example:

   ::

      ^[0-9]$

Add RegEx
   Clicking on the *⊞* button will add two new fields, where a regular expression and an error message can be added.


Lens Dynamic Script Settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Lens field allows referencing objects within OTOBO, along with their characteristics, enabling the display and/or editing of them.

.. figure:: images/dynamic-field-lens.png
   :alt: Lens Dynamic Field Settings

   Lens Dynamic Field Settings

The referenced dynamic field
   Here you can set up a dynamic field that references an object within OTOBO, such as Agent, Customer (User), Ticket, CI, and CI Version.

The attribute of the referenced object
   Here you can reference an attribute of the related object. For example, accessing an attribute of a related CI in the referenced dynamic field.


Reference Dynamic Field Settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Reference dynamic field allows you to point to an object within OTOBO such as an Agent, Customer, Company, or Ticket, from a dynamic field.

.. figure:: images/dynamic-field-reference-options.png
   :alt: Reference Dynamic Field Options

Customer Company
------------------------

.. figure:: images/dynamic-field-reference-company.png
   :alt: Compnay Reference Dynamic Field Settings

Referenced object type
   Here we indicate the type of object to be referenced in the dynamic field.

Input mode of edit field
   Here you can select the mode in which available company customers will be displayed. It can be 'Autocomplete', 'Dropdown', or 'Multiselect'.

Add empty value
  If this option is activated, an extra value is defined to show as a - in the list of possible values. This special value is empty internally.

Multiple Values
  Activating this option allows the field to have multiple values.

Attribute which will be searched on autocomplete
  Here, you can select the attribute by which tickets will be searched.

Check ReferenceFilter
  You can configure filters to limit the results of the list of referenced objects.

Add Reference Filter
  Allows adding more fields (Object attribute - Matches mask attribute - Matches string) to filter.

  Object attribute
    Here, you select an attribute of the company customer by which selectable entries will be filtered.

  Matches mask attribute
    Selects an attribute of the edit mask to compare with the selected attribute of the referenced object. This means that the value of the attribute of the referenced object will be compared with the value of the same attribute in the current edit mask.

  Matches string
    Enter a text string that will be used as a criterion to determine if there is a match between the value of the attribute of the referenced object and this string you provided.


Customer User
------------------------

.. figure:: images/dynamic-field-reference-customer-user.png
   :alt: Customer User Reference Dynamic Field Settings

Referenced object type
   Here we indicate the type of object to be referenced in the dynamic field.

Input mode of edit field
   Here you can select the mode in which available company customers will be displayed. It can be 'Autocomplete', 'Dropdown', or 'Multiselect'.

Add empty value
  If this option is activated, an extra value is defined to show as a - in the list of possible values. This special value is empty internally.

Multiple Values
  Activating this option allows the field to have multiple values.

Check ReferenceFilter
  You can configure filters to limit the results of the list of referenced objects.

Add Reference Filter
  Allows adding more fields (Object attribute - Matches mask attribute - Matches string) to filter.

  Object attribute
    Here, you select an attribute of the company customer by which selectable entries will be filtered.

  Matches mask attribute
    Selects an attribute of the edit mask to compare with the selected attribute of the referenced object. This means that the value of the attribute of the referenced object will be compared with the value of the same attribute in the current edit mask.

  Matches string
    Enter a text string that will be used as a criterion to determine if there is a match between the value of the attribute of the referenced object and this string you provided.
