.. include:: images.rst

.. _administration-label:

Administration
==============

.. _basic-parameters-label:

Basic parameters
-----------------------------------

*Get there:* More > Administration

    **Important**

    Configure all 'parameters' in the order they appear.

.. _libraries-label:

Libraries
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When setting up your Koha system you will want to add information for
every library that will be sharing your system. This data is used in
several areas of Koha.

-  *Get there:* More > Administration > Basic Parameters > Libraries

When visiting this page you are presented with a list of the libraries that have already been added to the system.

|image122|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: libraries).

.. _adding-a-library-label:

Adding a library
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new library:

-  Click 'New library'

-  The top of the form asks for some basics about the library

   |image124|

   -  The library code should not contain any spaces and be 10 or fewer
      characters. This code will be used as a unique identifier in the
      database.

   -  The name will be displayed on the OPAC wherever the library name
      displays to the public and should be a name that makes sense to
      your patrons.

-  Next you can enter basic contact info about the branch

   |image125|

   -  The address and contact fields can be used to make notices custom
      for each library

   -  The email address field is not required, but it should be filled
      for every library in your system

      -  **Important**

             Be sure to enter a library email address to make sure that
             notices are sent to and from the right address

   -  If you'd like you can enter a different 'Reply-To' email address.
      This is the email address that all replies will go to.

      -  **Note**

             If you do not fill in this value Koha will use the address
             in the :ref:`ReplytoDefault` preference

   -  If you'd like you can also enter a different 'Return-Path' email
      address. This is the email address that all bounced messages will
      go to.

      -  **Note**

             If you do not fill in this value Koha will use the address
             in the :ref:`ReturnpathDefault`
             preference

   -  If the URL field is populated then the library name will be linked
      in the holdings table on the OPAC

      |image126|

   -  The OPAC info box is for you to put information about the library
      that will appear in the OPAC when the library name is moused over
      in the holdings table

      |image127|

   -  IP does not have be filled in unless you plan on limiting
      access to your staff client to a specific IP Address

      -  **Important**

             An IP address is required if you have enabled
             :ref:`AutoLocation`

   -  If this library has a specific `MARC organization code <http://www.loc.gov/marc/organizations/orgshome.html>`_, you can enter it   here. If left blank, the code entered in the :ref:`MARCOrgCode` preference will be used for this library.

   -  If you have any notes you can put them here. These will
      not show in the OPAC

   -  Finally, you can choose whether the library will display as an available pickup location for holds

    **Note**

    Of the fields listed, only 'Library code' and 'Name' are required

.. _editing/deleting-a-library-label:

Editing/deleting a library
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You will be unable to delete any library that has patrons or items
attached to it.

|image128|

Each library will have an 'Edit' link to the right of it. Click this
link to edit/alter details associated with the library in question.

    **Important**

    You will be unable to edit the 'Library code'

.. _library-groups-label:

Library groups
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Library groups can serve four purposes: to limit access to patron data,
to limit OPAC searches, to limit staff searches, and/or to define holds
behavior.

-  *Get there:* More > Administration > Basic Parameters > Library groups

When visiting this page you are presented with a list of the groups
that have already been added to the system.

|image123|

.. _adding-a-group-label:

Adding a group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Click the 'Add Group' button at the top of the screen

|image129|

- Give the group a title and a description. Only the title is mandatory
  as it will show up in the staff client and in the OPAC. The description
  is only used in this page to give an idea of what the group is used for.

- You can limit staff from seeing other groups' patrons by checking the
  box next to the 'Limit patron data access by group' option.

    **Note**

    This can be overriden with the :ref:`user permission view_borrower_infos_
    from_any_libraries <patron-permissions-defined-label>`.

- If you want the group to show up in the library pulldown menu at the
  top of the OPAC (with :ref:`OpacAddMastheadLibraryPulldown` set to 'Add')
  and on the advanced search page you can check the 'Use for OPAC search
  groups' box.

- If you want the group to appear in the library pulldown in the staff
  client advanced search, check the 'Use for staff search groups' box.

|image131|

.. _adding-a-library-to-a-group-label:

- If you want to use this group to define holds rules, check the ‘Is local
  hold group’ box.
  
Adding a library to a group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Click on the 'Add library' button next to the group to add a library to
this group. You will be presented with a list of the libraries that are
not already in the group.

|image133|

.. _adding-a-sub-group-label:

Adding a sub-group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If your system is very large, you can create sub-groups. Click on the
'Actions' button next to the group and select the 'Add a sub-group'
option. Fill in the title and the description (optional) of the sub-group.
The features will be inherited from the parent group.

|image1323|

.. _deleting-a-group-label:

Deleting a group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To delete a group, click on the 'Actions' button next to the group and select
the 'Delete' option.

|image1324|

|image1325|

.. _circulation-desks-label:

Circulation desks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Koha allows you to define several circulation desks within a single library.
For example, if you have an adult circulation desk and a children's circulation 
desk, or if you have a different desk for each floor or each department.

Make sure to enable the :ref:`UseCirculationDesks` system preference to use this 
fuctionality.

-  *Get there:* More > Administration > Basic parameters > Desks

.. _adding-circulation-desks:

Adding circulation desks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new circulation desk, click on the 'New desk' button at the top of the 
page.

|image1477|

-  In the 'Desk' field, enter a name for your desk.

-  Choose the library in which this desk is.

-  Click 'Sumbit'.

.. _editing-circulation-desks:

Editing a circulation desk
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To edit an existing circulation desk, click on the 'Edit' button to the right 
of the desk to modify.

|image1478|

From there, you can change the name and/or the library of the desk.

.. _deleting-circulation-desks:

Deleting a circulation desk
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To delete an existing circulation desk, click on the 'Delete' button to the 
right of the desk to remove.

.. _item-types-label:

Item types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Koha allows you to organize your collection by item types and collection
codes.

-  *Get there:* More > Administration > Basic parameters > Item types

Item types typically refer to the material type (book, cd, dvd, etc),
but can be used in any way that works for your library.

|image134|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: table_item_type).

.. _adding-item-types-label:

Adding item types
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new item type, simply click the 'New item type' button at the
top of the Item types page.

|image135|

-  In the 'Item type' field, enter a short code for your item type (maximum
   of 10 characters)

-  The the 'Parent item type' field, you can choose an item type that will act 
   as a parent category for this item type. You can then define 
   :ref:`circulation rules <circulation-and-fines-rules-label>` based on those 
   parent item types.

   -  For example, you could have DVD and Blu-ray item types, and the DVD would 
      be the parent of the Blu-ray item type.

      |image1510|

      You can then create a :ref:`circulation rule <circulation-and-fines-rules-label>` 
      for either Blu-ray only or DVD and Blu-ray (DVD (All))

      |image1511|

-  The description is the plain text definition of the item type (for
   those with multiple languages installed you can translate the item
   type description in to all of those languages using the 'Translate in
   to other languages' link)

-  Item types can be grouped together for searching at the same time.
   For example you can put DVDs and Blu-rays in to a group called Movie
   and then they can be searched together. These groups are defined in
   the ITEMTYPECAT :ref:`authorized value category <existing-values-label>`.

-  You can choose to have an image associated with your item type

   -  You can choose from a series of image collections

   -  You can link to a remote image

   -  Or you can just have no image associated with the item type

      **Important**

      If this option is not enabled, you can change the setting of the 
      :ref:`noItemTypeImages` or :ref:`OPACNoItemTypeImages`.

      To have your item type images appear in the OPAC you need to
      set :ref:`OPACnoItemTypeImages` to 'Yes'

      -  *Get there:* More > Administration > Global system preferences
         > :ref:`OPAC <opac-system-preferences-label>`

-  For items that you are suppressing from the OPAC you can hide their
   item type from being searched in the OPAC

      **Note**
      This will not prevent those items to appear in search results, it
      will simply remove the item type from the advanced search form.

      If you want to completely hide items from a certain item type, let's
      say that you have a professional library with books reserved for staff
      and you don't want those to appear in the OPAC, use the
      :ref:`OpacHiddenItems` system preference.

-  For items that do not circulate, check the 'Not for loan' options

   -  Items marked 'Not for loan' will appear in the catalog, but cannot
      be checked out to patrons

-  For items that you charge a rental fee for, there are several ways that rental
   fees can be charged to a patron by item type. A flat rental charge
   (process fee) or a daily/hourly rental charge.

    -  For items that a library would charge a flat rental charge (process fee)
       for, enter the total fee you charge in the ‘Rental charge’ field.
       This will charge the patron on checkout (and renewal).

    -  For items that a rental charge will be charged by the number of days
       the item is checked out for, enter the daily fee in the 'Daily rental
       charge'. This will be charged to the patron upon checkout -
       the cost per day and how many days this item can be checked out to the
       patron. This daily rental charge will also be applied if/when a renewal
       occurs. 

       -  Check the 'Daily rentals use calendar', to exclude holidays from 
          the the rental fee calculation.

    -  For items that are loaned out hourly, enter the cost per hour in 'Hourly 
       rental charge'. Again, the total (hourly cost * number of hours loaned) 
       will be charged to the patron upon checkout and renewal.

       -  Check the 'Hourly rentals use calendar', to exclude holidays from 
          the the rental fee calculation.

    - Each amount will charge the patron on checkout.

      **Important**

      Do not enter symbols in this field, only numbers and decimal
      points (ex. $5.00 should be entered as 5 or 5.00)

-  You can add a default replacement cost for this type of item. This is the
   amount that will be charged to the patron when lost if the item doesn't have 
   a replacement cost. If the item has a replacement cost, that is the amount 
   that will be charged to the patron.

    **Important**

    Do not enter symbols in this field, only numbers and decimal
    points (ex. $5.00 should be entered as 5 or 5.00)

- You can also add a processing fee that will be added to the replacement cost.

  **Important**

  Do not enter symbols in this field, only numbers and decimal
  points (ex. $5.00 should be entered as 5 or 5.00)

-  If you would like a message or alert to appear when items of this
   type are checked in you can enter that in the 'Checkin message' box

   |image136|

   -  The checkin message type can be a 'message' or an 'alert'. The only
      difference between these two is the styling. By default a message
      is blue

      |image137|

      and an alert is yellow.

      |image138|

-  Some SIP devices need you to use a SIP-specific media type instead of
   Koha's item type (usually lockers and sorters need this media type).
   If you use a device like this you'll want to enter the SIP media
   type.

-  If this item type is only to be used in certain libraries, you can select 
   them here. Select 'All libraries' if this item type is used across the library 
   system.

   **Note** 

   If this is left blank, 'All libraries' is assumed.

   **Note**

   To select more than one library, hold the 'Ctrl' key while selecting the 
   libraries.

.. add description of 'Summary', unless bug 17598 passes...

-  When finished, click 'Save changes'

   **Note**

   All fields, with the exception of the 'Item type' will be
   editable from the item types list

-  Your new item type will now appear on the list

   |image139|

.. _editing-item-types-label:

Editing item types
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Each item type has an Edit button beside it. To edit an item simply
click the 'Edit' button.

    **Important**

    You will not be able to edit the code you assigned as the 'Item
    type' but you will be able to edit the description for the item.

.. _deleting-item-types-label:

Deleting item types
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Each item has a Delete button beside it. To delete an item type, simply click
the 'Delete' button.

    **Important**

    You will not be able to delete item types that are being used by
    items within your system.

|image140|

.. _authorized-values-label:

Authorized values
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Authorized values can be used in several areas of Koha. They are lists of 
controlled terms, phrases or codes.

For example, one reason you would add an authorized value category would be to 
control the values that can be entered into MARC fields by catalogers.

-  *Get there:* More > Administration > Basic parameters > Authorized values

.. _existing-values-label:

Existing authorized values categories
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Koha installs with pre-defined authorized values categories that your library 
is likely to use or that are used by the system.

-  Asort1

   -  Used for acquisitions statistical purposes. You can use this as 
      statistical categories when :ref:`creating a fund <add-a-fund-label>` 
      in acquisitions.

-  Asort2

   -  Used for acquisitions statistical purposes. You can use this as 
      statistical categories when :ref:`creating a fund <add-a-fund-label>` 
      in acquisitions.

-  BOR\_NOTES

   -  Values for pre-defined :ref:`patron messages <opac-messages-label>` that 
      appear on the circulation screen and the patron's account on the OPAC. 
      Write the message you want to appear in the Description field. Note that 
      this field is limited to 200 characters.

      |bor_notes|

-  Bsort1

   -  Values that can be entered to fill in the 
      :ref:`patron's sort 1 field <add-a-new-patron-label>`

-  Bsort2

   -  Values that can be entered to fill in the 
      :ref:`patron's sort 2 field <add-a-new-patron-label>`

-  CAND

   -  A list used in UNIMARC

-  CCODE

   -  Collection codes (appears when 
      :ref:`cataloging and working with items <adding-items-label>`)

   -  This is normally mapped to items.ccode in the Koha database.

   -  If you chose to install the default values for this category, you will have 

      -  Fiction (FIC)

      -  Non-fiction (NFIC)

      -  Reference (REF)

      You can change those to suit your organization's needs.

-  CONTROL\_NUM\_SEQUENCE

   -  Used to generate control numbers in the 
      :ref:`advanced cataloguing editor <advanced-editor-cataloging-label>`.
      Enter a string ending with a number as the authorized value and use
      the description to describe the type of number. For example: 'sprLib0001'
      'Springfield library'. In the advanced editor this will activate a
      new widget that will allow you to choose the type of number and
      generate the next number in the sequence.

-  COUNTRY

   -  A list of country names used in UNIMARC 102 $a

-  DAMAGED

   -  Descriptions for items marked as damaged (appears when 
      :ref:`cataloging and working with items <adding-items-label>`).

   -  This is normally mapped to items.damaged in the database.

   -  If you chose to install the default values for this category, you will have 

      -  Damaged (1)

      You can change those to suit your organization's needs, but the values must 
      be numerical.

.. Warning ::

   The authorized values for DAMAGED must be numerical.


-  DEPARTMENT

   -  Departments are required by and are used in the 
      :ref:`course reserves <course-reserves-label>` module

-  ETAT

   -  Used in French UNIMARC installations in field 995 $o to identify item status.
      Similar to NOT\_LOAN

-  HINGS\_AS

   -  General holdings: acquisition status designator :: This data
      element specifies acquisition status for the unit at the time of
      the holdings report.

-  HINGS\_C

   -  General holdings: completeness designator

-  HINGS\_PF

   -  Physical form designators

-  HINGS\_RD

   -  General holdings: retention designator :: This data element
      specifies the retention policy for the unit at the time of the
      holdings report.

-  HINGS\_UT

   -  General holdings: type of unit designator

-  HOLD\_CANCELLATION

   -  Reasons why a hold might have been cancelled. These are used when 
      :ref:`cancelling holds <managing-holds-label>`.

   -  If you chose to install the default values for this category, you will have 

      -  Item could not be located on shelves (NOT\_FOUND)

      -  Item was found to be too damaged to fill hold (DAMAGED)

      You can change those to suit your organization's needs.

-  HSBND\_FREQ

   -  Delivery frequencies used by the housebound module. They are displayed on
      the :ref:`housebound tab <housebound-patrons-label>` in the patron's 
      account in the staff interface.

   -  If you chose to install the default values for this category, you will have 

      -  Every week (EW)

      You can change those to suit your organization's needs.

-  ILLSTATUS

   -  Interlibrary loan (ILL) request statuses used in the 
      :ref:`ILL module <ill-requests-label>`.
      
-  ITEMTYPECAT

   -  Search categories for item types. These values allow multiple item types 
      to be searched at the same time.

   -  To combine item types in categories, choose the category in the 
      :ref:`item type settings <item-types-label>`.

   -  For example, an ITEMTYPECAT value could be 'NEW'. This search category 
      could be set for the item types 'NEW BOOKS' and 'NEW DVDS'. This will 
      replace NEW BOOKS and NEW DVDS item types in the advanced search form by 
      'NEW'. When a patron chooses the searched for the category 'NEW', they 
      will search multiple item types with a single search.

-  LANG

   -  A list of ISO 639-2 standard language codes.

-  LOC

   -  Shelving locations (usually appears when 
      :ref:`adding or editing an item <adding-items-label>`). 

   -  This is normally mapped to items.location in the Koha database.

   -  If you chose to install the default values for this category, you will have 

      -  Audio visual (AV)

      -  Book cart (CART)

         -  CART is used by :ref:`UpdateItemLocationOnCheckin`

      -  Children's area (CHILD)

      -  Fiction (FIC)

      -  General stacks (GEN)

      -  New materials shelf (NEW)

      -  On display (DISPLAY)

      -  Processing center (PROC)

         -  PROC can be used with :ref:`NewItemsDefaultLocation` and
            :ref:`UpdateItemLocationOnCheckin`.

      -  Reference (REF)

      -  Staff office (STAFF)

      You can change those to suit your organization's needs.

-  LOST

   -  Descriptions for the items marked as lost (appears when 
      :ref:`adding or editing an item <adding-items-label>`).

   -  This is normally mapped to items.itemlost in the Koha database.

   -  If you chose to install the default values for this category, you will have 

      -  Lost (1)

      -  Long overdue (lost) (2)

      -  Lost and paid for (3)

      -  Missing (4)

      You can change those to suit your organization's needs, but the values must 
      be numerical.

.. Warning ::

   The authorized values for LOST must be numerical.

-  OPAC\_SUG

   -  A list of reasons displayed in the 
      :ref:`suggestion form <purchase-suggestions-opac-label>` on the OPAC.

   -  If you chose to install the default values for this category, you will have 

      -  The copy on the shelf is damaged (damaged)

      -  Upcoming title by popular author (bestseller)

      You can change those to suit your organization's needs.

-  NOT\_LOAN

   -  Reasons why a title is not for loan (appears when 
      :ref:`adding or editing an item <adding-items-label>`)

   -  This is normally mapped to items.notforloan in the Koha database.

   -  If you chose to install the default values for this category, you will have 

      -  On order (-1)

      -  Not for loan (1)

      -  Staff collection (2)

      You can change those to suit your organization's needs, but the values must 
      be numerical.

.. Warning ::

   The authorized values for NOT\_LOAN must be numerical.

   -  Negative number values will still allow holds (use for 'on order' 
      statuses, for example) 

   -  Positive numbers will not allow holds or checkouts. 

   -  A value of 0 means 'for loan'.

-  ORDER\_CANCELLATION\_REASON

   -  Reasons why an order might have been cancelled, used in 
      :ref:`acquisitions <cancelling-an-order-label>`

   -  If you chose to install the default values for this category, you will have 

      -  No reason provided (0)

      -  Out of stock (1)

      -  Restocking (2)

      You can change those to suit your organization's needs.

-  PA\_CLASS

   -  Values used to group 
      :ref:`patron attributes <patron-attribute-types-label>` together in 
      the patron add form

-  PAYMENT\_TYPE

   -  Populates a dropdown list of custom payment types when 
      :ref:`paying fines <pay-and-writeoff-fines-label>`

   -  If you chose to install the default values for this category, you will have 

      -  Cash via SIP2 (SIP00)

      -  Visa via SIP2 (SIP01)

      -  Creditcard via SIP2 (SIP02)

      You can change those to suit your organization's needs.

-  qualif

   -  Function codes (author, editor, collaborator, etc.) used in UNIMARC 7XX $4
      (French)

-  RELTERMS

   -  French terms of relations

-  REPORT\_GROUP

   -  A way to sort and filter your reports. These will appear as tabs in the 
      :ref:`saved reports page <edit-custom-reports-label>`.

   -  If you chose to install the default values for this category, you will have 

      -  Account (ACC)

      -  Acquisitions (ACQ)

      -  Catalog (CAT)

      -  Circulation (CIRC)

      -  Patrons (PAT)

      -  Serials (SER)

      You can change those to suit your organization's needs.

-  REPORT\_SUBGROUP

   -  These values can be used to further sort and filter your reports. 

   -  Values here need to include the authorized value code from REPORT\_GROUP 
      in the Description (OPAC) field to link the subgroup to the appropriate group.

      |report_subgroup|

-  RESTRICTED

   -  Restricted status of an item (appears when 
      :ref:`adding or editing an item <adding-items-label>`)

   -  This is normally mapped to items.restricted in the Koha database.

   -  If you chose to install the default values for this category, you will have 

      -  Restricted access (1)

      You can change those to suit your organization's needs, but the values must 
      be numerical.

.. Warning ::

   The authorized values for this category must be numerical.

-  RETURN\_CLAIM\_RESOLUTION

   -  Reasons why a return claim has been resolved

   -  If you chose to install the default values for this category, you will have 

      -  Returned by patron (RET_BY_PATRON)

      -  Found in library (FOUND_IN_LIB)

      You can change those to suit your organization's needs.

-  ROADTYPE

   -  Road types to be used in patron addresses ('street type' field in the 
      :ref:`patron form <add-a-new-patron-label>`)

-  SIP\_MEDIA\_TYPE

   -  Used when :ref:`creating <adding-item-types-label>` or
      :ref:`editing <editing-item-types-label>` an item type to assign a SIP specific
      media type for devices like lockers and sorters.

-  STACK

   -  Shelving control number (appears when 
      :ref:`adding or editing an item <adding-items-label>`)

   -  This is normally mapped to items.stack in the Koha database.

.. Warning ::

   The authorized values for this category must be numerical.

-  SUGGEST

   -  Reasons for acceptance or rejection of suggestions in acquisitions 
      (appears when :ref:`managing suggestions <managing-purchase-suggestions-label>`)

   -  If you chose to install the default values for this category, you will have 

      -  Bestseller (BSELL)

      -  Shelf copy damaged (SCD)

      -  Library copy lost (LCL)

      -  Available via ILL (AVILL)

      You can change those to suit your organization's needs.

-  SUGGEST\_FORMAT

   -  List of item types to display in a drop down menu on the 
      :ref:`suggestion form <purchase-suggestions-opac-label>` on the OPAC.
   
   -  If you chose to install the default values for this category, you will have 

      -  Audiobook (AUDIOBOOK)

      -  Book (BOOK)

      -  EBook (EBOOK)

      -  DVD (DVD)

      -  Large print (LP)

      You can change those to suit your organization's needs.

-  SUGGEST\_STATUS

   -  A list of additional custom status values for 
      :ref:`suggestions <managing-purchase-suggestions-label>` that can be used 
      in addition to the default values. 

-  TERM

   -  Terms to be used in `Course Reserves <#coursereserves>`__ module.
      Enter terms that will show in the drop down menu when setting up a Course
      reserve. (For example: Spring, Summer, Winter, Fall).

-  UPLOAD

   -  Categories to be assigned to :ref:`file uploads <upload-label>`. Without 
      a category, an upload is considered temporary and may be removed during 
      automated cleanup.

-  WITHDRAWN

   -  Description of a withdrawn item (appears when 
      :ref:`adding or editing an item <adding-items-label>`)

   -  This is normally mapped to items.withdrawn in the Koha database.

   -  If you chose to install the default values for this category, you will have 

      -  Withdrawn (1)

      You can change those to suit your organization's needs, but the values must 
      be numerical.

.. Warning ::

   The authorized values for this category must be numerical.

-  YES\_NO

   -  A generic authorized value field that can be used anywhere you
      need a simple yes/no pull down menu.

   -  If you chose to install the default values for this category, you will have 

      -  Yes (1)

      -  No (0)

.. _add-new-authorized-value-category-label:

Add new authorized value category
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In addition to the existing categories that come by default with Koha,
librarians can add their own authorized value categories to control data
that is entered into the system. To add a new category:

-  Click 'New category'

   |image144|

-  Limit your Category to 10 characters (something short to make it
   clear what the category is for)

   -  **Important**

          Category cannot have spaces or special characters other than
          underscores and hyphens in it.

-  When adding a new category you're asked to create at least one
   authorized value

   -  Enter a code for your Authorized value into the 'Authorized value'
      field

      -  **Important**

             Authorized value is limited to 80 characters and cannot
             have spaces or special characters other than underscores
             and hyphens in it.

   -  Use the Description field for the actual value that will be
      displayed. If you want something different to show in the OPAC,
      enter a 'Description (OPAC)'

   -  If you would like to limit this authorized value category to only
      specific libraries you can choose them from the 'Branches
      limitation' menu. To have it show for all libraries just choose
      'All branches' at the top of the list.

   -  If you have
      `StaffAuthorisedValueImages <#StaffAuthorisedValueImages>`__
      and/or :ref:`AuthorisedValueImages` set to
      show images for authorized values you can choose the image under
      'Choose an icon'

-  Click 'Save'

-  Your new category and value will appear on the list of Authorized
   values

   |image145|

.. _add-new-authorized-value-label:

Add new authorized value
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

New authorized values can be added to any existing or new category. To
add a value:

-  Click 'New authorized value for ...'

   |image146|

-  Enter a code for your authorized value into the 'Authorized value'
   field

   -  **Important**

          Authorized value is limited to 80 characters and cannot have
          spaces or special characters other than underscores and
          hyphens in it.

-  Use the Description field for the actual value that will be
   displayed. If you want something different to show in the OPAC, enter
   a 'Description (OPAC)'

-  If you would like to limit this authorized value category to only
   specific libraries you can choose them from the 'Branches limitation'
   menu. To have it show for all libraries just choose 'All branches' at
   the top of the list.

-  If you have
   `StaffAuthorisedValueImages <#StaffAuthorisedValueImages>`__ and/or
   :ref:`AuthorisedValueImages` set to show images
   for authorized values you can choose the image under 'Choose an icon'

-  Click 'Save'

-  The new value will appear in the list along with existing values

   |image147|

.. _delete-authorized-values-label:

Deleting authorized values
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To delete an authorized value, click on the 'Delete' button at the right of the 
authorized value.

Once there are no authorized values left in an authorized value category, you 
can delete the category.

|image1480|

.. _patrons-and-circulation-label:

Patrons and circulation
-------------------------------------

Settings for controlling circulation and patron information.

.. _patron-categories-label:

Patron categories
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Patron categories allow you to organize your patrons into different
roles, age groups, and patron types.

-  *Get there:* More > Administration > Patrons and circulation > Patron
   categories

|patroncatlist|

.. Note :: 

   You can customize the columns of this table in the 
   :ref:`'Table settings'<column-settings-label>` section of the 
   Administration module (table id: patron_categories).

.. _adding-a-patron-category-label:

Adding a patron category
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new patron category click 'New category' at the top of the page

|newpatroncategory|

-  Category code: an identifier for your new category.

   -  The category code is limited to 10 characters (numbers and letters) and 
      must be unique.

   -  This field is required in order to save your patron category. If left 
      blank you will be presented with an error.

-  Description: a plain text version of the category.

   -  The description will be visible throughout Koha.

   -  This field is required in order to save your patron category. If left 
      blank you will be presented with an error.

-  Enrollment period:

   -  In months: should be filled in if you have a limited enrollment period 
      for your patrons. For example, student cards expire after 9 months

   -  Until date: you can choose a date when the cards will expire

   -  This field is required in order to save your patron category. If left 
      blank you will be presented with an error.

.. Warning ::

   You cannot enter both a month limit and a date until for one category. 
   Choose to enter either one or the other.

-  Age required: minimum age (in years) requirement associated with the 
   category. For example, an 'Adult' patron category could have a minimum age 
   of 18 years; this means patrons must be at least 18 to be in the patron 
   category.

   -  When creating or updating a patron, a warning will appear if the patron 
      is too young for this category.

      |patronagelimit|

   -  This value is used by the 
      :ref:`update\_patrons\_category.pl <cron-update-patron-categories-label>` 
      cron job to change the category of patrons who are too young.

-  Upperage limit: maximum age (in years) associated with the category. For 
   example, a 'Children' patron category could have an upperage limit of 18, 
   meaning patrons can have children cards until they turn 18.

   -  When creating or updating a patron, a warning will appear if the patron 
      is too old for this category.

      |patronagelimit|

   -  This value is used by the 
      :ref:`update\_patrons\_category.pl <cron-update-patron-categories-label>` 
      cron job to change the category of patrons who are too old.

-  Enrollment fee: enter the amount if you charge a membership fee for your 
   patrons (such as those who live in another region).

.. Warning ::

   Only enter numbers and decimals in this field.

.. Note ::

   Depending on your value for the :ref:`FeeOnChangePatronCategory` system 
   preference, this fee will be charged on patron renewal as well as when they 
   are first enrolled.

-  Overdue notice required: choose 'Yes' if you want patrons from this category 
   to receive overdue notices. This will enable you to set the
   :ref:`overdue notice triggers <overdue-notice/status-triggers-label>` in 
   the :ref:`Tools module <tools-label>`.

-  Lost items in staff interface: decide on a patron category basis if lost 
   items are shown in the staff interface.

   -  Shown: lost items are shown in the staff interface.

   -  Hidden by default: lost items are hidden, but staff members can click 
      'Show all items' to see them.

.. Note ::

   This is only applicable in the staff interface, so changing this value on 
   patron categories who do not have access to the staff interface won't make 
   any difference.

-  Hold fee: enter the fee amount if you charge patrons from this category a 
   fee for placing holds on items.

.. Warning ::

   Only enter numbers and decimals in this field.

-  Category type: choose one of the six main parent categories

       -  Adult: most common patron type, usually used for a general 'Patron' 
          category.

       -  Child: children patrons can have a guardian to be attached to them.

       -  Staff: library staff

       -  Organizational: organizations can be used as guarantors for Professional 
          patrons.

       -  Professional: professional patrons can be linked to Organizational 
          patrons.

       -  Statistical: this patron type is used strictly for statistical purposes, 
          such as in-house use of items.

   -  This field is required in order to save your patron category.
      If left blank you will be presented with an error.

-  Branch limitations: if necessary, limit this patron category to only some 
   branches in your library system. Select 'All branches' if you would like 
   any library to be able to use this category.

   -  To select more than one branch, hold the Ctrl key while making your 
      selection.

-  Password reset in OPAC: decide whether patrons of this category are allowed 
   to reset their password through the OPAC's 'Forgotten password' function. By
   default, it will follow the rule set in the :ref:`OpacResetPassword`
   system preference.

   -  Follow system preference :ref:`OpacResetPassword`.

   -  Allowed: patrons of this category will be able to reset their password 
      through the OPAC regardless of the setting in :ref:`OpacResetPassword`.

   -  Not allowed: patrons of this category will *not* be able to reset their 
      password through the OPAC regardless of the setting in 
      :ref:`OpacResetPassword`.

-  Password change in OPAC: decide whether patrons of this category are allowed 
   to change their password through the OPAC. By default, it will follow the 
   rule set in the :ref:`OpacPasswordChange` system preference.

   -  Follow system preference :ref:`OpacPasswordChange`.

   -  Allowed: patrons of this category will be able to change their password 
      through the OPAC regardless of the setting in :ref:`OpacPasswordChange`.

   -  Not allowed: patrons of this category will be *not* able to change their 
      password through the OPAC regardless of the setting in 
      :ref:`OpacPasswordChange`.

-  Minimum password length: enter the minimum password length for patrons of 
   this category. Leave blank to use the default length set in the 
   :ref:`minPasswordLength` system preference.

-  Require strong password: decide whether to enforce a strong password policy 
   (at least one uppercase letter, one lowercase letter and one digit) for 
   patrons of this category. By default, it will follow the rule set in the 
   :ref:`RequireStrongPassword` system preference.

   -  Follow the system preference :ref:`RequireStrongPassword`.

   -  Yes: patrons of this category will be required to have a strong password 
      regardless of the setting in :ref:`RequireStrongPassword`.

   -  No: patrons of this category will *not* be required to have a strong 
      password regardless of the setting in :ref:`RequireStrongPassword`.

-  Block expired patrons: decide if this patrons from this category are blocked 
   from performing actions in the OPAC if their card is expired. By default it 
   will follow the rule set in the :ref:`BlockExpiredPatronOpacActions` 
   preference.

   -  Follow the system preference :ref:`BlockExpiredPatronOpacActions`.

   -  Block: patrons of this category whose membership has expired will be 
      blocked from renewing and placing holds in the OPAC, regardless of the 
      setting in :ref:`BlockExpiredPatronOpacActions`.

   -  Don't block: patrons of this category whose membership has expired will 
      *not* be blocked from renewing and placing holds in the OPAC, regardless 
      of the setting in :ref:`BlockExpiredPatronOpacActions`.

-  Default privacy: choose the default privacy settings for patrons of this
   category. 

   -  Default: checkout history will be kept indefinitely, until either the 
      :ref:`batch\_anonymize.pl script <cron-anonymize-patron-data-label>` is 
      run or there is a manual 
      :ref:`batch anonymization <patrons-anonymize-bulk-delete-label>` which 
      is performed.

   -  Never: checkout history is anonymized upon return. Statistics are kept, 
      but the link between the checkout, the item and the patron is removed.

   -  Forever: checkout history is never anonymized for patrons of this 
      category, regardless of the cron job or manual anonymization.

   -  This setting can be edited by the patron via the OPAC if you allow it 
      with the :ref:`OPACPrivacy` system preference.

-  Exclude from local holds priority: choose whether holds for patrons of this 
   category are given a priority.

   -  Yes: holds for patrons of this category are not given special priority,
      regardless of the setting in 
      :ref:`LocalHoldsPriority <localholdspriority-preferences-label>`.

   -  No: holds for patrons of this category are subjected to the setting in 
      :ref:`LocalHoldsPriority <localholdspriority-preferences-label>`.

-  Default messaging preferences for this patron category: assign advanced 
   messaging preferences by default to the patron category

   -  These default preferences can be changed on an individual basis for 
      each patron. This setting is just a default to make it easier to set up 
      messages when creating new patrons. 

.. Note ::

   This requires that you have :ref:`EnhancedMessagingPreferences` system 
   preference set to 'Allow'.

.. Warning ::

   These defaults will only be applied to new patrons that are added to the 
   system. They will not edit the preferences of the existing patrons.

   If you need to apply the default preferences to existing patrons, you can 
   force those changes by running the borrowers-force-messaging-defaults script 
   found in the misc/maintenance folder. Ask your system administrator for 
   assistance with this script.

.. _circulation-and-fines-rules-label:

Circulation and fines rules
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These rules define how your items are circulated, how and when fines are
calculated and how holds are handled.

-  *Get there:* More > Administration > Patrons and circulation >
   Circulation and fines rules

The rules are applied from most specific to less specific, using the
first found in this order:

-  same library, same patron category, same item type

-  same library, same patron category, all item types

-  same library, all patron categories, same item type

-  same library, all patron categories, all item types

-  default (all libraries), same patron category, same item type

-  default (all libraries), same patron category, all item types

-  default (all libraries), all patron categories, same item type

-  default (all libraries), all patron categories, all item types

The :ref:`CircControl` and :ref:`HomeOrHoldingBranch` also come in to play when
figuring out which circulation rule to follow.

-  If :ref:`CircControl` is set to "the library you are logged in at" circulation
   rules will be selected based on the library you are logged in at

-  If :ref:`CircControl` is set to "the library the patron is from" circulation rules
   will be selected based on the patron's library

-  If :ref:`CircControl` is set to "the library the item is from" circulation rules
   will be selected based on the item's library where
   :ref:`HomeOrHoldingBranch` chooses if the item's home library  or its holding
   library is used.

-  If :ref:`IndependentBranches` is set to 'Prevent'
   then the value of :ref:`HomeOrHoldingBranch` is used in figuring out if the
   item can be checked out. If the item's home library does not match
   the logged in library, the item cannot be checked out unless you are
   a :ref:`superlibrarian <patron-permissions-defined-label>`.

    **Important**

    At the very least you will need to set a default circulation rule.
    This rule should be set for all item types, all libraries and all
    patron categories. That will catch all instances that do not match a
    specific rule. When checking out if you do not have a rule for all
    libraries, all item types and all patron categories then you may see
    patrons getting blocked from placing holds.

.. _defining-circulation-rules-label:

Defining circulation rules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Using the issuing rules matrix you can define rules that depend on
patron category/item type combos. To set your rules, choose a library from the
pull down (or 'Standard rules for all libraries' if you want to apply these rules 
to all branches):

|image156|

From the matrix you can choose any combination of patron categories and
item types to apply the rules to

|image157|

-  First choose which patron category you'd like the rule to be applied
   to. If you leave this to 'All' it will apply to all patron categories

-  Choose the item type you would like this rule to apply to. If you
   leave this to 'All' it will apply to all item types for this patron category

   -  If an item type has a parent item type, the rule will be displayed as 
      Parent -> Child. The number of current checkouts will be limited to either 
      the maximum for the parent (including sibling types) or the specific type's
      rule, whichever is less.

      |image1512|

      In the example above, there is a rule for the DVD item type with a 
      maximum of 5 checkouts and a rule for Blu-ray, a child of DVD, with a 
      maximum of 2 checkouts. A patron at this library will be able to check out 
      a maximum of 2 Blu-rays in a total of 5 items of either DVD or Blu-ray 
      types.

      To summarize, a patron at this library would be able to take either :
      -  0 Blu-ray and a maximum of 5 DVDs
      -  1 Blu-ray and a maximum of 4 DVDs
      -  2 Blu-ray and a maximum of 3 DVDs

-  Add notes about your circulation rule into the notes field. This can
   be helpful to remember why and when something was last changed.

-  Limit the number of items of this type a patron of this category can have 
   checked out at the same time by entering a number in the 'Current checkouts 
   allowed' field.

-  If you're allowing :ref:`on-site checkouts <onsitecheckouts-label>` then you
   may also want to set a limit on the number of items of this type patrons of 
   this category can have on-site.

   -  **Note**

          This setting also depends on the
          :ref:`ConsiderOnSiteCheckoutsAsNormalCheckouts`
          preference

-  Define the period of time an item of this type can be checked out to a 
   patron of this category by entering the number of units (days or hours) in 
   the 'Loan period' box.

-  Define if the loan period should include closed days or not in the 'Days 
   mode' column. The option chosen here will override the :ref:`useDaysMode` 
   system preference for this particular rule.

   -  The 'Default' option will take the option defined in the 
      :ref:`useDaysMode` system preference

   -  Choose the 'Calendar' option if you want to use the calendar to skip the 
      days when the library is closed

   -  Choose the 'Datedue' option if you want to push the due date to the next 
      open day

   -  Choose the 'Days' option if you want to ignore the calendar and calculate 
      the due date directly

   -  Choose the 'Dayweek' option if you want to use the calendar to push the 
      due date to the next open matching weekday for weekly loan periods, or 
      the next open day otherwise

-  Choose which unit of time, days or hours, that the loan period and
   fines will be calculated in in the 'Unit' column

-  You can also define a hard due date for a specific patron category
   and item type. The hard due date offers three options:

   -  Exactly on: The due date of any item checked out with this rule
      will be set to the hard due date.

   -  Before: Koha will calculate the normal loan period. If the calculated
      due date would be after or on the hard due date, the hard due date
      will be used instead.

   -  After: Koha will calculate the normal loan period. If the calculated
      due date would be before the hard due date, the hard due date will
      be used instead.

-  'Fine amount' should have the amount you would like to charge for
   overdue items.

   **Important**

   Enter only numbers and decimal points (no currency symbols).

-  Enter the 'Fine charging interval' in the unit you set (ex. charge
   fines every 1 day, or every 2 hours). The :ref:`finesCalendar` system
   preference controls wether the days the library is closed will be taken
   into account or not.

-  'When to charge' is most handy in libraries that have a fine charging
   interval of more than 1 day.

   -  End of interval: Given a grace period of 2 days and a fine interval of 7 
      days, the first fine will appear 7 days after the due date, it will 
      always take one fine interval (7 days), before the first fine is charged.

   -  Start of interval: Given a grace period of 2 days and a fine interval of 
      7 days, the first fine will appear 2 days after the due date and the
      second fine 7 days after the due date.

-  The 'Fine grace period' is the period of time an item can be overdue
   before you start charging fines. The :ref:`FinesIncludeGracePeriod`
   system preference controls if the grace period will be included when
   calculating the fine or not.

   **Important**

   This can only be set for the 'Day' unit, not in 'Hours'

-  The 'Overdue fines cap' is the maximum fine per item for this patron
   and item type combination.

   **Important**

   If this field is left blank then Koha will not put a limit on the fines 
   this item will accrue. A maximum fine amount for all overdues can be
   set using the :ref:`MaxFine` system preference.

-  If you would like to prevent overcharging patrons for a lost items,
   you can check the box under 'Cap fine at replacement price.' This
   will prevent the patron's fines from going above the replacement
   price on the item.

   **Note**

   If the 'Overdue fines cap' is also set, the fine will be the
   lesser of the two, if both apply to the given overdue
   checkout.

-  If your library 'fines' patrons by suspending their account you can
   enter the number of days their fine should be suspended in the
   'Suspension in days' field.

   **Important**

   This can only be set for the 'Day' unit, not in 'Hours'

-  You can also define the maximum number of days a patron will be
   suspended in the 'Max suspension duration' setting

-  The 'Suspension charging interval' option is just like the 'Fin charging 
   interval'. For example, you could 'fine' a patron one day suspension for 
   every two days overdue.

-  Next decide if the patron can renew this item type and if so, enter
   how many times they can renew it in the 'Renewals allowed' box.

-  If you're allowing renewals you can control how long the renewal loan
   period will be (in the units you have chosen) in the 'Renewal period'
   box.

-  If you're allowing renewals you can control how soon before the due
   date patrons can renew their materials with the 'No renewals before'
   box.

   -  Items can be renewed at any time if this value is left blank.
      Otherwise items can only be renewed if the item is due after the
      number in units (days/hours) entered in this box.

   -  To control this value on a more granular level please set the
      :ref:`NoRenewalBeforePrecision` preference.

-  You can enable automatic renewals for certain items/patrons if you'd
   like. This will renew automatically following your circulation rules
   unless there is a hold on the item.

   **Important**

   You will need to enable the 
   :ref:`automatic renewal cron job <cron-automatic-renewal-label>` for this to 
   work.

   **Important**

   This feature needs to have the "no renewal before" column
   filled in or it will auto renew every day after the due date.

-  If you are using automatic renewals, you can use the 'No automatic renewals 
   after' to limit the time a patron can have the item. For example: don't 
   allow automatic renewals after a checkout period of 80 days.

-  Similar to the hard due date setting, you can also stop automatic renewals
   after a specific date using the 'No automatic renewal after (hard limit)'
   setting.

-  If patrons of this category can place holds on items of this type, enter the 
   total numbers of items (of this type) that can be put on hold in the 'Holds
   allowed' field.

   -  Leave empty to have unlimited holds.

   -  If you'd rather put a hold limit per patron category, independent of the 
      item type, see the 
      :ref:`default checkout and hold policy by patron category <default-checkouts-and-hold-by-category-label>` 
      section below.

   -  If you want to have a hard hold limit, independent of patron category and 
      item type, for this particular library, see the
      :ref:`Default checkout, hold, and return policy <default-checkouts-and-hold-policy-label>`
      section below.

   -  If you want to have a hard hold limit, independent of patron category, 
      item type, and across all libraries, see the :ref:`maxreserves` system 
      preference.

-  You can also set a daily limit on the number of holds a patron can place.

-  While the two settings before limit the holds that can be placed across
   various records, the next setting is used to limit the number of holds
   that can be placed on one record at the same time.
   For example, for fiction books you might want to allow only one item to be 
   placed on hold at the same time by the same user. But for serials where items
   represent different issues more than one hold at the same time is fine.

-  Next you can decide how the availability of items influences the ability
   to place a hold. The 'On shelf holds allowed' option has three settings:

   -  Yes: This will allow to place holds on items at all times. It doesn't
      matter if they are available or checked out.

   -  If any unavailable: This will allow to place a hold as soon as one
      or more items of the record are checked out. It doesn't matter if
      there are still one or more items available on the shelf.

   -  If all unavailable: This will allow to place a hold as soon as all
      items on the record are checked out that could fill the hold. This is
      especially useful for libraries that don't offer the service of getting 
      items placed on hold off the shelf for patrons.

-  Under 'OPAC item level hold' you can decide if patrons are allowed to place 
   item specific holds on the item type in question. The options are:

   -  Allow: Will allow patrons the option to choose next available or
      a specific item.

   -  Don't allow: Will only allow patrons to choose next available item.

   -  Force: Will only allow patrons to choose a specific item.

-  If you want to allow patrons of this category to be able to place article 
   requests on items of this type, choose an option in the 'Article requests' 
   column

   -  No: patrons of this category will not be able to place article requests 
      on items of this type

   -  Yes: patrons of this category will be able to place article requests on 
      items of this type, either on specific items (for example in the case of 
      serial issues) or on entire records (for example in the case of 
      monographs)

   -  Record only: patrons of this category will be able to place article 
      requests on records of this type, but not on specific items

   -  Item only: patrons of this category will be able to place article 
      requests on items of this type, but not on entire records

   **Important**

   If you want to use the article request functionality you need to enable it 
   using the :ref:`ArticleRequests` system preference and configure the form 
   using the other related preferences.

-  Finally, if you :ref:`charge a rental fee for the item type <adding-item-types-label>` 
   and want to give this specific patron category a discount on that fee,
   enter the percentage discount (without the % symbol) in the 'Rental
   discount' field

When finished, click 'Save' to save your changes. To modify a rule,
simply click the 'Edit' button either at the beginning or at the end of the row.
The row of the rule being edited will be highlighted in yellow and the values 
will appear filled in at the bottom of the table. Edit the values at the bottom 
and click save.

|image158|

  **Note**

  If, while editing a rule, you change either the patron category or the item 
  type, it will create a new rule. You can do this to duplicate rules instead of 
  creating new ones if the values are similar.

Alternatively, you can create a rule with the same patron category and item type 
and it will edit the existing one, as there can only be one rule per library-
patron category-item type combination.

If you would like to delete your rule, click the 'Delete' button at the beginning
or at the end of the rule row.

To save time you can clone rules from one library to another by choosing
the clone option above the rules matrix. Please note that this will overwrite
all rules already configured for that library.

|image159|

After choosing to clone you will be presented with a confirmation message.

|image160|

.. _default-checkouts-and-hold-policy-label:

Default checkout, hold, and return policy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can set a default maximum number of checkouts, a default maximum number
of holds and a hold policy that
will be used if none is defined below for a particular item type or
category. This is the fall back rule for defaults.

|image161|

From this menu you can set a default to apply to all item types and
patrons in the library if no other option is set in the forms below.

-  In 'Total current checkouts allowed' enter the total number of items
   patrons can have checked out at one time

-  In 'Total current on-site checkouts allowed' enter the total number
   of items patrons can have checked out on site at a time
   (:ref:`OnSiteCheckouts` needs to be set to 'Enable')

-  In 'Maximum total holds allowed (count)' enter the total number
   of pending holds patrons can have at the same time.

-  Control where patrons can place holds from using the 'Hold Policy'
   menu

   -  From Any Library: Patrons from any library may put this item on
      hold. (default if none is defined)

   -  From Local Hold Group: Only patrons from a library in the item home
      library’s local hold group may put this book on hold.

   -  From Home Library: Only patrons from the item's home library may
      put this book on hold.

   -  No Holds Allowed: No patron may put this book on hold.

-  Control where patron can pick up holds using the “Hold Pickup Library
   Match” menu

   -  any library

   -  item's hold group

   -  patron's hold group

   -  item's home library

   -  item's holding library


-  Control where the item returns to once it is checked in

   -  Item returns home

   -  Item returns to issuing branch

   -  Item floats

      -  When an item floats it stays where it was checked in and does
         not ever return 'home'

-  Once your policy is set, you can unset it by clicking the 'Unset'
   link to the right of the rule

.. _default-checkouts-and-hold-by-category-label:

Default checkout and hold policy by patron category
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For this library, you can specify the maximum number of checkouts,
on-site checkouts and holds that a patron of a given category can have,
regardless of the item type.

|image162|

    **Note**

    If the total amount of checkouts, on-site checkout and holds
    for a given patron category is left blank, no limit applies,
    except possibly for a limit you define in the circulation rules above.

For example, if you have a rule in the matrix that says Board patrons
are allowed 10 books and 5 DVDs but you want to make it so that Board
patrons only have a total of 12 things checked out at once. If you enter
12 here and the patron has 10 books out already they will only be
allowed 2 DVDs to equal the 12 total they're allowed.

.. _item-fee-refund-on-return-label:

Default lost item fee refund on return policy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here, you can specify the default policy for lost item fees on return.
This policy will apply to this library. This rule is to be used with the
:ref:`RefundLostOnReturnControl` system preference.

You can limit the number of days during which a lost item is refundable using 
the :ref:`NoRefundOnLostReturnedItemsAge` system preference.

.. _item-hold-policies-label:

Default holds policy by item type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For this library, you can edit hold and return policies for a given item
type, regardless of the patron's category.

|image163|

The various hold policies have the following effects:

-  From any library: Patrons from any library may put this item on hold.
   (default if none is defined)

-  From local hold group: Only patrons from libraries in the same item's
   home library hold groups may put this book on hold.
   
-  From home library: Only patrons from the item's home library may put
   this book on hold.

-  No holds allowed: No patron may put this book on hold.

    **Important**

    Note that if the system preference
    :ref:`AllowHoldPolicyOverride` set to
    'allow', these policies can be overridden by your circulation staff.

    **Important**

    These policies are applied based on the ReservesControlBranch
    system preference.

Control where patron can pick up holds using the “Hold Pickup Library Match”
menu

-  any library

-  item's hold group

-  patron' hold group

-  item's home library

-  item's holding library

The various return policies have the following effects:

-  Item returns home: The item will prompt the librarian to transfer the
   item to its home library

   -  **Important**

          If the :ref:`AutomaticItemReturn`
          preference is set to automatically transfer the items home,
          then a prompt will not appear

-  Item returns to issuing branch: The item will prompt the librarian to
   transfer the item back to the library where it was checked out

   -  **Important**

          If the :ref:`AutomaticItemReturn`
          preference is set to automatically transfer the items home,
          then a prompt will not appear

-  Item floats: The item will not be transferred from the branch it was
   checked in at, instead it will remain there until transferred
   manually or checked in at another branch

For example you might allow holds at your libraries but not what New
items or DVDs to be placed on hold by other branches so you can set the
'Hold policy' to 'From home library' so that those items can only be
placed on hold if the items' owning library and the patron's home
library are the same. You can also block holds completely on specific
item types from this form. This is also how you can set up floating item
types and types that remain with their home library.

.. _patron-attribute-types-label:

Patron attribute types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Patron attributes can be used to define custom fields to associate with
your patron records. In order to enable the use of custom fields you
need to set the :ref:`ExtendedPatronAttributes`
system preference.

-  *Get there:* More > Administration > Patrons and circulation > Patron
   attribute types

A common use for this field would be for a student ID number or a
Driver's license number.

|image164|

.. _adding-patron-attributes-label:

Adding patron attributes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new patron attribute type, click the 'New patron attribute
type' button at the top of the page

|image165|

-  In the 'Patron attribute type code', enter a short code to identify
   this field

   -  **Important**

          This field is limited to 10 characters (numbers and letters
          only)

   -  **Important**

          This setting cannot be changed after an attribute is defined

-  In the 'Description' field, enter a longer (plain text) explanation
   of what this field will contain

-  Check the box next to 'Repeatable' to let a patron record have
   multiple values of this attribute.

   -  **Important**

          This setting cannot be changed after an attribute is defined

-  If 'Unique identifier' is checked, the attribute will be a unique
   identifier which means, if a value is given to a patron record, the
   same value cannot be given to a different record.

   -  Unique attributes can be used as match points on the :ref:`patron
      import tool <patron-import-label>`

   -  **Important**

          This setting cannot be changed after an attribute is defined

-  Check 'Display in OPAC' to display this attribute on a patron's
   details page in the OPAC.

-  Check 'Editable in OPAC' to enable patrons to edit this information in 
   the OPAC.

-  Check 'Searchable' to make this attribute searchable in the staff
   patron search.

-  Check 'Display in patron's brief information' to make this attribute visible in the
   patron's short detail display on the left of the checkout screen and
   other patron pages

   |image166|

-  Authorized value category; if one is selected, the patron record
   input page will only allow values to be chosen from the authorized
   value list.

   -  You will first need to add an authorized value list for it to
      appear in this menu

      -  *Get there:*\ More > Administration > Basic parameters >
         :ref:`Authorized values <authorized-values-label>`

   -  **Important**

          an authorized value list is not enforced during batch patron
          import.

-  If you would like this attribute to only be used by specific branches
   you can choose those branches from the 'Branches limitation' list.
   Choose 'All branches' to show it for all libraries.

   -  **Important**

          Note that items with locations already set on them will not be
          altered. The branch limitation only limits the choosing of an
          authorized value based on the home branch of the current staff
          login. All authorized values for item records (LOC, LOST,
          CCODE, etc) will show in the OPAC for all patrons.

-  If you'd like to only show this attribute on patrons of one type
   choose that patron type from the 'Category' pull down

-  If you have a lot of attributes it might be handy to group them so
   that you can easily find them for editing. If you create an
   :ref:`Authorized value <authorized-values-label>` for PA\_CLASS it will show
   in the 'Class' pull down and you can then change your attributes page
   to have sections of attributes

   |image167|

-  Click Save to save your new attribute

Once added your attribute will appear on the list of attributes and also
on the patron record add/edit form

|image168|

If you have set up classes for organizing attributes they will appear
that way on the add/edit patron form

|image169|

.. _editing/deleting-patron-attributes-label:

Editing/deleting patron attributes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Each patron attribute has an edit and a delete link beside it on the
list of attributes.

Some fields in the attribute will not be editable once created:

-  Patron attribute type code

-  Repeatable

-  Unique identifier

You will be unable to delete an attribute if it's in use.

|image170|

.. _library-transfer-limits-label:

Library transfer limits
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Limit the ability to transfer items between libraries based on the
library sending, the library receiving, and the collection code
involved.

-  *Get there:* More > Administration > Patrons and circulation > Library
   transfer limits

These rules only go into effect if the preference
:ref:`UseBranchTransferLimits <usebranchtransferlimits-and-branchtransferlimitstype-label>` is set to 'enforce'.

Before you begin you will want to choose which library you are setting
these limits for.

|image171|

Transfer limits are set based on the collections codes you have applied
via the :ref:`Authorized values <authorized-values-label>` administration area.

|image172|

Collection codes will appear as tabs above the checkboxes:

|image173|

Check the boxes for the libraries you allow your items to be transferred to for the
collection code you have selected at the top (in the example below - FIC)

|image174|

In the above example, Centerville library will allow patrons from all libraries 
except Liberty and Franklin to request items from their branch.

.. _transport-cost-matrix-label:

Transport cost matrix
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The transport cost matrix lets a library system define relative costs to
transport books to one another. In order for the system to use this
matrix you must first set the
:ref:`UseTransportCostMatrix` preference to
'Use'.

    **Important**

    The transport cost matrix takes precedence in controlling where
    holds are filled from, if the matrix is not used then Koha checks
    the :ref:`StaticHoldsQueueWeight <holds-queue-system-preferences-label>`.

Costs are decimal values between some arbitrary maximum value (e.g. 1 or
100) and 0 which is the minimum (no) cost. For example, you could just
use the distance between each library in miles as your 'cost', if that
would accurately reflect the cost of transferring them. Perhaps post
offices would be a better measure. Libraries sharing a post office would
have a cost of 1, adjacent post offices would have a cost of 2, etc.

To enter transport costs simply click in the cell you would like to
alter, uncheck the 'Disable' box and enter your 'cost'

|image175|

After entering in your cost, hit 'Enter' on your keyboard or click the
'Save' button at the bottom of the matrix to save your changes.

    **Note**

    A NULL value will make no difference where the From and To libraries
    are the same library. However, as a best practice, you should put a
    0 in there. For all other To/From combinations, a NULL value will
    cause that relationship to act as if it has been disabled. So, in
    summary, don't leave any of the values empty. It's best to always
    put a number in there ( even if you choose to disable that given
    To/From option ).

.. _item-circulation-alerts-label:

Item circulation alerts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Libraries can decide if they want to have patrons automatically notified
of circulation events (check ins and check outs).

-  *Get there:* More > Administration > Patrons and circulation > Item
   circulation alerts

These preferences are set based on patron types and item types.

    **Important**

    These preference can be overridden by changes in the individual
    patron's messaging preferences.

To set up circulation alerts:

-  Choose your library from the pull down at the top of the screen

   |image176|

   -  To set preferences for all libraries, keep the menu set to
      'Default'

-  By default all item types and all patrons are notified of check ins
   and check outs. To change this, click on the item/patron type combo
   that you would like to stop notices for.

   |image177|

   -  In the above example, Juveniles and Kids will not receive check
      out notices.

.. _cities-and-towns-label:

Cities and towns
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To standardize patron input you can define cities or towns within your
region so that when new patrons are added librarians simply have to
select the town from a list instead of having to type the town and zip
(or postal) code information.

-  *Get there:* More > Administration > Patrons and circulation > Cities
   and towns

.. _adding-a-city-label:

Adding a city
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new city, click the 'New city' button at the top of the page
and enter the city name, state, zip/postal code and country.

|image178|

One you click Submit, your city will be saved and will be listed on the
Cities and towns page

|image179|

Cities can be edited or deleted at any time.

.. _viewing-cities-on-patron-add-form-label:

Viewing cities on patron add form
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you have defined local cities using the 'New city' form, then when
adding or editing a patron record you will see those cities in a pull
down menu to make city selection easy.

|image180|

This will allow for easy entry of local cities into the patron record
without risking the potential for typos or mistaken zip/postal codes.

.. _accounting-administration-label:

Accounting
---------------------------------------------------------------------

-  *Get there:* More > Administration > Accounting

This section deals with the parameters used in managing the patron 
accounts.

.. _debit-types-label:

Debit types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  *Get there:* More > Administration > Accounting > Debit types

This is where you define the manual fees you can charge patrons.

|image1444|

When you first get to the page, you will only see the manual fees that 
are already defined in your system. 

You can see the default system fees by clicking "Show all debit types".

|image1445|

You can go back to seeing only the manual fees by clicking "Filter 
system debit types".

.. _system-debit-types-label:

System debit types
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Several debit types come installed with Koha. Most of them are 
automatic fees that are added according to the policies you set up 
elsewhere in Koha.

-  ACCOUNT (Account creation fee): this is charged to the patron's 
   account upon registration. The fee can be changed in the 
   :ref:`patron category settings <adding-a-patron-category-label>` 
   under 'Enrollment fee'.

-  ACCOUNT\_RENEW (Account renewal fee): this is charged to the 
   patron's account when their account is renewed. Like the ACCOUNT 
   debit type above, this can be changed in the 
   :ref:`patron category settings <adding-a-patron-category-label>` 
   under 'Enrollment fee'.

-  LOST (Lost item): this is charged to the patron's account when an 
   item in their file is declared lost. The amount depends on the 
   :ref:`item's 'replacement cost' field <adding-items-label>` or on 
   the :ref:`item type's default replacement cost <adding-item-types-label>`. 
   It can also be added manually in the :ref:`manual invoices 
   <creating-manual-invoices-label>` tab.

-  MANUAL (Manual fee): this is the default manual fee installed with 
   Koha. This is not charged automatically by Koha, but can be added 
   to a patron's account manually in the :ref:`manual invoices 
   <creating-manual-invoices-label>` tab.

-  NEW\_CARD (New card fee): this is another default manual fee installed 
   with Koha. This will not be charged automatically by Koha, but can 
   be added to a patron's account manually in the :ref:`manual invoices 
   <creating-manual-invoices-label>` tab.

-  OVERDUE (Overdue fine): this is charged automatically to the patron's 
   account when they have overdue items. The amount for overdue fines are 
   set in the :ref:`circulation and fines rules <circulation-and-fines-rules-label>`.

-  PAYOUT (Payment from library to patron): this is used when the library 
   reimburses the patron (for an overpayment for example).

-  PROCESSING (Lost item processing fee): this is charged automatically 
   to the patron's account when an item in their file is declared lost. 
   The amount is set by :ref:`item type <adding-item-types-label>` under 
   'Processing fee (when lost)'.

-  RENT (Rental fee): this is charged automatically to the patron's 
   account upon checkout if the :ref:`item type <adding-item-types-label>` 
   has a rental charge.

-  RENT\_DAILY (Daily rental fee): this is charged automatically to the 
   patron's account upon checkout if the :ref:`item type <adding-item-types-label>` 
   has a daily rental charge.

-  RENT\_DAILY\_RENEW (Renewal of daily rental item): this is charged 
   automatically to the patron's account upon renewal if the 
   :ref:`item type <adding-item-types-label>` has a daily rental charge.

-  RENT\_RENEW (Renewal of rental item): this is charged automatically 
   to the patron's account upon renewal if the :ref:`item type 
   <adding-item-types-label>` has a rental charge.

-  RESERVE (Hold fee): this is charged automatically to the patron's 
   account upon placing a hold. The amount depends on the 'Hold fee' 
   amount in the :ref:`patron's category <adding-a-patron-category-label>` 
   settings.

-  RESERVE\_EXPIRED (Hold waiting too long): this is charged automatically 
   to the patron's account if they haven't picked up their hold after the 
   number of days defined in the :ref:`ExpireReservesMaxPickUpDelay` 
   system preference. The amount is set in the :ref:`ExpireReservesMaxPickUpDelayCharge` 
   system preference.

.. _add-debit-type-label:

Adding a new debit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new debit type:

-  Click 'New debit type'

   |image1446|

   -  Enter a code (limited to 64 letters)

   -  Enter the default amount

      **Note**

      Staff will be able to change this amount when adding the charge 
      to the patron's account, if necessary

      **Note**

      Do not enter currency symbols. Only write the amount with a decimal 
      point (for example, 5 or 5.00 instead of $5)

   -  Write a description

      This description will be used in the drop-down menu when adding 
      a new charge to a patron's account as well as in their transaction 
      history

   -  If this debit type can be added manually by staff to a patron's 
      account via the :ref:`manual invoices <creating-manual-invoices-label>`, 
      check the 'Can be added manually?' check box

   -  If this debit type is only to be used in specific branches, you can 
      select the libraries in 'Libraries limitation'

      **Note**

      You can select more than one library by pressing the 'Ctrl' key 
      while selecting.

   -  Click 'Save'

.. _edit-debit-type-label:

Editing an existing debit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can only modify the debit types you have added, as well as the 
'Manual fee'.

To edit a debit type:

-  Click the 'Edit' button to the right of the debit type

-  Modify any field

-  Click 'Save'

.. _archive-debit-type-label:

Archiving a debit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If there is a debit type you don't need anymore, you can archive it. 

  **Note**

  There is no way to delete a debit type since they are used in the 
  patron's accounting section.

To archive a debit type, simply click the 'Archive' button to the 
right of the debit type.

.. _restore-debit-type-label:

Restoring an archived debit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you need to use an archived debit type again, simply click on the 
'Restore' button to the right of the debit type.

This will make it available again.

.. _credit-types-label:

Credit types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  *Get there:* More > Administration > Accounting > Credit types

This is where you define the manual credits you can give patrons.

When you first get to the page, you will only see the credits that 
are already defined in your system. 

You can see the default system credit types by clicking "Show all credit types".

|image1475|


You can go back to seeing only the manual credit types by clicking "Filter 
system credit types".

.. _system-credit-types-label:

System credit types
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Several credit types come installed with Koha. Most of them are 
automatic credits that are added according to the policies you set up 
elsewhere in Koha. They can not be deleted.

-  CANCELLATION (Cancelled charge): this is used when 
   :ref:`cancelling a charge in a patron's account <charging-fines/actions-label>`

-  CREDIT (Credit): this is used for :ref:`manual credits <creating-manual-credits-label>` 
   to give to your patrons.

-  DISCOUNT (A discount applied to a patrons fine): this is used to 
   :ref:`discount fines and charges <charging-fines/actions-label>`.

-  FORGIVEN (Forgiven): this is used for :ref:`manual credits <creating-manual-credits-label>` 
   to give to your patrons.

-  LOST\_FOUND (Lost item fee refund): this is used when a previously 
   lost item is returned. If you refund the lost fees (see :ref:`Default 
   lost item fee refund on return policy <item-fee-refund-on-return-label>`), 
   this credit will be applied to refund the fee.

-  OVERPAYMENT (Overpayment refund): this is automatically applied to a 
   patron's account when they paid too much for a fee. This is mostly used 
   when backdating checkins where the patron has already paid the full fine.

-  PAYMENT (Payment): as the name states, this is used to indicate 
   :ref:`fee payments <pay-and-writeoff-fines-label>`.

-  PURCHASE (Purchase): this is used when a payment is made through 
   the :ref:`point of sale module<point-of-sale-label>`.

-  REFUND (A refund applied to a patrons fine): this is used when 
   :ref:`refunding the payment of a fine or charge <charging-fines/actions-label>`.

-  WRITEOFF (Writeoff): this is used when :ref:`writing off a fine or charge<pay-and-writeoff-fines-label>`.

.. _add-credit-type-label:

Adding a new credit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new credit type:

-  Click 'New credit type'

   |image1476|

   -  Enter a code (limited to 64 letters)

   -  Write a description

      This description will be used in the drop-down menu when adding 
      a new credit to a patron's account as well as in their transaction 
      history

   -  If this credit type can be added manually by staff to a patron's 
      account via the :ref:`manual credit <creating-manual-credits-label>`, 
      check the 'Can be added manually?' check box

   -  If you need this credit type to be sequentially numbered, check the 
      'Enable credit number'. The format of the number is defined in the 
      :ref:`AutoCreditNumber` system preference.

   -  If this credit type is only to be used in specific branches, you can 
      select the libraries in 'Libraries limitation'

      **Note**

      You can select more than one library by pressing the 'Ctrl' key 
      while selecting.

   -  Click 'Save'

.. _edit-credit-type-label:

Editing an existing credit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can only modify the credit types you have added.

To edit a credit type:

-  Click the 'Edit' button to the right of the credit type

-  Modify any field

-  Click 'Save'

.. _archive-credit-type-label:

Archiving a credit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If there is a credit type you don't need anymore, you can archive it. 

  **Note**

  There is no way to delete a credit type since they are used in the 
  patron's accounting section.

To archive a credit type, simply click the 'Archive' button to the 
right of the credit type.

.. _restore-credit-type-label:

Restoring an archived credit type
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you need to use an archived credit type again, simply click on the 
'Restore' button to the right of the credit type.

This will make it available again.

.. _cashregisters-label:

Cash registers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  *Get there:* More > Administration > Accounting > Cash registers

This feature is enabled through the :ref:`UseCashRegisters` system preference.

If you have no cash registers already defined, you will be invited to create 
one.

Otherwise, you will see the list of all your cash registers.

|image1450|

In the 'Actions' columns, you can choose to edit your cash registers, make one 
of them default or remove the default status, and archive or restore an 
archived register.

The default status is only useful in libraries that have more than one register 
per branch. The default register will be pre-selected when :ref:`entering a 
payment <pay-and-writeoff-fines-label>`. If there is only one cash register per 
branch, the branch's cash register will be selected when paying.

.. _addnewcashregister-label:

Adding a new cash register
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

-  Click on 'New cash register'

   |image1449|

-  Give your cash register a name

-  Optionally you can also add a description

-  Choose in which library this cash register is located

-  And finally, enter the initial float, i.e. the amount in the cash register

-  Click 'Add'

.. _catalog-administration-label:

Catalog administration
--------------------------------------

Set these controls before you start cataloging on your Koha system.

-  *Get there:* More > Administration > Catalog

.. _marc-bibliographic-frameworks-label:

MARC bibliographic frameworks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Think of frameworks as templates for creating new bibliographic records.
Koha comes with some predefined frameworks that can be edited or
deleted, and librarians can create their own frameworks for content
specific to their libraries.

-  *Get there:* More > Administration > Catalog > MARC bibliographic
   frameworks

|image181|

    **Important**

    Do not delete or edit the Default framework since this will cause
    problems with your cataloging records - always create a new template
    based on the Default framework, or alter the other frameworks.


.. _add-new-framework-label:

Add new framework
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a new framework

-  Click 'New framework'

   |image183|

   -  Enter a code of 4 or fewer characters

   -  Use the Description field to enter a more detailed definition of
      your framework

-  Click 'Submit'

-  Once your framework is added click Actions then 'MARC structure' to the right of
   it on the list of frameworks

   |image184|

   -  You will be asked to choose a framework to base your new framework
      on, this will make it easier than starting from scratch

-  Once your framework appears on the screen you can edit or delete each
   field by following the instructions for :ref:`editing fields and
   subfields <edit-framework-fields-and-subfields-label>`

.. _edit-existing-frameworks-label:

Edit existing frameworks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Clicking Actions and then 'Edit' to the right of a framework will only allow you to edit
the description for the framework:

|image185|

.. _edit-framework-fields-and-subfields-label:

Edit framework fields and subfields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Frameworks are made up of MARC fields (tags) and subfields.  To make edits to the fields and subfields 
associated with the framework you must click on 'Actions' and then 'MARC structure'.

.. _edit-a-marc-field-label:

Edit a MARC field (tag)
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

After clicking on 'MARC structure' you will be taken to a screen listing all the available tags for that framework and you can search for the tag you need. To make edits to a MARC **field** click on 'Actions' on the right of the field then 'Edit tag'.

|image189|

The next screen shows details of the tag.

-  Each field has a tag (which is the MARC tag) that is uneditable

-  The 'Label for lib' is what will show in the staff interface if you have 
   :ref:`advancedMARCeditor` set to display labels

-  The 'Label for OPAC' is what will show on the MARC view in the OPAC

-  If you check 'Repeatable' then the field will have an icon next to it 
   allowing you to add multiples of that tag

-  If you check 'Mandatory' the record cannot be saved unless the field has a 
   value. A 'Required' flag will display as a prompt

-  If you check 'Important', the field will generate a warning if it is not 
   filled, but unlike 'Mandatory', you will still be able to save your record 
   nonetheless

-  If you add default values for indicators here these will be pre-filled to 
   save time when cataloguing but can still be edited if required

-  'Authorized value' is where you define an :ref:`authorized value 
   <authorized-values-label>` pull down list for your catalogers

   **Note**

   The authorized value option at field level does not work.

.. _edit-a-marc-subfield-label:

Edit a MARC subfield
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

To edit the **subfields** associated with the tag, click 'Actions' then 'Edit 
subfields' to the right of the tag on the framework field list. Each subfield 
has its own tab which contains three sections - Basic constraints, Advanced 
constraints and Other options.

-  For each subfield you can set the following basic constraint options

   |image190|

   -  Subfield code: this is the MARC subfield code, this wouldn't normally be 
      changed

   -  Text for librarian: what appears before the subfield in the staff 
      interface

   -  Text for OPAC: what appears before the field in the OPAC

         -  If left empty, the text for librarian is used instead

   -  Repeatable: the field will have an icon next to it allowing you to add
      multiples of the subfield

   -  Mandatory: the record cannot be saved unless you have a value assigned 
      to this subfield. A 'Required' flag will display as a prompt

   -  Important: this indicates that a field is not mandatory, but important. 
      If you try to save a record where an important field is empty, you will 
      get a warning, but the record will still be saved. 

   -  Managed in tab: defines the tab where the subfield is shown.

         **Important**

         All subfields of a given field must be in the same tab or ignored. 
         Ignore means that the subfield is not managed.

         **Important**

         When :ref:`importing records<stage-marc-records-for-import-label>`, 
         subfields that are managed in tab 'ignore' will be deleted. If you 
         still wish to keep the subfields, but hide them, use the 'Visibility' 
         options below.

-  For each subfield you can set the following advanced constraint options

   -  Default value: defines what you want to appear in the field by default, 
      this will be editable, but it saves time if you use the same text over 
      and over or the same value in a field often.

      **Note**
    
      There are several values that you can use here that will be replaced 
      automatically when a new record is created:
             
      -  <<MM>> - the current month, 2 digits

      -  <<DD>> - the current day of month, 2 digits

      -  <<YEAR>> - the current year, 4 digits

      -  <<USER>> - the username of the currently logged in user
             
      For example: a default of "<<MM>>/<<DD>>/<<YEAR>>" 
      (without quotes) will print the current date in the form of
      "01/21/2021"

   -  Visibility: allows you to select from where this subfield is
      visible/hidden, simply check the boxes where you would like the
      field to show and uncheck the boxes where you would like it
      hidden.

      **Note**

      The Editor tickbox controls whether this subfield will display within
      cataloguing editor for this framework. If you tick Collapsed the
      subfield will be hidden in the editor but will be displayed if
      the field label is clicked to expand all subfields

      |image192|

   -  Is a URL: if checked, it means that the subfield is a URL and can be
      clicked

   -  Link: if you enter an index name here, a link appears after
      the subfield in the MARC detail view in the staff interface.
      If the librarian clicks on the link, a catalog search is done using
      the index and the content of the subfield.

   -  Koha link: this field is used to create a link between the MARC subfield
      and a column in the items, biblioitems and biblio database
      tables. Whenever a record is added or changed, this mapping
      will be used to update the linked database column. The information
      from the database columns is used as a way to quickly look up
      important information without having to parse the full MARC record.
      It is used for displaying information in a lot of pages and can
      also be used in reports.

      It is possible to map multiple MARC subfields to the same database
      column. The first existing mapped subfield will be saved into the 
      database. Usage example: For a MARC21 installaton with both RDA and AACR2 
      records where some records store the publication data 
      in 260 and others in 264 both fields can be mapped to the database
      columns for publisher, publication date and publication year.

      The mappings can be changed on this page or from the
      :ref:`Koha to MARC mapping <koha-to-marc-mapping-label>` page.

      **Warning**

      The Koha links should not be changed after data has been added to
      your catalog. If you need to change or improve them, you must ask
      your system administrator to run misc/batchRebuildBiblioTables.pl.
      This will update the values in the database columns for all your
      records.

-  For each subfield you can set the following Other option values

   -  Authorized value: means the value cannot by typed, but must be
      chosen from a pull down generated by the :ref:`authorized
      value <authorized-values-label>` list

      In the example above, the 504a field will show the MARC504
      authorized values when cataloging

      |image194|

   -  Thesaurus: means that the value is not free text, but must be searched in
      the authority/thesaurus of the selected category

   -  Plugin: means the value is calculated or managed by a plugin. Plugins
      can do almost anything.

      -  Examples:

         -  For call numbers there is an option to add a call number
            browser next to the the call number subfield so that you can
            identify which call numbers are in use and which are not.
            Simply choose the cn\_browser.pl plugin. Learn more in the
            :ref:`cataloging section <adding-items-label>` of this manual.

         -  If you'd like to let file uploads via cataloging you can
            choose the upload.pl plugin and this will allow you to
            :ref:`upload files to Koha to link to your
            records <attaching-files-to-records-label>`.

         -  In UNIMARC there are plugins for every 1xx fields that are
            coded fields. The plugin is a huge help for cataloger! There
            are also two plugins (unimarc\_plugin\_210c and
            unimarc\_plugin\_225a that can "magically" find the editor
            from an ISBN, and the collection list for the editor)

         -  If you would like to enable an autocomplete search for publishers 
            in 260b and 264b you can set the plugin to marc21_field_260b.pl.  When you start 
            typing in a publisher name you will be given search results based on publisher 
            names already in the catalogue.

-  To save your changes simply click the 'Save changes'.

.. _add-fields-to-frameworks-label:

Add fields to frameworks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If a framework doesn't contain a field that you require you may need to add it.
To add a field to a framework click the 'New tag' button at the top of
the framework definition

|image186|

This will open up a blank form for entering MARC field data

|image187|

Enter the information about your new tag:

-  The 'Tag' is the MARC field number

-  The 'Label for lib' is the text that will appear in the staff interface
   when in the cataloging module

-  The 'Label for OPAC' is the text that will appear in the OPAC when
   viewing the MARC version of the record

-  If this field can be repeated, check the 'Repeatable' box

-  If this field is mandatory, check the 'Mandatory' box

-  If this field is not mandatory but is important, check the 'Important' box

   -  If the important field is not filled upon saving the record, there will 
      be a warning, but the user will still be able to save the record

-  You can enter default values for indicators in the 'First indicator default 
   value' and 'Second indicator default value' field

-  If you want this field to be a pull down with limited possible
   answers, choose which 'Authorized value' list you want to use
   
   **Note**

   The authorized value option at field level does not work.

When you're finished, click 'Save changes' and your new tag will be displayed 
in the framework field list.

|image188|

You will need to add at least one subfield to your new tag before it will appear 
in your framework when you are cataloguing.

Click on the 'Actions' button for your new tag and then 'Edit subfields'.  Click on the 'New' tab and enter your
subfield code.  The process for entering the remainder of the settings for the new subfield 
is the same as those found in the :ref:`editing fields and subfields in 
frameworks <edit-framework-fields-and-subfields-label>` section of this manual.

.. _import/export-frameworks-label:

Import/export frameworks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Next to each framework is a link to either import or export the
framework.

.. _export-framework-label:

Export framework
''''''''''''''''''''''''''''''''''''''''

To export a framework simply click the 'Export' link to the right of
framework title.

|image195|

When you click 'Export' you will be prompted to choose what format to
export the file in.

|image196|

A framework exported this way can be imported into any other Koha
installation using the import framework option.

.. _import-framework-label:

Import framework
''''''''''''''''''''''''''''''''''''''''

An easy way to create a new framework is to import one created for your
or another Koha installation. This framework would need to be exported
from the other system :ref:`using the instructions
above <export-framework-label>` to be available for import here.

To import a framework you first need to create :ref:`a new
framework <add-new-framework-label>`. Once you have that framework, click
Actions then 'Import' to the right of the new framework.

|image197|

You will be prompted to find a file on your computer to import into the
framework.

|image198|

You will be asked to confirm your actions before the file is imported.

|image199|

As your file is uploaded you will see an image that will confirm that
the system is working.

|image200|

Once your import is complete you will be brought to the framework edit
tool where you can make any changes you need to the framework you
imported.

.. _koha-to-marc-mapping-label:

Koha to MARC mapping
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

While Koha stores the entire MARC record, it also stores common fields
for easy access in various tables in the database. Koha to MARC mapping
is used to tell Koha where to find these values in the MARC record. In
many cases you will not have to change the default values set by in this
tool on installation, but it is important to know that the tool is here
and can be used at any time.

-  *Get there:* More > Administration > Catalog > Koha to MARC mapping

The table shows all the database fields that can be mapped to MARC fields.

|image201|

To add a new mapping, click on the 'Add' button to the right of the
appropriate field.

|image202|

Write in the MARC field and subfield you would like to map, separated
by a comma, to this Koha field and click the 'OK' button.

    **Note**

    It is possible to link more than one MARC field to a database field.
    For example, you could link both 260$a and 264$a to the biblioitems.place
    field.

If you would like to clear the mapping for a database field, click
the 'Remove' button.

    **Note**

    All changes are immediate.

.. _marc-bibliographic-framework-test-label:

MARC bibliographic framework test
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Checks the MARC structure.

-  *Get there:* More > Administration > Catalog > MARC bibliographic
   framework test

If you change your MARC bibliographic framework it's recommended that
you run this tool to test for errors in your definition.

|image206|

.. _authority-types-label:

Authority types
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Authority types are basically MARC frameworks for authority records and
because of that they follow the same editing rules found in the :ref:`MARC
bibliographic frameworks <marc-bibliographic-frameworks-label>` section of this manual.
Koha comes with many of the necessary authority frameworks already
installed. To learn how to add and edit authority types, simply review
the :ref:`MARC bibliographic frameworks` section of this manual.

-  *Get there:* More > Administration > Catalog > Authority types

.. _classification-sources-label:

Classification sources
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Source of classification or shelving scheme are mapped to field 952$2 and
942$2 in Koha's :ref:`MARC bibliographic frameworks <marc-bibliographic-frameworks-label>` 
and stored in the items.cn\_source and biblioitems.cn\_source fields in the 
database.

-  *Get there:* More > Administration > Catalog > Classification sources

|image207|

Commonly used classification sources are:

-  ddc - Dewey Decimal Classification

-  lcc - Library of Congress Classification

If you chose to install classification sources during Koha's
installation, you would see other values too:

-  ANSCR (sound recordings)

-  SuDOC classification

-  Universal Decimal Classification

-  Other/Generic Classification

.. _adding/editing-classification-sources-label:

Adding/editing classification sources
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can add your own source of classification by using the 'New classification 
source' button. To edit use the 'Edit' button.

|image208|

When creating or editing:

-  Enter a code. The code is limited to 10 characters and must be unique.

.. Note::
   The code is not editable once it has been created.

-  Enter a description. The description is used in the drop-down lists in the 
   cataloging module.

-  Check the 'Source in use?' checkbox if you want the value to appear
   in the drop-down list for this category.

-  Select the appropriate :ref:`filing rule <classification-filing-rules-label>` 
   from the drop-down list. 

-  Select the appropriate :ref:`splitting rule <classification-splitting-rules-label>` 
   from the drop-down list.

.. _classification-filing-rules-label:

Classification filing rules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Filing rules determine the order in which items are placed on shelves. Filing 
rules normalize call numbers in order for Koha to be able to compare them and 
sort them in the right order.

For example, a Dewey call number such as '636.8/07 SHAW' will become 
'636_800000000000000_07_SHAW' in order to be sorted.

The sorted call number is saved in the items.cn\_sort or biblioitems.cn\_sort 
fields in the database

Values that are pre-configured in Koha are:

-  Dewey

-  LCC

-  Generic

Filing rules are mapped to 
:ref:`Classification sources <adding/editing-classification-sources-label>`. 
You can setup new filing rules by using the 'New filing rule' button. To edit, 
use the 'Edit' button.

When creating or editing:

-  Enter a code. The code is limited to 10 characters and must be unique.

.. Note::
   The code is not editable once it has been created.

-  Enter a description. The description is used in the drop-down list when 
   :ref:`creating or editing a classification source <adding/editing-classification-sources-label>`.

-  Choose an appropriate filing routine - dewey, generic or lcc

   -  The Dewey filing routine generates a sorted call number by following 
      these rules:

      -  Concatenates classification and item parts.

      -  Converts to uppercase.

      -  Removes any leading or trailing whitespaces, and forward slashes (\/)

      -  Separates alphabetic prefix from the rest of the call number

      -  Splits into tokens on whitespaces and periods.

      -  Leaves first digit group as is.

      -  Converts second digit group to 15-digit long group, padded on right 
         with zeroes.

      -  Converts each whitespace to an underscore.

      -  Removes any remaining non-alphabetical, non-numeric, non-underscore 
         characters.

   -  The generic filing routine generates a sorted call number by following 
      these rules:
      
      -  Concatenates classification and item parts.

      -  Removes any leading or trailing whitespaces.

      -  Converts each whitespace to an underscore.

      -  Converts to uppercase.

      -  Removes non-alphabetical, non-numeric, non-underscore characters.

   -  The LCC filing routine generates a sorted call number by following 
      these rules:

.. I need help here, I can't read the code. CCLR 2020-12-08

      -  

      -  



.. _classification-splitting-rules-label:

Classification splitting rules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Splitting rules determine how call numbers are split when printed on a spine 
label.

.. Note::
   Splitting rules are only used if your :ref:`label layout <label-layouts-label>` 
   specifies to split call numbers.

For example, a Dewey call number such as '636.8/07 SHAW' will become 
::

   636.807
   SHAW

once printed on a spine label.

Values that are pre-configured in Koha are:

-  Dewey

-  LCC

-  Generic

Splitting rules are mapped to 
:ref:`Classification sources <adding/editing-classification-sources-label>`. 
You can setup new splitting rules by using the 'New splitting rule' button. To 
edit, use the 'Edit' button.

When creating or editing:

-  Enter a code. The code is limited to 10 characters and must be unique.

.. Note::
   The code is not editable once it has been created.

-  Enter a description. The description is used in the drop-down list when 
   :ref:`creating or editing a classification source <adding/editing-classification-sources-label>`.

-  Choose an appropriate splitting routine - Dewey, Generic, LCC or RegEx

   -  The Dewey splitting routine looks for the three digits and the decimal, 
      puts it on one line with the other parts (Cutter, prefix, etc.) each on 
      a separate line (generally split on spaces).

   -  The Generic splitting routine splits on spaces.

   -  The LCC splitting routine puts each component on a separate line.

   -  The RegEx splitting routine allows you to create a custom splitting 
      routine.

      -  Some examples of RegEx splitting routines:

         -  Split on spaces::

             s/\s/\n/g         

         -  Split on equal signs (=)::

             s/(\s?=)/\n=/g

         -  Split on forward slashes (\/)::

             s/(\s?\/)/\n/g

         -  Remove first split if call number starts with J or K::

             s/^(J|K)\n/$1 /

         -  Cut after 9 characters::

             s/(^.{9})/$1\n/


It is possible to mix and match RegEx splitting routines by clicking the 
'New' link just under the RegEx input box.

For example, if you want to cut after nine characters AND split on spaces, 
you can write both and the call number '971.42805092 C669r' will be split

::

  971.42805
  092
  C669r

|multipleregexsplittingrule|

.. _record-matching-rules-label:

Record matching rules
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Record matching rules are used when importing MARC records into Koha.

-  *Get there:* More > Administration > Catalog > Record matching rules

The rules that you set up here will be referenced with you :ref:`Stage MARC
records for import <stage-marc-records-for-import-label>`.

It is important to understand the difference between 'Match points' and
'Match checks' before adding new matching rules to Koha.

Match points are the criteria that you enter that must be met in order
for an incoming record to match an existing MARC record in your catalog.
You can have multiple match points on an import rule each with its own
score. An incoming record will be compared against your existing records
('one record at a time') and given a score for each match point. When
the total score of the match points matches or exceeds the threshold
given for the matching rule, Koha assumes a good match and
imports/overlays according your specifications in the import process. An
area to watch out for here is the sum of the match points. Double check
that the matches you want will add up to a successful match.

Example:

Threshold of 1000

Match point on 020$a 1000

Match point on 022$a 1000

Match point on 245$a 500

Match point on 100$a 100

In the example above, a match on either the 020$a or the 022$a will
result in a successful match. A match on 245$a title and 100$a author
(and not on 020$a or 022$a) will only add up to 600 and not be a match.
And a match on 020$a and 245$a will result in 1500 and while this is a
successful match, the extra 500 point for the 245$a title match are
superfluous. The incoming record successfully matched on the 020$a
without the need for the 245$a match. However, if you assigned a score
of 500 to the 100$a Match Point, a match on 245$a title and 100$a author
will be considered a successful match (total of 1000) even if the 020$a
is not a match.

Match checks are not commonly used in import rules. However, they can
serve a couple of purposes in matching records. First, match checks can
be used as the matching criteria instead of the match points if your
indexes are stale and out of date. The match checks go right for the
data instead of relying on the data in the indexes. (If you fear your
indexes are out of date, a rebuild of your indexes would be a great idea
and solve that situation!) The other use for a match check is as a
'double check' or 'veto' of your matching rule. For example, if you have
a matching rule as below:

Threshold of 1000

Match point on 020$a 1000

Match check on 245$a

Koha will first look at the 020$a tag/subfield to see if the incoming
record matches an existing record. If it does, it will then move on to
the Match Check and look directly at the 245$a value in the incoming
data and compare it to the 245$a in the existing 'matched' record in
your catalog. If the 245$a matches, Koha continues on as if a match was
successful. If the 245$a does not match, then Koha concludes that the
two records are not a match after all. The Match Checks can be a really
useful tool in confirming true matches.

When looking to create matching rules for your authority records the
following indexes will be of use:

+--------------------------+--------------------+
| Index name               | Matches MARC tag   |
+==========================+====================+
| LC-cardnumber            | 010$a              |
+--------------------------+--------------------+
| Personal-name            | 100$a              |
+--------------------------+--------------------+
| Corporate-name-heading   | 110$a              |
+--------------------------+--------------------+
| Meeting-name             | 111$a              |
+--------------------------+--------------------+
| Title-uniform            | 130$a              |
+--------------------------+--------------------+
| Chronological-term       | 148$a              |
+--------------------------+--------------------+
| Subject-topical          | 150$a              |
+--------------------------+--------------------+
| Name-geographic          | 151$a              |
+--------------------------+--------------------+
| Term-genre-form          | 155$a              |
+--------------------------+--------------------+

Table: Authority indexes

.. _adding-matching-rules-label:

Adding matching rules
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To create a new matching rule :

-  Click 'New record matching rule'

   |image209|

   -  Choose a unique name and enter it in the 'Matching rule code'
      field

   -  'Description' can be anything you want to make it clear to you
      what rule you're picking

   -  'Match threshold' is the total number of 'points' a biblio must
      earn to be considered a 'match'

   -  'Record type' is the type of import this rule will be used for -
      either authority or bibliographic

   -  Match points are set up to determine what fields to match on

   -  'Search index' can be found by looking at the index configuration
      on your system. For Zebra you might find the right index names
      in your ccl.properties file. You can also find useful information in
      the :ref:`Koha Search Indexes` chapter of this manual.

   -  'Score' - The number of 'points' a match on this field is worth.
      If the sum of each score is equal or greater than the match threshold, the
      incoming record is a match to the existing record.

   -  Enter the MARC tag you want to match on in the 'Tag' field.

   -  Enter the MARC tag subfield you want to match on in the
      'Subfields' field. For matching on controlfields like 001 the subfields
      input field can be left empty.

   -  'Offset' - For use with control fields, 001-009

   -  'Length' - For use with control fields, 001-009

   -  There are currently several options for 'Normalization rules':

      - None - no normalization rule will be applied

      - Remove spaces

      - Uppercase

      - Lowercase

      - Legacy default - this option was added to maintain the behaviour
        form before the other normalization rules became available.

      - ISBN - using this option will improve matching on ISBN. If your
        incoming records ISBN fields contain extra text, like
        '9780670026623 (alk. paper)', they will still match correctly.

   -  'Required match checks' - While match points work on the search
      index, match checks work directly on the data and can be used
      as the matching criteria instead of the match points or in addition
      to them to confirm true matches.

.. _sample-bibliographic-record-matching-rule-control-number-label:

Sample bibliographic record matching rule: Control number
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|image210|

-  Match threshold: 100

-  Record type: Bibliographic

   -  **Note**

          If you'd like a rule to match on the 001 in authority records
          you will need the repeat all of these values and change just
          the record type to 'Authority record'

-  Matchpoints (just the one):

-  Search index: Control-number

-  Score: 100

-  Tag: 001

   -  **Note**

          this field is for the control number assigned by the
          organization creating, using, or distributing the record

-  Subfields: empty

-  Offset: 0

-  Length: 0

-  Normalization rule: None

-  Required match checks: none (remove the blank one)

   |image211|

.. _oai-sets-configuration-label:

OAI sets configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

On this page you can create, modify and delete OAI-PMH sets

.. _create-a-set-label:

Create a set
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To create a set:

-  Click on the link 'Add a new set'

-  Fill the mandatory fields 'setSpec' and 'setName'

-  Then you can add descriptions for this set. To do this click on 'Add
   description' and fill the newly created text box. You can add as many
   descriptions as you want.

-  Click on 'Save' button'

.. _modify/delete-a-set-label:

Modify/delete a set
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To modify a set, just click on the link 'Modify' on the same line of the
set you want to modify. A form similar to set creation form will appear
and allow you to modify the setSpec, setName and descriptions.

To delete a set, just click on the link 'Delete' on the same line of the
set you want to delete.

.. _define-mappings-label:

Define mappings
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here you can define how a set will be build (what records will belong to
this set) by defining mappings. Mappings are a list of conditions on
record content.

-  Fill the fields 'Field', 'Subfield' and 'Value'. For example if you
   want to include in this set all records that have a 999$9 equal to
   'XXX'. Fill 'Field' with 999, 'Subfield' with 9 and 'Value' with XXX.

-  If you want to add another condition, click on 'Add' button and repeat
   step 1. You can choose between 'and' or 'or' boolean operators to link 
   your conditions.

-  Click on 'Save'

To delete a condition, just leave at least one of 'Field', 'Subfield' or
'Value' empty and click on 'Save'.

    **Note**

    Actually, a condition is true if value in the corresponding subfield
    is strictly equal to what is defined if 'Value'. A record having
    999$9 = 'XXX YYY' will not belong to a set where condition is 999$9
    = 'XXX'.

And it is case sensitive : a record having 999$9 = 'xxx' will not belong
to a set where condition is 999$9 = 'XXX'.

.. _build-sets-label:

Build sets
^^^^^^^^^^^^^^^^^^^^^^^^^^

Once you have configured all your sets, you have to build the sets. This
is done by calling the script misc/migration\_tools/build\_oai\_sets.pl.

.. _item-search-fields-label:

Item search fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

From here you can add custom search fields to the :ref:`item
search <item-searching-label>` option in the staff client.

    |image1205|

To add a new search term simply click the 'New search field' button

    |image1206|

-  Name is a field for you to identify the search term

-  Label is what will appear on the item search page

-  MARC field allows you to pick which field you'd like to search in

-  MARC subfield is the subfield you'd like to search in

-  Authorised values category can be used to turn this search field in
   to a pull down instead of a free text field

Once your new field is added it will be visible at the top of this page
and on the item search page

    |image1207|

.. _search-engine-configuration:

Search engine configuration
----------------------------
Once you have switched to Elasticsearch in your SearchEngine system preference,
you’ll see a new link for Search engine configuration in the Catalog section of 
Administration. Here you will manage indexes, facets, and their mappings to MARC
fields and subfields.

.. _acquisitions-module-label:

Acquisitions
----------------------------

The Koha Acquisitions module provides a way for the library to record
orders placed with vendors and manage purchase budgets.

Before using the `Acquisitions Module <#acqmodule>`__, you will want to
make sure that you have completed all of the set up.

-  *Get there:* More > Administration > Acquisitions

.. _currencies-and-exchange-rates-label:

Currencies and exchange rates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you place orders from more than one country you will want to input
currency exchange rates so that your acquisitions module will properly
calculate totals.

-  *Get there:* More > Administration > Acquisitions > Currencies and
   exchange rates

|image212|

    **Note**

    This data is not automatically updated, so be sure to keep it up to
    date so that your accounting is kept correct.

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: currency).

The ISO code you enter will be used when importing MARC files via the
staging tools, the tool will attempt to find and use the price of the
currently active currency.

The active currency is the main currency you use in your library. Your
active currency will have a check mark in the 'Active' column. If you
don't have an active currency you will see an error message telling you
to choose an active currency.

|image213|

.. _budgets-label:

Budgets
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Budgets are used for tracking accounting values related to acquisitions.
For example you could create a budget for the current year (ex. 2015)
and then break that into :ref:`Funds` for different areas of the
library (ex. Books, Audio, etc).

-  *Get there:* More > Administration > Acquisitions > Budgets

When visiting the main budget administration you will see two tabs, one
for active and one for inactive budgets.

|image214|

.. _adding-budgets-label:

Adding budgets
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Budgets can either be created :ref:`from scratch <add-a-new-budget-label>`, by
:ref:`duplicating the previous year's budget <duplicate-a-budget-label>` or by
:ref:`closing a previous year's budget <close-a-budget-label>`.

.. _add-a-new-budget-label:

Add a new budget
''''''''''''''''''''''''''''''''''''

If you haven't used Koha before for acquisitions then you'll need to
start fresh with a new budget. To add a new budget click the 'New
budget' button.

|image215|

-  Choose the time period this budget is for, whether it's an academic
   year, a fiscal year, a quarter, etc.

-  The description should be something that will help you identify the
   budget when ordering

-  In the amount box do not use any symbols, simply enter the amount of
   the budget with numbers and decimals.

-  Marking a budget active makes it usable when placing orders in the
   acquisitions module, even if the order is placed after the budget end
   date. This will allow you to record orders that were places in a
   previous budget period.

-  Locking a budget means that funds will not be able to be modified by
   librarians

Once you have made your edits, click the 'Save changes' button. You will
be brought to a list of your existing budgets.

|image216|

.. _duplicate-a-budget-label:

Duplicate a budget
'''''''''''''''''''''''''''''''''''''''''

To duplicate a budget from a previous year, click on the link for the
budget name from the list of budgets

|image217|

On the screen listing the budget breakdown click the 'Edit' button at the
top and choose to 'Duplicate budget'

|image218|

You can also click the 'Actions' button to the right of the budget and
choose 'Duplicate'.

|image1208|

In both cases you will be presented with a form where you simply need to
enter the new start and end date and save the budget.

|image219|

Check the box for 'Mark the original budget as inactive' if the original
budget should no longer be used.

Check the box for 'Set all funds to zero' if you wish the new budget to
contain all the same fund structures as the previous budget but no
allocations until you manually enter an amount in the fund.

This will not only duplicate your budget, but all of the funds
associated with that budget so that you can reuse budgets and funds from
year to year and so that you can move unreceived orders and if desired
unspent funds from a previous budget to the new budget.

.. _close-a-budget-label:

Close a budget
'''''''''''''''''''''''''''''''''

Close a budget to move or roll over unreceived orders and if desired
unspent funds from a previous budget to a new budget. Before closing
your budget you might want to :ref:`duplicate the previous year's
budget <duplicate-a-budget-label>` so that you have somewhere for the
unreceived orders to roll to.

Find the previous budget with unreceived orders on the Active budgets or
the Inactive budgets tab and select 'Close' under 'Actions'.

    |image1209|

    **Note**

    In order for the unreceived orders to be automatically moved to the
    new budget, the fund structures in the previous budget must exist in
    the new budget. Budgets without unreceived orders cannot be closed.

When you select 'Close' you will be presented with a form.

    |image1210|

Use the 'Select a budget' drop down to choose the new budget for the
unreceived orders.

Check the box for 'Move remaining unspent funds' to move the unspent
amounts from the funds of the budget being closed to the selected
budget.

Once you have made your choices, click the 'Move unreceived orders'
button. You will be presented with a dialog box that says 'You have
chosen to move all unreceived orders from 'Budget X' to 'Budget Y'. This
action cannot be reversed. Do you wish to continue?' Budget X is the
budget to be closed and Budget Y is the selected budget.

    |image1211|

If everything seems correct click 'OK' and the unreceived orders and, if
selected, unspent funds will be moved.

Wait until the 'Report after moving unreceived orders from budget X to
Y' displays. This will list the order numbers which have been impacted
(grouped by fund) and detail if the unreceived order was moved or if
there was a problem. For example, if the new budget does not contain a
fund with the same name as the previous budget, the order will not be
moved.

|image220|

.. _funds-label:

Funds
~~~~~~~~~~~~~~~~~~

-  *Get there:* More > Administration > Acquisitions > Funds

.. _add-a-fund-label:

Add a Fund
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A fund is added to a budget.

    **Important**

    A :ref:`budget <adding-budgets-label>` must be defined before a fund can be
    created.

To add a new fund click the 'New' button and then choose which budget you
would like to add the fund to.

|image221|

In the form that appears you want to enter the basics about your fund.

|image222|

The three first fields are required, the rest are optional

-  Fund code is a unique identifier for your fund

-  The fund name should be something that librarians will understand

-  Amount should be entered with only numbers and decimals, no other
   characters

-  Warning at (%) or Warning at (amount) can be filled in to make Koha
   warn you before you spend a certain percentage or amount of your
   budget. This will prevent you from overspending.

-  You can choose to assign this fund to a librarian. Doing so will make
   it so that only that librarian can make changes to the fund

-  Choose which library will be using this fund

-  You can restrict who can order from this fund by choosing either the
   'owner', 'owner and users' or 'owner, users and library' from the
   'Restrict access to' menu

   |image223|

   -  **Important**

          Without an owner, the access restriction will be ignored, be
          sure to enter an owner as well as choose a restriction

-  Notes are simply for any descriptive notes you might want to add so
   that librarians know when to use this fund

-  Planning categories are used for statistical purposes. If you will be
   using the Asort1 and/or Asort2 authorised values lists to track your orders
   you need to select them when setting up the fund.  Select the Asort1/Asort2
   option from the dropdown lists for the Statiscal 1 done on: and
   Statistical 2 done on: fields.

-  To learn more about planning categories, check out the :ref:`Planning category FAQ <faq-planning-categories-label>`.

When complete, click 'Submit' and you will be brought to a list of all
of the funds for the budget.

|image224|

The monetary columns in the fund table break down as follows:

1. Base-level allocated is the 'Amount' value you defined when creating
   the fund

2. Base-level ordered is the ordered amount for this fund (without child
   funds)

3. Total ordered is the base-level ordered for this fund and all its
   child funds

4. Base-level spent is the spent amount for this fund (without child
   funds)

5. Total spent is the base-level spent for this fund and all its child
   funds

6. Base-level available is 1 - 2

7. Total available is 1 - 3

To the right of each fund you will find the 'Actions' button under which
you will find the 'Edit,' 'Delete,' and 'Add child fund' options.

|image225|

A child fund simply a sub-fund of the fund listed. An example would be
to have a fund for 'Fiction' and under that have a fund for 'New
releases' and a fund for 'Science Fiction.' It is an optional way to
further organize your finances.

Funds with children will show with a small arrow to the left. Clicking
that will show you the children funds.

|image226|

.. _budget-planning-label:

Budget planning
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When viewing the list of funds click the 'Planning' button and choose
how you would like to plan to spend your budget.

|image227|

If you choose 'Plan by MONTHS' you will see the budgeted amount broken
down by months:

|image228|

To hide some of the columns you can click the 'hide' link to the right
(or below as in the screenshot above) the dates. To add more columns you
can click the 'Show a column' link found below the 'Fund remaining'
heading.

|image229|

From here you can plan your budget spending by manually entering values
or by clicking the 'Auto-fill row' button. If you choose to auto-fill
the form the system will try to divide the amount accordingly, you may
have to make some edits to split things more accurately.

|image230|

Once your changes are made, click the 'Save' button. If you would like
to export your data as a CSV file you can do so by entering a file name
in the 'Output to a file named' field and clicking the 'Output' button.

|image231|

.. _edi-accounts-label:

EDI accounts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

From here you can set up the information needed to connect to your
acquisitions vendors.

    **Note**

    Before you begin you will need at least one :ref:`Vendor set up in
    Acquisitions <add-a-vendor-label>`.

To add account information click the 'New account' button.

    |image1212|

In the form that appears you will want to enter your vendor information.

New account information

Each vendor will have one account.

.. _library-eans-label:

Library EANs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A library EAN is the identifier the vendor gives the library to send
back to them so they know which account to use when billing. One EDI
account can have multiple EANs.

To add an EAN click the 'New EAN' button.

New EAN

In the form that appears enter the information provided by your vendor.

New EAN form

.. _additional-parameters-label:

Additional parameters
--------------------------------------------

-  *Get there:* More > Administration > Additional parameters

.. _z39.50/sru-servers-label:

Z39.50/SRU servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Z39.50 is a client/server protocol for searching and retrieving
information from remote computer databases, in short it's a tool used
for copy cataloging.

SRU- Search/Retrieve via URL - is a standard XML-based protocol for
search queries, utilizing CQL - Contextual Query Language - a standard
syntax for representing queries.

Using Koha you can connect to any Z39.50 or SRU target that is publicly
available or that you have the log in information to and copy both
bibliographic and/or authority records from that source.

-  *Get there:* More > Administration > Additional parameters >
   Z39.50/SRU servers

Koha comes with a default list of Z39.50/SRU targets set up that you can
add to, edit or delete

|image232|

To find additional Z39.50 targets you use IndexData's IRSpy:
`http://irspy.indexdata.com <http://irspy.indexdata.com/>`__ or the
Library of Congress's list of targets http://www.loc.gov/z3950/

.. _add-a-z39.50-target-label:

Add a Z39.50 target
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

-  From the main Z39.50 page, click 'New Z39.50 server'

   |image233|

   -  'Z39.50 server' should be populated with a name that will help you
      identify the source (such as the library name).

   -  'Hostname' will be the address to the Z39.50 target.

   -  'Port' tells Koha what port to listen on to get results from this
      target.

   -  'Userid' and 'Password' are only required for servers that are
      password protected.

   -  Check the 'Preselected' box if you want this target to always be
      selected by default.

   -  'Rank' lets you enter where in the list you'd like this target to
      appear.

      -  If this is left blank the targets will be in alphabetical
         order.

   -  'Attributes' lets you define PQF attributes to be added to all queries.

   -  'Syntax' is the MARC flavor you use.

   -  'Encoding' tells the system how to read special characters.

   -  'Timeout' is helpful for targets that take a long while. You can
      set the timeout so that it doesn't keep trying the target if
      results aren't found in a reasonable amount of time.

   -  'Record type' lets you define if this is a bibliographic or an
      authority target.

   -  'XSLT file(s)' lets enter one or more (comma-separated) XSLT file
      names that you want to apply on the search results.

      -  When retrieving records from external targets you may wish to
         automate some changes to those records. XSLT's allow you to do
         this. Koha ships with some sample XSLT files in the
         /koha-tmpl/intranet-tmpl/prog/en/xslt/ directory ready for use:

         -  Del952.xsl: Remove items (MARC21/NORMARC)

         -  Del995.xsl: Remove items (UNIMARC)

         -  Del9LinksExcept952.xsl: Remove $9 links. Skip item fields
            (MARC21/NORMARC)

         -  Del9LinksExcept995.xsl: Remove $9 links. Skip item fields
            (UNIMARC)

.. _suggested-bibliographic-z39.50-targets-label:

Suggested bibliographic Z39.50 targets
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Koha libraries with open Z39.50 targets can share and find connection
information on the Koha wiki:
http://wiki.koha-community.org/wiki/Koha_Open_Z39.50_Sources. You can
also find open Z39.50 targets by visiting IRSpy:
http://irspy.indexdata.com.

The following targets have been used successfully by other Koha
libraries (in the Americas):

-  ACCESS PENNSYLVANIA 205.247.101.11:210 INNOPAC

-  CUYAHOGA COUNTY PUBLIC webcat.cuyahoga.lib.oh.us:210 INNOPAC

-  GREATER SUDBURY PUBLIC 216.223.90.51:210 INNOPAC

-  HALIFAX PUBLIC catalogue.halifaxpubliclibraries.ca:210 horizon

-  HALTON HILLS PUBLIC cat.hhpl.on.ca:210 halton\_hills

-  LIBRARY OF CONGRESS lx2.loc.gov: 210 LCDB

-  LONDON PUBLIC LIBRARY catalogue.londonpubliclibrary.ca:210 INNOPAC

-  MANITOBA PUBLIC library.gov.mb.ca:210 horizon

-  MILTON PL cat.mpl.on.ca:210 horizon

-  NATIONAL LIBRARY OF WALES cat.llgc.org.uk:210 default

-  NHUPAC 199.192.6.130:211 nh\_nhupac

-  OCEAN STATE LIBRARIES (RI) catalog.oslri.net:210 INNOPAC

-  OHIOLINK olc1.ohiolink.edu:210 INNOPAC

-  PUBCAT prod890.dol.state.vt.us:2300 unicorn

-  SAN JOAQUIN VALLEY PUBLIC LIBRARY SYSTEM (CA) hip1.sjvls.org:210
   ZSERVER

-  SEATTLE PUBLIC LIBRARY ZSERVER.SPL.ORG:210 HORIZON

-  TORONTO PUBLIC symphony.torontopubliclibrary.ca:2200 unicorn

-  TRI-UNI 129.97.129.194:7090 voyager

-  VANCOUVER PUBLIC LIBRARY z3950.vpl.ca:210 Horizon

.. _suggested-authority-z39.50-targets-label:

Suggested Authority Z39.50 Targets
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The following targets have been used successfully by other Koha
libraries (in the Americas):

-  LIBRARIESAUSTRALIA AUTHORITIES
   z3950-test.librariesaustralia.nla.gov.au:210 AuthTraining Userid:
   ANLEZ / Password: z39.50

-  LIBRARY OF CONGRESS NAME AUTHORITIES lx2.loc.gov:210 NAF

-  LIBRARY OF CONGRESS SUBJECT AUTHORITIES lx2.loc.gov:210 SAF

.. _add-a-sru-target-label:

Add a SRU target
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

-  From the main Z39.50/SRU page, click 'New SRU server'

   |image234|

   -  'Server name' should be populated with a name that will help you
      identify the source (such as the library name).

   -  'Hostname' will be the address to the Z39.50 target.

   -  'Port' tells Koha what port to listen on to get results from this
      target.

   -  'Userid' and 'Password' are only required for servers that are
      password protected.

   -  Check the 'Preselected' box if you want this target to always be
      selected by default.

   -  'Rank' lets you enter where in the list you'd like this target to
      appear.

      -  If this is left blank the targets will be in alphabetical
         order.

   -  'Syntax' is the MARC flavor you use.

   -  'Encoding' tells the system how to read special characters.

   -  'Timeout' is helpful for targets that take a long while. You can
      set the timeout so that it doesn't keep trying the target if
      results aren't found in a reasonable amount of time.

   -  'Additional SRU options' is where you can enter additional options
      of the external server here, like sru\_version=1.1 or
      schema=marc21, etc. Note that these options are server dependent.

   -  'SRU Search field mapping' lets you add or update the mapping from
      the available fields on the Koha search form to the specific
      server dependent index names.

      -  To further refine your searches, you could add the following
         index names to the SRU search field mappings. To do this, edit
         the server and click the Modify button next to this field.

         +---------------+---------------------------+
         | Title         | dc.title                  |
         +---------------+---------------------------+
         | ISBN          | bath.isbn                 |
         +---------------+---------------------------+
         | Any           | cql.anywhere              |
         +---------------+---------------------------+
         | Author        | dc.author                 |
         +---------------+---------------------------+
         | ISSN          | bath.issn                 |
         +---------------+---------------------------+
         | Subject       | dc.subject                |
         +---------------+---------------------------+
         | Standard ID   | bath.standardIdentifier   |
         +---------------+---------------------------+

         Table: SRU mapping

   -  'XSLT file(s)' lets enter one or more (comma-separated) XSLT file
      names that you want to apply on the search results.

      -  When retrieving records from external targets you may wish to
         automate some changes to those records. XSLT's allow you to do
         this. Koha ships with some sample XSLT files in the
         /koha-tmpl/intranet-tmpl/prog/en/xslt/ directory ready for use:

         -  Del952.xsl: Remove items (MARC21/NORMARC)

         -  Del995.xsl: Remove items (UNIMARC)

         -  Del9LinksExcept952.xsl: Remove $9 links. Skip item fields
            (MARC21/NORMARC)

         -  Del9LinksExcept995.xsl: Remove $9 links. Skip item fields
            (UNIMARC)

.. _did-you-mean?-label:

Did you mean?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*Get there:* More > Administration > Additional parameters > Did you
mean?

Koha can offer 'Did you mean?' options on searches based on values in
your :ref:`authorities <authorities-label>`.

    **Important**

    Did you mean? only works in the OPAC at this time. The intranet
    options are here for future development.

Using this page you can control which options Koha gives patrons on
their search results.

|image235|

To turn on the 'Did you mean?' bar on your search results you need to
check the box next to each plugin you would like to use. The two plugins
you have to choose from are:

-  The ExplodedTerms plugin suggests that the user try searching for
   broader/narrower/related terms for a given search (e.g. a user
   searching for "New York (State)" would click the link for narrower
   terms if they're also interested in "New York (City)"). This is only
   relevant for libraries with highly hierarchical authority data.

-  The AuthorityFile plugin searches the authority file and suggests the
   user might be interested in bibs linked to the top 5 authorities

If you want one plugin to take priority over another you simply drag it
above the other.

|image236|

If you choose both plugins you will see several options at the top of
your search results

|image237|

If you choose just the AuthorityFile you'll see just authorities.

|image238|

.. _column-settings-label:

Table settings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This administration area will help you hide or display columns on fixed
tables throughout the staff interface and OPAC.

-  *Get there:* Administration > Additional parameters > Table settings

|tablesettings|

Clicking on the module you'd like to edit tables for will show you the
options available to you.

This area lets you control the columns that show in the table in
question. If nothing is hidden you will see no check marks in the 'is
hidden by default' column.

|setcurrencynohide|

And will see all of the columns when viewing the table on its regular
page.

|currenciesnohide|

If columns are hidden they will have checks in the 'is hidden by
default' column.

|setcurrencyhide|

And hidden when you view the table.

|currencieshide|

The 'Cannot be toggled' column is used to prevent individual users from showing 
or hiding this column when viewing the table.

Individual users can toggle columns using the 'Columns' button at the
top of the table.

|togglecolumns|

For example, in the Currencies table, the 'Currency' and 'Rate' columns cannot 
be toggled. When the user clicks on the 'Columns' button, they are not able to 
choose whether these two columns are hidden or visible.

Note that using the 'Columns' button show or hide columns will only toggle them 
for the current user and session. Once the user logs out, the columns will go 
back to their default settings as set in the table settings administration 
page. It will not affect any other user.

+---------------------+--------------------------------------------------------------------------------------------------+
| Module              | Tables                                                                                           |
+=====================+==================================================================================================+
| Acquisitions        | - :ref:`Basket summary <create-a-basket-label>` (orders)                                         |
|                     | - :ref:`Order search results <acquisition-searches-label>` (histsearcht)                         |
|                     | - :ref:`Late orders <claims-and-late-orders-label>` (late\_orders)                               |
|                     | - :ref:`Suggestions <managing-purchase-suggestions-label>` (suggestions)                         |
+---------------------+--------------------------------------------------------------------------------------------------+
| Administration      | - :ref:`Patron categories <patron-categories-label>` (patron\_categories)                        |
|                     | - :ref:`Currencies <currencies-and-exchange-rates-label>` (currency)                             |
|                     | - :ref:`Item types <item-types-label>` (table\_item\_type)                                       |
|                     | - :ref:`Libraries <libraries-label>` (librairies)                                                |
+---------------------+--------------------------------------------------------------------------------------------------+
| Authorities         | There aren't any tables that can be configured from the                                          |
|                     | Authorities module.                                                                              |
+---------------------+--------------------------------------------------------------------------------------------------+
| Catalog             | - Acquisition details (acquisitiondetails-table)                                                 |
|                     | - Checkout history (checkoutshistory-table)                                                      |
|                     | - Holdings/items (holdings\_table)                                                               |
|                     | - Holdings/items from other libraries (otherholdings\_table)                                     |
|                     |   (when :ref:`SeparateHoldings <separateholdings-and-separateholdingsbranch-label>` is enabled)  |
+---------------------+--------------------------------------------------------------------------------------------------+
| Cataloging          | - :ref:`Item table above edit item form <adding-items-label>` (Items Editor)                     |
|                     | - :ref:`Z39.50 search results <adding-records-label>` (resultst)                                 |
+---------------------+--------------------------------------------------------------------------------------------------+
| Circulation         | - :ref:`Checkouts <checking-items-out-label>` (issues-table)                                     |
|                     | - :ref:`Patron search results <check-out-(issuing)-label>` (table\_borrowers)                    |
|                     | - :ref:`Holds to pull <holds-to-pull-label>` (holds-to-pull)                                     |
|                     | - :ref:`Holds awaiting pickup (holds waiting over X days) <holds-awaiting-pickup-label>` (holdso)|
|                     | - :ref:`Holds awaiting pickup (holds waiting) <holds-awaiting-pickup-label>` (holdst)            |
|                     | - :ref:`Hold ratios <hold-ratios-label>` (holds-ratios)                                          |
|                     | - :ref:`Overdues report <overdues-label>` (circ-overdues)                                        |
|                     | - :ref:`Checkins <checking-items-in-label>` (checkedintable)                                     |
|                     | - :ref:`Holds queue <holds-queue-label>` (holds-table)                                           |
+---------------------+--------------------------------------------------------------------------------------------------+
| Course reserves     | - :ref:`Courses <adding-courses-label>` (courses page, course\_reserves\_table)                  |
|                     | - :ref:`Reserves <adding-reserve-materials-label>` (reserves page, course\_reserves\_table)      |
+---------------------+--------------------------------------------------------------------------------------------------+
| Interlibrary loans  | - :ref:`Requests <viewing-ILL-requests-label>` (ill-requests)                                    |
+---------------------+--------------------------------------------------------------------------------------------------+
| Patrons             | - :ref:`Patron checkout history <circulation-history-label>` (checkouthistory-table)             |
|                     | - :ref:`Accounting > Transactions <fines-label>` (account-fines)                                 |
|                     | - :ref:`Holds history <holds-history-label>` (holdshistory-table)                                |
|                     | - :ref:`Patron search results <patron-search-label>` (memberresultst)                            |
|                     | - :ref:`Details > Checkouts <circulation-summary-label>` (issues-table)                          |
|                     | - :ref:`Patron lists <patron-lists-label>` (patron-list-table)                                   |
|                     | - :ref:`Accounting > Make a payment <pay-and-writeoff-fines-label>` (pay-fines-table)            |
+---------------------+--------------------------------------------------------------------------------------------------+
| Point of sale       | - :ref:`Point of sale <making-a-sale-label>` (invoices)                                          |
+---------------------+--------------------------------------------------------------------------------------------------+
| Tools               | - :ref:`Log viewer <log-viewer-label>` (logst)                                                   |
|                     | - :ref:`Notices and slips <notices-and-slips-label>` (lettert)                                   |
|                     | - :ref:`Stock rotation rotas <stock-rotation-label>` (stock\_rotation)                           |
|                     | - :ref:`Stock rotation items <stock-rotation-label>` (stock\_rotation\_manage\_items)            |
+---------------------+--------------------------------------------------------------------------------------------------+
| OPAC                | - :ref:`Course reserves <course-reserves-in-the-opac-label>` (course-items-table)                |
|                     | - :ref:`Courses <course-reserves-in-the-opac-label>` (course\_reserves\_table)                   |
|                     | - :ref:`Holdings/Items <bibliographic-record-label>` (holdingst)                                 |
|                     | - :ref:`Serials issues on subscription tab <bibliographic-record-label>` (subscriptionst)        |
+---------------------+--------------------------------------------------------------------------------------------------+
| Reports             | - :ref:`Items lost <lost-items-label>` (lostitems-table)                                         |
|                     | - :ref:`Orders by fund <orders-by-fund-label>` (funds-table)                                     |
|                     | - :ref:`Saved SQL reports <edit-custom-reports-label>` (table\_reports)                          |
+---------------------+--------------------------------------------------------------------------------------------------+
| Serials             | - :ref:`Acquisition details <subscriptions-in-staff-client-label>` (orders)                      |
+---------------------+--------------------------------------------------------------------------------------------------+

.. Note ::

  Patrons in the OPAC can't toggle column visibility. For OPAC tables
  this feature only allows to control the visibility of columns.

.. Note ::

  Any tables with columns listed here also have the option to export to Excel, export to CSV,
  copy, or print within the table header.

.. _audio-alerts-label:

Audio alerts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you have your :ref:`AudioAlerts` preference set to
'Enable' you will be able to control the various alert sounds that Koha
uses from this area.

-  *Get there:* More > Administration > Additional parameters > Audio
   alerts

Each dialog box in Koha has a CSS class assigned to it that can be used
as a selector for a sound.

    |image1213|

You can edit the defaults by clicking the 'Edit' button to the right of
each alert.

    |image1214|

You can assign alerts to other CSS classes in Koha by entering that
information in the selector box. For example if you enter

::

    body:contains('Check in message')

Then when you visit the checkin page you will hear an alert.

Every page in Koha has a unique ID in the body tag which can be used to
limit a sound to a specific page

Any ID selector (where HTML contains id="name\_of\_id" ) and can also be
a trigger as: #name\_of\_selector

.. _sms-cellular-providers-label:

SMS cellular providers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

    **Important**

    This option will only appear if the
    :ref:`smssenddriver-label` preference is set to 'Email'

From here you can enter as many cellular providers as you need to send
SMS notices to your patrons using the email protocol.

    |image1215|

Some examples in the US are:

+---------------------+-----------------------------+
| Mobile Carrier      | SMS Gateway Domain          |
+=====================+=============================+
| Alltel              | sms.alltelwireless.com      |
+---------------------+-----------------------------+
| AT&T                | txt.att.net                 |
+---------------------+-----------------------------+
| Boost Mobile        | sms.myboostmobile.com       |
+---------------------+-----------------------------+
| Project Fi          | msg.fi.google.com           |
+---------------------+-----------------------------+
| Republic Wireless   | text.republicwireless.com   |
+---------------------+-----------------------------+
| Sprint              | messaging.sprintpcs.com     |
+---------------------+-----------------------------+
| T-Mobile            | tmomail.net                 |
+---------------------+-----------------------------+
| U.S. Cellular       | email.uscc.net              |
+---------------------+-----------------------------+
| Verizon Wireless    | vtext.com                   |
+---------------------+-----------------------------+
| Virgin Mobile       | vmobl.com                   |
+---------------------+-----------------------------+

Table: SMS provider examples

To add new providers enter the details in the form and click 'Add new'
to save.

    |image1216|

These options will appear in the OPAC for patrons to choose from on the
:ref:`messaging tab <your-messaging-label>` if you have
:ref:`EnhancedMessagingPreferences`
enabled.

    |image1217|

.. _share-your-usage-statistics-label:

Share your usage statistics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can share your Koha usage statistics with the Hea community. Sharing your 
usage statistics helps with the development of Koha as the community regularly 
checks these statistics to make decisions.

Note that statistics are anonymized and no patron information is shared.

Worldwide statistics can be viewed at https://hea.koha-community.org/

|image1479|

-  Share my Koha usage statistics:

   -  The default choice is 'Undecided', this make the message appear on the 
      administration main page.

   -  Choose 'yes' if you want to share your usage statistics

   -  Choose 'no' if you don't want to share your statistics and you don't want 
      to see the message on the administration page

-  Your country: choose the country where your library is located

-  Library name: enter your library's name

-  Library type: choose your library's type

-  Library URL: enter your library's Web site URL

-  Last update: here your will see the last date when your data was uploaded 
   to the Hea website

-  Geolocation: use the map on the right to put the marker where your main 
   library is situated. The coordinates will appear in the Geolocation field.

-  Libraries information: if you have more than one branch, you can choose 'yes' 
   here to put all your branches on the map

-  See your public page: this is the URL to your information on the Hea website.

Click 'Update your statistics usage' to save the information.

.. _share-with-mana-kb-label:

Share content with Mana KB
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Mana KB is a worldwide knowledge base used to share content specific to libraries.
Koha is currently connected to Mana Kb in order to share serial subscription
models and reports. This section is used to configure your connexion
with Mana KB.

*Get there:* More > Administration > Additional parameters > Share
content with Mana KB

|image1426|

In the form, choose whether you want to use Mana KB to share content or not.
The default is "No, let me think about it". If you do want to use Mana KB,
change the option to "Yes". If you do not want to share with Mana KB, choose
"No", this will remove the blue rectangle from the Administration home
page.

The rest of this section assumes you chose "Yes".

Choose whether you want to share your subscription models automatically.
This means that every time you create a subscription in the serials
module, it will be automatically shared with Mana KB and other libraries
will be able to copy it.

In order to configure Mana KB, you must get a Mana KB token to authenticate
your Koha installation on the Mana KB server.

Enter your name or your organization's name in the "Your name" field.

Enter your email in the "Email" field. Make sure you have access to this
email inbox since you will receive further information by email.

Once you send your information to Mana KB, you will get a Mana KB token.

|image1427|

In the email your receive, click on the confirmation link and confirm you
are not a robot to finish the Mana KB setup.

.. _additional-fields-label:

Additional fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section is used to add custom fields to serial subscriptions or
order baskets.

To add a new field, first choose which table you want to add it to.

- Order baskets (aqbasket): a field added to aqbasket will appear upon
  the :ref:`creation of a new order basket <create-a-basket-label>`
  or the modification of an existing order basket in the 
  :ref:`acquisitions module<acquisitions-label>`.

  |addfieldsorderbasket|

- Subscriptions (subscription): a field added to subscription will appear
  when :ref:`creating a new subscription <add-a-subscription-label>` or
  when :ref:`editing an existing subscription <edit-subscription-label>` in the 
  serials module.

  |addsub2|

Click on "Create field"

Fill out the form

|addfield|

- Name: this is the name of the field as you want it to appear.

- Authorized value category: if you want to add a drop-down menu to the field
  choose an :ref:`authorized value category <existing-values-label>` here (you 
  can also :ref:`create a new authorized value category <add-new-authorized-value-category-label>` 
  if you need to).

- MARC field: for additional subscription fields, it is possible to link
  the field to a MARC field. The additional field will be automatically
  populated with the corresponding record's value for this MARC field.

.. Note::

    You can only choose one of the two options (authorized value OR MARC field)

.. Warning::

    If you choose the MARC field, make sure you enter it in this
    format: field$subfield

    For example: 590$a

- Searchable: check this box if you want to be able to search baskets or
  subscriptions based on this field

  - Order basket searchable additional fields will be available in the
    :ref:`orders advanced search <acquisition-searches-label>` form

  - Subscription searchable additional fields will be available in the
    :ref:`subscription advanced search <searching-serials-label>` form

.. _additional-fields-examples-label:

Examples of additional fields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Example 1:** Additional subscription field using 
:ref:`authorized values <authorized-values-label>`

You might want to track which department you're ordering this serial for

-  In the 'Name' field, enter 'Department'

-  In the 'Authorized value category' field, choose DEPARTMENT

-  Check the 'Searchable' box

|adddept|

When you are :ref:`adding a subscription <add-a-subscription-label>`,
the field will be in the 'Additional fields' section with its
authorized values drop-down menu.

|addsub2|

When you view the subscription, the field will appear under 'Additional
fields'.

|subscriptiondetailsinfo|

Because we made the field searchable, it will also be in the serials
subscription search.

|advancedserialsearch|

**Example 2:** Additional field using MARC field

This is particularly useful if you want to view bibliographic
information in the subscription detail page. In this example, we will
add the 521$a field, which is, in MARC21, the target audience note.

- In the 'Name' field, enter 'Target audience'

- In the 'MARC field' field, enter '521$a'

|addmarcfield|

.. Note::

   You will not be able to edit this field from the subscription
   form. If you need to add or change the value in this field,
   you must go through the :ref:`cataloging module <cataloging-label>`.

When you view the subscription, the field and the information from the
bibliographic record will appear under 'Additional fields'.

|subscriptiondetailsinfo|

.. TO DO: add an example for order basket additional field
