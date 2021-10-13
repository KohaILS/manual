.. include:: images.rst

.. _patrons-label:

Patrons
===============================================================================

Before importing or adding patrons be sure to set up your 
:ref:`patron categories <patron-categories-label>`.

.. _add-a-new-patron-label:

Add a new patron
-------------------------------------------------------------------------------

Patrons are added by going to the 'Patrons' module.

-  *Get there:* Patrons

Once there you can add a new patron.

-  Click 'New patron'

   |image407|

-  The fields that appear on the patron add form can be controlled by
   editing the :ref:`BorrowerUnwantedField` system preference.

-  Required fields are defined in the :ref:`BorrowerMandatoryField` system
   preference

-  First, enter the identifying information regarding your patron

   |image408|

   -  'Salutation' is populated by the :ref:`BorrowersTitles` system preference

   -  **Note**

          If you'd like to prevent full names from printing on
          :ref:`slips <notices-and-slips-label>` and you're not using the Initials or
          Other name fields for anything else, you can use them for
          shortened versions of the name to then be printed on the slip.

          For example:

          ::

              Firstname: Nicole C.
              Surname: Engard
              Initials: NCE

          Then on the slip you can have it print the
          <<borrowers.initials>> instead of the full name (NCE).

          Or you could do something like this:

          ::

              Firstname: Nicole
              Surname: Engard
              Initials: E

          Then on the slip you can have it print the
          <<borrowers.initials>>, <<borrowers.firstname>> instead of the
          full name (E, Nicole).

-  If this patron is a child, you will be asked to attach the child
   patron to an adult patron (guarantor)

   **Note**
   Guarantors can only be attached to patrons whose :ref:`category <patron-categories-label>` 
   is of the 'Child', 'Professional' or 'Organization' type.

   |image410|

   -  If the guarantor is a patron of the library, click 'Search to add' to 
      search your system for an existing patron

      |image1463|

   -  Click 'Select' to choose the patron

      |image1464|

   -  The relationships are set using the :ref:`borrowerRelationship` system 
      preference

      |image1465|

           **Note**

           It is possible to add more than one guarantor to a patron account 
           (both parents for example).

   -  If the guarantor is not a patron, you can still add their information in 
      the 'Non-patron guarantor' section.

-  Next enter the main address and contact information

   |image1466|

       **Note**

       The street type is populated by the ROADTYPE 
       :ref:`authorized values <existing-values-label>`

   |image409|

   -  For contact information, note that the primary phone number and primary 
      email address are the ones that appear on notices and slips printed
      during circulation (receipts, transfer slips and hold slips). The
      primary email is also the one that overdue notices and other
      messages go to.

-  You can also record an alternate address for each patron. This could be used 
   in an academic setting to store the patron's home address for example.

   |image411|

-  Each patron can have an alternate contact. An alternate contact could be a 
   parent or guardian, for example.

   |image412|

-  The library management section includes values that are used within
   the library

   |image413|

   -  The card number field is automatically calculated if you have the
      :ref:`autoMemberNum` system preference set that way

      -  **Note**

             For a newly installed system this preference will start at
             1 and increment by 1 each time after. To have it start with
             the starting number of your barcodes, enter the first
             barcode by hand in the patron record and save the patron.
             After that the field will increment that number by 1.

   -  If you accidentally chose the wrong patron category at the
      beginning you can fix that here

   -  Sort 1 and 2 are used for statistical purposes within your library

      -  You can create drop-down menus for these fields by adding values 
         in the Bsort1 and Bsort2 :ref:`authorized values categories <existing-values-label>`

   -  'Allow auto-renewal of items' is used to control whether this patron 
      wants to automatically renew their checkouts. This requires the 
      :ref:`automatic_renewal cronjob <cron-automatic-renewal-label>` to run 
      daily. 

   -  'Check for previous checkouts' is used to set the patron's personal 
      preference regarding checking their circulation history to see if they 
      have borrowed This item in the past. This overrides the setting of the 
      :ref:`patron category <adding-a-patron-category-label>` and of the 
      :ref:`CheckPrevCheckout` system preference.

-  Next, the library set-up section includes additional library settings

   |image414|

   -  The registration date will automatically be filled in with today's
      date

   -  The expiry date will automatically be calculated based on your 
      :ref:`patron category settings <patron-categories-label>`

   -  The OPAC note is a note for the patron, it will appear in the patron's 
      online account on the OPAC

      |image1504|

      **Note**

      See also :ref:`OPAC messages <opac-messages-label>`

   -  The Circulation note is meant solely for your library staff and
      will appear when the circulation staff goes to check an item out
      to the patron

      |image415|

-  The 'OPAC/Staff interface login' section asks for the username and 
   password to be used by the patron (or staff member) to log into their 
   account in the OPAC and for staff to log in to the staff interface.

   -  Staff will only be able to use this login information to log in to
      the staff interface if they have at least the 
      :ref:`catalogue permission <patron-permissions-label>`.

-  If you have enabled the housebound module (with the :ref:`HouseboundModule` 
   system preference), you will be able to choose a 
   :ref:`housebound role <housebound-patrons-label>` for this patron.

   |image1509|

-  If you have set :ref:`additional patron attributes <patron-attribute-types-label>` 
   in the administration module, these will appear next

   |image416|

-  Finally, if you have the :ref:`EnhancedMessagingPreferences` system 
   preference set to 'allow,' you can choose the messaging preferences for 
   this patron.

   |image417|

   See the definition of each notice in the 
   :ref:`advance notices and hold notices <advance-notices-and-hold-notices-label>`
   section

   -  **Important**

          These preferences will override any you set via the :ref:`patron
          categories <adding-a-patron-category-label>`

   -  **Important**

          These preference can be altered by the patron via the OPAC if the 
          :ref:`EnhancedMessagingPreferencesOPAC` system preference is set to 
          'show'

-  Once finished, click 'Save'

If the system suspects this patron is a duplicate of another it will
warn you.

|image418|

    **Note**

    See the :ref:`PatronDuplicateMatchingAddFIelds` system preference to see 
    or change which fields are used to detect duplicate patrons. The default is 
    the surname, the firstname and the date of birth.

If you have set a minimum or upper age limit on the patron category and
are requiring that the birth date be filled in, Koha will warn you if
the patron you're adding is too old or young for the patron category you
have selected:

|patronagelimit|

If the patron's :ref:`category <patron-categories-label>` has an enrollment 
fee, the fee will be charged to the patron's account when the account is 
created. You can then manage the charge in the patron's :ref:`accounting tab <fines-label>`.

.. _quick-add-patron-label:

Quick add a patron
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If your circulation desk is very busy and you want to register patron quickly,
you can use the 'quick add' feature. It's a shortened version of the add
patron form with only a couple of necessary fields to fill out.

This feature uses two system preferences: :ref:`BorrowerMandatoryField`
and :ref:`PatronQuickAddFields`. These are the two system preferences that
control which fields are in the quick add form.

To quick add a patron, go to the Patrons module

-  *Get there:* Patrons

Click on the 'Quick add new patron' button.

You will be asked to choose a patron category.

Then, you will be presented with a shortened form.

|image1346|

Once the form is filled out, click on 'Save'.

If you need to access the full form, you can click on 'Show full form'
above the 'Save' button.

.. _add-a-staff-patron-label:

Add a staff patron
----------------------------------------

All staff members must be entered into Koha as patrons of the 'Staff'
type. Follow the steps in :ref:`Add a Patron <add-a-new-patron-label>` to add a
staff member. To give the staff member permissions to access the staff
client, follow the steps in :ref:`patron permissions <patron-permissions-label>`

    **Important**

    Remember to assign your staff secure usernames and passwords since
    these will be used to log into the staff client.

.. _add-a-statistical-patron-label:

Add a statistical patron
----------------------------------------------

One way to track use of in house items is to "check out" the materials
to a statistical patron. The "check out" process doesn’t check the book
out, but instead tracks an in house use of the item. To use this method
for tracking in house use you first will need a :ref:`patron
category <patron-categories-label>` set up for your statistical patron.

|image420|

Next, you will need to create a new patron of the statistical type.

|image421|

Next, follow the steps put forth in the ':ref:`Add a new
patron <add-a-new-patron-label>`' section of this manual. Since this patron is
not a real person, simply fill in the required fields, the correct
library and nothing else.

To learn about other methods of tracking in house use visit the
:ref:`tracking inhouse use <tracking-in-house-use-label>` section of this manual.

.. _duplicate-a-patron-label:

Duplicate a patron
-----------------------------------------

Sometimes when you're adding a new family to your system you don't want
to type the contact information over and over. Koha allows for you to
duplicate a patron and change only the parts you want to (or need to)
change.

-  Open the patron you want to use as your base (the patron you want to
   duplicate information from)

-  Click the 'Duplicate' button at the top of their record

   |image422|

-  All of the fields with the exception of first name, card number,
   username and password have been duplicated. Fill in the missing
   pieces and click 'Save'

   |image423|

   -  **Note**

          Clicking in a field that is already populated with data will
          clear that field of all information (making it easier for you
          to type in something different)

-  You will be brought to your new patron

   |image424|

.. _add-patron-images-label:

Add patron images
----------------------------------------

If you would like you can add patron images to help identify patrons. To
enable this feature you must first set the
:ref:`patronimages` preference to 'Allow'.

If the preference is set to 'Allow' you will see a placeholder image
under the patron's name and box to upload a patron image below the basic
contact information.

|image425|

In the 'Upload patron image' box click 'Browse' to find the image on
your computer and 'Upload' to load the image on to the patron record.

|image426|

    **Important**

    There is a limit of 100K on the size of the picture uploaded and it
    is recommended that the image be 200x300 pixels, but smaller images
    will work as well.

.. _editing-patrons-label:

Editing patrons
----------------------------------

Patrons in Koha can be edited using one of many edit buttons.

-  To edit the entire patron record simply click the 'Edit' button at
   the top of the patron record.

   |image427|

-  Patron passwords are not recoverable. The stars show on the patron
   detail next to the password label are always there even if a password
   isn't set. If a patron forgets their password the only option is to
   reset their password. To change the patron's password, click the
   'Change password' button.

   |image428|

   -  Koha cannot display existing passwords as they are encrypted in the
      database. Leave the field blank to leave password unchanged.

   -  This form can automatically generate a random password if you
      click the link labeled "Click to fill with a randomly generated
      suggestion. Passwords will be displayed as text."

-  To edit a specific section of the patron record (for example the
   'Library use' section) click the 'Edit' button beside the section.

   |image429|

-  A patron image can be added by browsing for the image on your machine
   from the 'Manage patron image' section.

   |image430|

   -  This form will not appear if you have the
      :ref:`patronimages` system preference to not allow
      patron images.

   -  To add patron images in bulk, use the :ref:`Upload patron
      images <upload-patron-images-label>` tool.

-  Patrons can also be blocked from checking items out by setting Patron
   flags

   |image431|

   -  If you would like your circulation staff to confirm a patron's
      address before checking items out to the patron, you can see the
      'Gone no address' flag

      |image432|

   -  If the patron reports that they have lost their card you can set
      the 'Lost card' flag to prevent someone else from using that card
      to check items out

      |image433|

   -  If you would like to bar a patron from the library you can add a
      manual restriction

      |image434|

      -  **Note**

             This flag can automatically be set with the :ref:`Overdue/notice
             status triggers <overdue-notice/status-triggers-label>`

   -  If you enter in a date and/or note related to the restriction you
      will see that in the restricted message as well

      |image435|

-  Children patrons do not become adults automatically in Koha unless
   you have the :ref:`Update patron categories <cron-update-patron-categories-label>` cron job running. To
   upgrade a child patron to and adult patron category manually go to
   the 'More' menu and choose 'Update child to adult patron'

   |image436|

   -  You will then be presented with a pop up window asking which one
      of your adult patron categories this Child should be updated to

      |image437|

.. _renew-patron-account-label:

Renew patron account
----------------------------------

When renewing a patron account you can either edit the the expiry date
manually in the patron record or use the 'Renew patron' option from the
More menu in the toolbar at the top.

|image1393|

Using the latter the new expiry date will be calculated using the
enrollment period configured for the patron category of the user.
The system preference :ref:`BorrowerRenewalPeriodBase` determines if
the new expiry date will be calculated from the current date or from the
old expiry date.

One advantage of using the 'Renew patron' option is that it will be logged
as a membership renewal in the action_logs table and be visible as such
when using the :ref:`Log viewer <log-viewer-label>` or the
:ref:`Modificaton log <modification-log-label>` from the patron account.

The renewal date of the patron account will be visible on the details tab.

|image1392|

If the patron is in a :ref:`patron category <patron-categories-label>` with a 
membership fee, the charge will also be added upon renewal. You can then manage 
the charge in the patron's :ref:`accounting tab <fines-label>`.

.. _delete-patron-account-label:

Deleting a patron account
----------------------------------

From the 'More' drop-down, the patron account can be deleted. 

|image1469|

There will be an alert if the patron has checkouts, holds, fines or credits. 

-  If a patron has current checkouts, the deletion will not be possible. 

   |image1470|

-  If a patron has outstanding fines, the deletion will not be possible.

   |image1468|

-  If a patron has unused credits, the option to delete the patron is possible 
   but there will be a warning.

   |image1471|

-  If a patron has existing holds on their account, the option to delete the 
   patron is possible. The hold will be cancelled and moved to the old reserves 
   table. 

   |image1462|

.. _managing-patron-self-edits-label:

Managing patron self edits
--------------------------------------------------

If you are allowing patrons to edit their accounts via the OPAC with the
:ref:`OPACPatronDetails` preference then you will need
to approve all changes via the staff client before they're applied. If
there are patron edits awaiting action they will appear on the staff
client dashboard below the modules list (along with other items awaiting
action).

|image438|

    **Note**

    Superlibrarians will see modifications for any branch, other staff
    will only see modifications for patrons who belong to their logged
    in branch.

When you click the 'Patrons requesting modifications' link you will be
brought to a list of patrons with requested changes.

|image439|

From here you can 'Approve' and apply the changes to the patron record,
'Delete' and remove the changes or 'Ignore' and keep the changes pending
to review later.

If you would like to see the entire patron record you can click the
'Patron details' links to the right of the buttons. This will open in a
new tab.

Merging patron records
-----------------------------------

If you accidentally end up with one patron with two cards it is possible
to merge their records together so that you don't lose their loan history
or holds.

-  In the patron list, check the boxes next to the records you want to
   merge and click on the 'Merge selected patrons' button.

|image1326|

    **Note**

    It is possible to merge more than two records at a time.

-  Select the patron record you want to keep and click on the 'Merge
   patrons' button.

|image1327|

The checkouts and statistics will be transferred to the right record and
the other one will be deleted.

|image1328|

.. _patron-permissions-label:

Patron permissions
-------------------------------------------

Patron permissions are used to allow staff members access to the staff
client.

    **Important**

    In order for a staff member to log into the staff interface they
    must have (at the very least) 'catalogue' permissions which allow
    them to view the staff interface.

.. _setting-patron-permissions-label:

Setting patron permissions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  On the patron record click 'More' and choose 'Set permissions' to alter
   patron permissions

   |image440|

-  You will be presented with a list of preferences, some of which can
   be expanded by clicking the 'Show details' link on the right
   title.

   |image441|

-  In all cases, if the parent permission is checked, the user has all the
   child permissions. If you want to set permissions on a more granular level,
   expand the section and only check the permissions you want that user to
   have.


.. _patron-permissions-defined-label:

Patron permissions defined
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Access to all librarian functions (superlibrarian)

      **Note**

      With this selected there is no need to choose any other
      permissions

-  Check out and check in items (circulate)

   -  Remaining circulation permissions (circulate\_remaining\_permissions)

      -  This permission grants all circulation rights except those covered by
         permissions listed below

   -  Force checkout if a limitation exists (force\_checkout)

      -  With this permission a staff member will be allowed to override a
         check out restriction in the following cases:

         -  age restriction

         -  the item is issued to another patron

         -  the item is not for loan

         -  the patron has overdue items

         -  the item is lost

         -  the item is a high demand item

         -  the item is on hold

   -  Mark checkout notes as seen\/not seen (manage\_checkout\_notes)

      -  The permission to manage the checkout notes written by users
          through the OPAC

   -  Manage restrictions for accounts (manage\_restrictions)

      -  Grants permission to the staff member to lift a restriction that
         might be on the patron's record

   -  Execute overdue items report (overdues\_report)

      -  The permission to run the overdues reports found under Circulation

   -  Override blocked renewals (override\_renewals)

      -  With this permission, a staff member can override renewals if there
         is a restriction

      -  Requires that the staff member also has
         circulate\_remaining\_permissions

-  Staff access, allows viewing the catalogue in staff client (catalogue)
   **Required for staff login.**

      **Important**

      Must be given to all staff members to allow them to login
      to the staff interface

-  Manage Koha system settings (Administration panel) (parameters)

   -  Manage account debit and credit types (manage\_accounts)

      -  This gives access to the :ref:`debit types section <debit-types-label>`

   -  Manage additional fields for baskets or subscriptions (manage\_additional
      \_fields)

      -  This gives access to the 
         :ref:`additional fields section <additional-fields-label>`

      -  **Important**

         This permission requires that the staff member also have the 'Edit
         an existing subscription' permission from the 'Manage serial
         subscriptions' section and the 'Manage basket and order lines'
         permission from the 'Acquisition and\/or suggestion management' section

   -  Manage audio alerts (manage\_audio\_alerts)

      - The ability to access the :ref:`audio alerts <audio-alerts-label>`
        configuration in the administration module.

   -  Manage authorized value categories and authorised values (manage\_auth\_
      values)

      - The ability to access the :ref:`auhorized values <authorized-values-label>`
        configuration in the administration module.

   -  Manage circulation rules (manage\_circ\_rules)

      -  The ability to access the :ref:`circulation and fines rules
         <circulation-and-fines-rules-label>` configuration in the
         administration module.

   -  Manage circulation rules form any library (manage\_circ\_rules\_from\_
      any\_libraries)

      -  If not set the logged in user can only edit circulation rules from
         their own library

      -  The staff member still has to have the 'Manage circulation rules'
         permission above.

   -  Manage cities and towns (manage\_cities)

      -  The ability to access the :ref:`cities and towns <cities-and-towns-label>`
         configuration in the administration module.

   -  Manage classification sources and filing rules (manage\_classifications)

      -  The ability to access the :ref:`classification sources
         <classification-sources-label>` configuration in the administration
         module.

   -  Manage column configuration (manage\_column\_config)

      -  The ability the access the :ref:`configure columns <column-settings-label>`
         page in the administration module.

   -  Manage Did you mean? configuration (manage\_didyoumean)

      -  The ability to access the :ref:`Did you mean? <did-you-mean?-label>`
         configuration in the administration module.

   -  Manage item circulation alerts (manage\_item\_circ\_alerts)

      -  The ability to access the :ref:`item circulation alerts <item-circulation-alerts-label>`
         configuration in the administration module.

   -  Manage item search fields (manage\_item\_search\_fields)

      -  The ability to access the :ref:`item search fields <item-search-fields-label>`
         configuration in the administration module.

   -  Manage item types (manage\_itemtypes)

      -  The ability to access the :ref:`item types <item-types-label>`
         configuration in the administration module.

   -  Manage keyboard shortcuts for the advanced cataloging editor (manage\_
      keyboard\_shortcuts)

      -  The ability to access the keyboard shortcuts configuration in the
         administration module

   -  Manage libraries and library groups (manage\_libraries)

      -  The ability to access the :ref:`libraries <libraries-label>` and
         :ref:`library groups <library-groups-label>` configuration pages
         in the administration module.

   -  Manage Mana KB content sharing (manage\_mana)

      -  The ability to access the :ref:`share content with Mana KB
         <share-with-mana-kb-label>` in the administration module

   -  Manage MARC bibliographic and authority frameworks and test them
      (manage\_marc\_frameworks)

   -  The ability to access the
      :ref:`MARC bibliographic framework <marc-bibliographic-frameworks-label>`,
      :ref:`authority types <authority-types-label>`,
      :ref:`Koha to MARC mapping <koha-to-marc-mapping-label>`, and
      :ref:`MARC Bibliographic framework test <marc-bibliographic-framework-test-label>`
      configuration areas in the administration module.

   -  Manage record matching rules (manage\_matching\_rules)

      -  The ability to access the :ref:`record matching rules <record-matching-rules-label>`
         configuration in the administration module.

   -  Manage OAI sets (manage\_oai\_sets)

      -  The ability to access the :ref:`OAI sets <oai-sets-configuration-label>`
         configuration in the administration module.

   -  Manage extened patron attributes (manage\_patron\_attributes)

      -  The ability to access the :ref:`patron attribute types <patron-attribute-types-label>`
         configuration in the administration module.

   -  Manage patron categories (manage\_patron\_categories)

      -  The ability to access the :ref:`Patron categories <patron-categories-label>`
         configuration in the administration module.

   -  Manage search engine configuration (manage\_search\_engine\_config)

      -  The ability to access the Search engine configuraton in the
         administration module. Note: This area will only be visible when
         the :ref:`SearchEngine` system preference is set to 'Elasticsearch'.

   -  Manage Z39.50 and SRU server configuration (manage\_search\_targets)

      -  The ability to access the :ref:`Z39.50/SRU servers <z39.50/sru-servers-label>`
         configuration in the administration module.

   -  Manage SMS cellular providers (manage\_sms_providers)

      -  The ability to access the :ref:`SMS cellular providers
         <sms-cellular-providers-label>` configuration in the administration
         module. Note: This area will only be visible when the
         :ref:`SMSSendDriver` system preference is set to 'Email'.

   -  Manage global system preferences (manage\_sysprefs)

      -  The ability to access the :ref:`global system preferences
         <administration-system-preferences-label>` in the administration module.

   -  Manage library transfer limits and transport cost matrix (manage\_transfers)

      -  The ability to access the :ref:`library transfer limits <library-transfer-limits-label>`
         and :ref:`transport cost matrix <transport-cost-matrix-label>`
         configuration pages in the administration module.

   -  Manage usage statistics settings (manage\_usage\_stats)

      -  The ability to access the :ref:`share your usage statistics <share-anonymous-usage-statistics-label>`
         configuration in the administration module.

   -  Remaining system parameters permissions (parameters\_remaining\_permissions)

      -  The ability to access all remaining areas in the administration module.

-  Add, modify and view patron information (borrowers)

   -  Add, modify and view patron information (edit\_borrowers)

      -  The ability to access the Patrons module to view patron files,
         as well as adding new patrons and editing patron files

   -  View patron infos from any libraries (view\_borrower\_infos\_from\_any\_libraries)

   -  If not set the logged in user will only be able to access patron
      information from their own library or group of libraries.

-  Set user permissions (permissions)

   -  The ability to set permissions for other staff members

-  Place and modify holds for patrons (reserveforothers)

   -  Modify holds priority (modify\_holds\_priority)

      -  Allows staff members to alter the holds priority (moving patrons up
         and down the queue)

   -  Place holds for patrons (place\_holds)

      -  Allows staff members to place holds in the staff interface

-  Edit catalog (Modify bibliographic/holdings data) (editcatalogue)

   -  Use the advanced cataloging editor (advanced\_editor)

      -  Grants the ability to use the advanced cataloging editor in the
         cataloging module

      -  **Note**

         Staff members with this permission need to also have the 'Edit catalog
         (Modify bibliographic/holdings data)' permission

   -  Delete all items at once (delete\_all\_items)

      -  Ability to use the 'Delete all items' option found under the
         'Edit' menu in cataloging

   -  Edit catalog (Modify bibliographic/holdings data) (edit\_catalogue)

      -  Ability to access all cataloging functions via the
         `Cataloging <#cataloging>`__ page

   -  Edit items (edit\_items)

      -  Ability to make :ref:`edits to item/holdings
         records <editing-items-label>`, but not bibliographic records

   -  Limit item modification to subfields defined in the
      :ref:`SubfieldsToAllowForRestrictedEditing` system preference
      (edit\_items\_restricted)

      -  If checked, the staff member will only be able to modify some
         item subfields

      -  **Note**

         Please note that the 'Edit items' permission is still required

   -  Fast cataloging (fast\_cataloging)

      -  The ability to catalog using only the :ref:`Fast add
         framework <fast-add-cataloging-label>` found on the
         `Circulation <#circulation>`__ page

-  Manage patrons fines and fees (updatecharges)

   -  Discount debits for patrons (discount)

      -  Grant the ability to apply discounts to charges

   -  Payout credits to patrons (payout)

      -  Grant the ability to reimburse credits to patrons

   -  Refund payments to patrons (refund)

      -  Grant the ability to refund payments that patrons have already made to 
         the library

   -  Remaining permissions for managing fines and fees (remaining\_permissions)

      -  Grant the ability to manage fines and fees other than the actions
         described in the other subpermissions (dicounts, payouts, refunds and 
         writeoffs)

   -  Write off fines and fees (writeoff)

      -  Grants the ability to write off patron fees


-  Acquisition and/or suggestion management (acquisition)

   **Note**

   All the acquisitions sub-permissions give access to the acquisitions home
   page. That means that staff who have one or more of the following permissions
   will be able to view the budgets, search and view vendor information, and
   view invoices.

   -  Add and delete funds (but can't modify funds) (budget\_add\_del)

      -  Grants the ability to add and delete funds within a budget

      -  Note that the budget\_manage and budget\_modify permissions are
         required for this one to work correctly

   -  Manage funds (budget\_manage)

      -  Grants the ability to acces the :ref:`fund administration page <funds-label>`

      -  Note that this only gives viewing access to the page, you will need
         to give your staff budget\_add\_del and budget\_modify if you want
         them to be able to make changes to the funds

   -  Manage all funds (budget\_manage\_all)

      -  Grants viewing access to all funds regardless of restrictions on
         them (owner, user or library restrictions)

      -  Note that the budget\_manage permission is required

   -  Modify funds (can't create lines, but can modify existing ones) (budget\_modify)

      -  Grants the ability to edit fund information and amounts

      -  Note that the budget\_add\_del and budget\_manage permissions are
         required for this one to work correctly

   -  Manage contracts (contracts\_manage)

      -  Grants the ability to add, edit and delete contracts with vendors

   -  Manage currencies and exchange rates (currencies\_manage)

      -  The ability to access the :ref:`Currencies and exchange rates
         <currencies-and-exchange-rates-label>` configuration page.

   -  Manage EDIFACT transmissions (edi\_manage)

      -  Grants the ability to access the :ref:`EDI account <edi-accounts-label>`
         administration page, the :ref:`library EANs <library-eans-label>`
         administration page and access sent :ref:`EDI messages <edifact-messages-label>`

      -  In order to be able to send orders via EDI, your staff member also
         needs the

   -  Manage basket groups (group\_manage)

      -  Grants the ability to :ref:`create, edit, close and delete basket
         groups <create-a-basket-group-label>`

   -  Manage baskets and order lines (order\_manage)

      -  Grants the ability to :ref:`place orders <placing-orders-label>`,
         including creating baskets, adding order lines, closing baskets, etc.

   -  Manage all baskets and order lines, regardless of restrictions on them
      (order\_manage\_all)

      -  Grants the ability to manage all baskets and orders even if they are
         restricted to the owner, users or library

      -  Note that the order\_manage permission is required

   -  Receive orders and manage shipments (order\_receive)

      -  Grants the ability to create invoices, receive items and claim late
         orders

   -  Manage budgets (period\_manage)

      -  Grants access to the :ref:`budget administration page <budgets-label>`
         and the ability to create, edit and delete budgets

      -  This permission does not give the ability to edit budget funds.

   -  Manage budget plannings (planning\_manage)

      -  Grants the ability to view :ref:`budget planning <budget-planning-label>`

      -  Note that the budget\_manage and the period\_manage permissions are
         required for this one to work

   -  Manage purchase suggestions (suggestions\_manage)

      -  Grants the ability to :ref:`create and manage purchase suggestions
         <managing-purchase-suggestions-label>`, including creating new
         suggestions and changing the suggestions' statuses

   -  Manage vendors (vendors\_manage)

      -  Grants the ability to :ref:`add, edit and delete vendors <vendors-label>`

      -  Note that vendors are used in the acquisition and the serials module.

-  Use all tools (tools)

   -  Access to the files stored on the server (access\_files)

      -  Access to the :ref:`Upload tool <upload-label>`

   -  Upload patron images in batch or one at a time (batch\_upload\_patron\_images)

      -  Access to the :ref:`Image upload tool <upload-patron-images-label>`

   -  Delete old borrowers and anonymize circulation/reading history
      (deletes borrower reading history) (delete\_anonymize\_patrons)

      -  Access to the :ref:`Anonymize patron tool <patrons-anonymize-bulk-delete-label>`

   -  Define days when the library is closed (edit\_calendar)

      -  Access to the :ref:`Calendar/holidays tool <calendar-label>`

   -  Write news for the OPAC and staff interfaces (edit\_news)

      -  Access to the :ref:`News tool <news-label>`

   -  Set notice/status triggers for overdue items (edit\_notice\_status\_triggers)

      -  Access to the :ref:`Overdue notice status/triggers
         tool <overdue-notice/status-triggers-label>`

   -  Define notices (edit\_notices)

      -  Access to the :ref:`Notices and slips tool <notices-and-slips-label>`

   -  Perform batch modification of patrons (edit\_patrons)

      -  Access to the :ref:`Batch patron modification tool <batch-patron-modification-label>`

   -  Edit quotes for the quote-of-the-day feature (edit\_quotes)

      -  Access to the :ref:`Quote of the Day (QOTD) Editor <quote-of-the-day-(qotd)-editor-label>`

   -  Export bibliographic and holdings data (export\_catalog)

      -  Access to the :ref:`Export data tool <export-data-(marc-and-authorities)-label>`

   -  Import patron data (import\_patrons)

      -  Access to the :ref:`Import patrons tool <patron-import-label>`

   -  Perform inventory of your catalog (inventory)

      -  Access to the :ref:`Inventory tool <inventory-tool-label>`

   -  Perform batch deletion of items (items\_batchdel)

      -  Access to the :ref:`Batch item deletion tool <batch-item-deletion-label>`

   -  Perform batch modification of items (items\_batchmod)

      -  Access to the :ref:`Batch item modification tool <batch-item-modification-label>`

   -  Limit batch item modification to subfields defined in the
      SubfieldsToAllowForRestrictedBatchmod preference (items\_batchmod\_restricted)

      -  Restricts the :ref:`batch item modification <batch-item-modification-label>` tool
         to modify only the subfields defined in the
         :ref:`SubfieldsToAllowForRestrictedBatchmod` preference

      -  Please note that items\_batchmod permission is still required

   -  Create printable labels and barcodes from catalog and patron data
      (label\_creator)

      -  Access to the :ref:`Patron card creator <patron-card-creator-label>`,
         the :ref:`Label creator <label-creator-label>` and the
         :ref:`Quick label creator <quick-spine-label-creator-label>` tools

   -  Manage CSV export profiles (manage\_csv\_profiles)

      -  Access to the :ref:`CSV profiles tool <csv-profiles-label>`

   -  Add, edit and delete patron lists and their contents (manage\_patron\_lists)

      -  Access to the :ref:`Patron lists tool <patron-lists-label>`

   -  Manage staged MARC records, including completing and reversing imports
      (manage\_staged\_marc)

      -  Access to the :ref:`Manage staged MARC records tool <staged-marc-record-management-label>`

   -  Manage MARC modification templates (marc\_modification\_templates)

      -  Access to the :ref:`MARC modification templates tool <marc-modification-templates-label>`

   -  Moderate patron comments (moderate\_comments)

      -  Access to the :ref:`Comments tool <comments-label>`

   -  Moderate patron tags (moderate\_tags)

      -  Access to the :ref:`Tags tool <tag-moderation-label>`

   -  Perform batch deletion of records (bibliographic or authority)
      (records\_batchdel)

      -  Access to the :ref:`Batch record deletion tool <batch-record-deletion-label>`

   -  Perform batch modification of records (bibliographic or authorities)
      (records\_batchmod)

      -  Access to the :ref:`Batch record modification tool <batch-record-modification-label>`

   -  Manage rotating collections (rotating\_collections)

      -  Access to the :ref:`Rotating collections tool <rotating-collections-label>`

   -  Schedule tasks to run (schedule\_tasks)

      -  Access to the :ref:`Task scheduler tool <task-scheduler-label>`

   -  Stage MARC records into the reservoir (stage\_marc\_import)

      -  Access to the :ref:`Stage MARC records tool <stage-marc-records-for-import-label>`

   -  Upload any file (upload\_general\_files)

      -  Access to upload files via the :ref:`Upload tool <upload-label>`

   -  Upload local cover images (upload\_local\_cover\_images)

      -  Access to the :ref:`Upload local cover image
         tool <upload-local-cover-image-label>` as well as permission to add and
         delete local cover images from the record detail page

   -  Manage uploaded files (upload\_manage)

      -  Access to uploaded files via the :ref:`Upload tool <upload-label>`

      -  Note that the upload\_general\_files permission is required for this
         permission to work

   -  Browse the system logs (view\_system\_logs)

      -  Access to the :ref:`Log viewer tool <log-viewer-label>`

-  Edit authorities (editauthorities)

   -  Grants the ability to create, edit and delete authority records

   -  Note that it is possible to search authority records with only the
      catalogue permission

-  Manage serial subscriptions (serials)

   -  Check the expiration of a serial (check\_expiration)

   -  Gives ability to check the :ref:`expiration date of serials
      <check-serial-expiration-label>`

   -  Claim missing serials (claim\_serials)

      -  Gives the ability to :ref:`claim missing issues <claim-late-serials-label>`

   -  Create a new subscription (create\_subscription)

      -  Gives the ability to :ref:`add new subscriptions <add-a-subscription-label>`

   -  Delete an existing subscription (delete\_subscription)

      -  Gives the ability to delete serial subscriptions

   -  Edit an existing subscription (edit\_subscription)

      -  Gives the ability to :ref:`edit existing serial subscriptions
         <edit-subscription-label>`

      -  This permission does not include the ability to delete or create a
         subscription

   -  Serials receiving (receive\_serials)

      -  Gives the ability to :ref:`receive issues <receive-issues-label>` of
         existing subscriptions

   -  Renew a subscription (renew\_subscription)

      -  Gives the ability to :ref:`renew serial subscriptions <renewing-serials-label>`

   -  Routing (routing)

      -  Gives the ability to manage :ref:`routing lists <create-a-routing-list-label>`

   -  Manage subscriptions from any branch (superserials)

      -  This permission is only useful if the :ref:`IndependentBranches`
         system preference is used

-  Allow access to the reports module (reports)

   -  Reports found on the :ref:`Circulation page <circulation-reports-label>`
      are not controlled by this permission; this only controls access to the
      :ref:Reports module <reports-label>`

   -  Reports in the :ref:`Statistics wizard <statistics-reports-label>` section
      and the other reports on the main reports page can be run with any one
      of the following permissions. They only affect the SQL reports.

   -  Create SQL reports (create\_reports)

      -  The ability to create :ref:`guided reports <guided-report-wizard-label>`
         or :ref:`SQL reports <report-from-sql-label>`, but not run saved ones

   -  Delete SQL reports (delete\_reports)

      -  The ability to delete saved :ref:`SQL reports <report-from-sql-label>`

      -  Note that you need execute\_reports in order to be able to delete them

   -  Execute SQL reports (execute\_reports)

      -  The ability to :ref:`run custom SQL reports <running-custom-reports-label>`,
         but not create or edit them

-  Allow staff members to modify permissions for other staff members (staffaccess)

   -  This permission requires the borrowers permission above

-  Course reserves (coursereserves)

   -  Allow access to the :ref:`course reserves module <course-reserves-label>`

   -  Note that if the :ref:`UseCourseReserves` system preference is not enabled,
      these permissions will not have any effect

   -  Add course reserves (add\_reserves)

      -  Grants the ability to :ref:`add items to existing courses
         <adding-reserve-materials-label>`

   -  Remove course reserves (delete\_reserves)

      -  Grant the ability to remove items from existing courses

   -  Add, edit and delete courses (manage\_courses)

      -  Grants the ability to :ref:`create, edit and delete courses
         <adding-courses-label>`, but not manage the items

-  Koha plugins (plugins)

   -  Configure plugins (configure)

      -  Gives the ability to run the 'configure' section of a plugin if it has
         one

      -  Note that the staff member needs either the report permission or the
         tool permission (below) in order to be able to access the plugins

   -  Manage plugins (manage)

      -  The ability to install or uninstall plugins

      -  Note that the staff member needs either the report permission or the
         tool permission (below) in order to be able to access the plugins

   -  Use report plugins (report)

      -  The ability to use report plugins

   -  Use tool plugins (tool)

      -  The ability to use tool plugins

-  Lists (lists)

      **Important**

      All staff have permission to create and modify their own
      lists, this permission is only necessary if you'd like to give
      a staff member permission to delete public lists that they
      have not created.

   -  Delete public lists (delete\_public\_lists)

      -  The ability to delete public lists created by someone else

-  Patron clubs (clubs)

   -  Create and edit clubs (edit\_clubs)

      -  Create and edit patron clubs using the :ref:`Patron clubs tool <patron-clubs-label>`

   -  Create and edit club templates (edit\_templates)

      -  Create and edit club templates using the :ref:`Patron clubs tool <patron-clubs-label>`

   -  Enroll patrons in clubs (enroll)

      -  Enroll patrons from the patron file

      -  The borrowers permissions is required in order to enroll patrons in
         clubs

-  Create and modify interlibrary loan requests (ill)

   -  Gives access to the :ref:`Interlibrary loan (ILL) module <ill-requests-label>`

-  Self check modules (self\_check)

   -  Log into the self check-in module (self\_checkin\_module)

      **Note**

      This permission prevents the patron from using any other OPAC
      functionality

-  Perform self checkout at the OPAC (self\_checkout\_module)

      **Note**

      This permission should be used for the patron matching the
      :ref:`AutoSelfCheckID <autoselfcheck-preferences-label>`
      system preference

-  Manage :ref:`stockrotation <stock-rotation-label>` operations (stockrotation)

   -  Add and remove items from rotas (manage_rota_items)

      -  Staff with only this permission will be able to manage the items in the
         rotas, but not the rotas themselves

   -  Create, edit and delete rotas (manage_rotas)

      -  Staff with only this permission will be able to manage the rotas, but not
         the actual items

-  Cash management (cash_management)

   -  Add, edit and archive cash registers (manage_cash_registers)

      -  Staff with this permissions will be able to manage the :ref:`cash
         registers in the administration module <cashregisters-label>`

   -  Access the point of sale page and take payments (takepayment)

      -  Grants access to the point of sale module

.. _patron-information-label:

Patron information
-------------------------------------------

When viewing a patron record you have the option to view information
from one of many tabs found on the left hand side of the record.

-  *Get there:* Patrons > Browse or search for patron > Click patron
   name

.. _check-out-label:

Check out
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For instruction on checking items out, view the :ref:`Checking
out <check-out-(issuing)-label>` section of this manual.

Staff members can access their own check out screen by clicking their
username in the top right of the staff client and choosing 'My
checkouts'

|image1178|

.. _details-label:

Details
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

     **Note**

     Staff members can access their own account details by clicking their
     username in the top right of the staff client and choosing 'My account'

     |image442|

All patron information will appear in the Details tab. This includes all
the contact information, notes, custom patron attributes, messaging
preferences, etc. entered when adding the patron.

|image1359|

In the case of patrons who are marked as 'Child' or 'Professional' and
their guarantors additional information will appear on their record.

-  A child patron will list their guarantor

   |image443|

-  On the guarantor's record, all children and/or professionals will be
   listed

   |image444|

.. _circulation-summary-label:

If the age of the patron is outside the age range defined in their patron
category a warning will appear on their record.

   |image1461|

Circulation summary
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Below the patron's information on the details screen is a tabbed display
of the items they have checked out, overdue, and on hold.

Checkouts
''''''''''''''''''''''''''''''''''''''''''

The first tab shows the items the patron currently has checked out.

|image445|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: issues-table).

Relatives' checkouts
''''''''''''''''''''''''''''''''''''''''''

If they have family at the library, staff can see what the other family
members have checked out.

|image446|

Charges
'''''''''''''''''''''''''''''''''''''''''

The Charges tab will only show in the patron accounts that have unpaid amounts 
or unused credits.

The tab will show the total amount, without any details. To see the details, 
go to the :ref:`accounting tab <fines-label>`.

|image1360|

Holds
'''''''''''''''''''''''''''''''''''''''''

If the patron has holds, the number of holds will appear on this tab's
title and the details will appear in the tab.

|image490|

     **Note**

     The barcode and call number will only appear on item-level holds or
     holds that have been confirmed. Record-level holds that are not
     waiting to be picked up will not have barocdes or call numbers.

From here you can manage the patron's holds: change the pickup library,
cancel or suspend holds.

     **Note**

     You will only be able to suspend holds if the :ref:`SuspendHoldsIntranet`
     system preference is set to "Allow".

     **Note**

     If, when suspending a hold, you want to be able to set a date at which to
     automatically resume the hold, set the :ref:`AutoResumeSuspendedHolds`
     system preference to "Allow" and make sure the :ref:`unsuspend_holds cron
     job <cron-unsuspend-holds-label>` is activated.

.. _article-requests-label:

Article requests
'''''''''''''''''''''''''''''''''''''''''''''

If the :ref:`ArticleRequests` system preference is enabled, and the circulation
rules allow it, the patrons will be able to request articles, either through the
OPAC or in the staff interface.

The details of the patron's request, and its status, are visible in this
tab.

|image1361|

Restrictions
''''''''''''''''''''''''''''''''''''''''''''

The Restrictions tab will show for all patrons. If the patron has no
restrictions you will see that on the tab.

|image447|

If the patron has restrictions on their account the tab will show the
number and the description.

There are four kinds of restrictions:
  - Manual
  - Overdues
  - Suspension
  - Discharge

Using the 'Add manual restriction' button you can add a restriction to
the patron record from here. This can be used for any type of restriction
you need to put manually on a patron record.

|image449|

|image448|

The overdues restrictions are automatically set when overdue notices are sent
if you specified you wanted the patron restricted in the
:ref:`Overdue notice/status triggers tool <overdue-notice/status-triggers-label>`.

This restriction will not be removed automatically when the overdue items are
returned unless the :ref:`AutoRemoveOverduesRestrictions` system preference
is set to 'Do'.

In the :ref:`circulation rules <circulation-and-fines-rules-label>`, you can choose
to fine users by suspending them instead of (or in addition to) fining them money.
In that case, returning an overdue document will trigger a suspension restriction.

Patrons may also be restricted if you have issued a :ref:`discharge <patron-discharges-label>` for them. Once the discharge is validated, the patron is automatically restricted.

Restrictions on a patron record will block checkouts. In fact,
a message will appear in red when going to the checkout page.

|image1363|

Restrictions may also prevent renewing items if the :ref:`RestrictionBlockRenewing`
system preference is set to 'block'.

On the OPAC, patrons will get a message saying their account is frozen. They will
not be able to place holds from the OPAC.

If you have patrons that have more than one restriction, you can choose to
cumulate their restriction periods or not through the :ref:`CumulativeRestrictionPeriods`
system preference.

     **Note**

     If you want to restrict patrons from doing various actions if their record
     is not pristine, check the following system preferences:

     - Set the :ref:`OverduesBlockCirc` system preference to 'Block' to prevent
       patrons who have overdue materials from checking out other materials.
     - Set the :ref:`OverduesBlockRenewing` system preference to 'block renewing
       for all the patron's items' or 'block renewing only for this item' to prevent
       patrons who have overdue materials from renewing their loans.
     - Enter values in the :ref:`noissuescharge` and :ref:`NoIssuesChargeGuarantees`
       system preferences in order to block checking out to patrons who have more
       than a certain amount in fines or to patrons whose guarantees owe more than
       a certain amount.
     - Enter a value in the :ref:`maxoutstanding` system preference to prevent
       patron from placing holds on the OPAC if they owe more than a certain amount.
     - Enter a value in the :ref:`OPACFineNoRenewals` system preference to prevent
       patron who owe more than a certain amount to renew their loans from the OPAC.
     - Set the :ref:`BlockExpiredPatronOpacActions` system preference to 'Block' if
       you want to prevent patron whose membership has expired to place hold or
       renew their loans from the OPAC.

Clubs
'''''''''''''''''''''''''''''''''''''''''''

If you use :ref:`patron clubs <patron-clubs-label>`, patrons will have a tab
in their record indicating which club they are enrolled in, if any.

|image1362|

.. _fines-label:

Accounting
~~~~~~~~~~~~~~~~~~~~~~~~

The patron's complete accounting history will appear on the Accounting tab.
The Accounting tab will show all types of charges and credits: overdue fines, 
membership fees, rental fees, reserve fees and any other charge you may have 
for patrons.

|image450|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: account-fines).

The Transactions tab will show you the following columns:

-  Date: the date the charge, payment or credit was posted

   -  In the case of fines this will be the last day that the fine was
      accrued

-  Account type: what type of charge, payment or credit it is

   -  In cases where an account type may have an accompanying `status` it will be
      displayed alongside the accounttype in brackets.

-  Description of charges: a description of the charges including the due date for
   overdue items and a link to the item record where one is available

-  Barcode: if the charge is linked to a particular item, the barcode is 
   displayed

-  Due date: if the charge is an overdue fine, the due date is displayed

-  Checkin date: if the charge is an overdue fine, the checkin date is displayed

-  Checkout date: if the charge is an overdue fine, the check out date is displayed

-  Home library: if the charge is linked to a particular item the home library
   is displayed

-  Note: any notes about this charge/payment

   -  If you're allowing patrons to pay fines via the OPAC with PayPal
      (:ref:`EnablePayPalOpacPayments <enablepaypalopacpayments-and-paypalsandboxmode-label>`) you
      will see a Note that says 'PayPal' for items paid this way

-  Amount: the total amount of the payment or charge

-  Outstanding: the amount still due on charge

-  Actions:

   - A selection of actions available to take upon the account line as detailed below

At the top of the table you can click the 'Filter paid transaction' to
hide all completed transaction and above that you can use the search box
to find a specific charge or payment.

.. _charging-fines/actions-label:

Actions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Action buttons will be available for the different account lines depending on 
the users available permissions and the account type and status.

- A button to print a receipt for that line item

- A button to show further details about the charge and any payments that have been made

- A button to void (reverse) a payment/credit

  - This button will only appear on a payment/credit line. Upon voiding the
    line it will reverse the payment process restoring the amountoutstanding
    for any debts/debits which the payment/credit may have previously been 
    used to offset. This action is most commonly used to correct cases where
    a payment was recorded but never actually recieved. The credit line will be
    set to a zero amount and updated to `VOID`.

- A button to cancel (remove) a charge/debit

  - This button will only appear on a charge/debit line that has not already
    had any payment/credits applied to it. Upon cancelling the line it will
    be marked as 'Cancelled' and a `CANCELLATION` line will be added and offset 
    against it. This action is most commonly used to correct cases where a 
    charge was made mistakenly.

- A button to pay against charges/debits with outstanding amounts

  - This button will appear against any charge/debit with an outstanding 
    amount.  The subsequent page can be used to pay or writeoff the line 
    partially or in full with a `PAYMENT` or `WRITEOFF` line will being added.

- A button to issue a payout of credit

  - This button will appear against any credit line that has an amount 
    outstanding and you have the :ref:`payout permission <patron-permissions-defined-label>`.
    It allows the librarian to return outstanding credit to the patron and 
    record the action with a `PAYOUT` line.

- A button to issue a refund against a charge/debit

  - This button will appear against any charge/debit line that has been paid or
    partially paid and you have the :ref:`refund permission <patron-permissions-defined-label>`.
    The subsequent modal dialogue will allow you to partially or fully refund 
    the offset debt, either in `CASH` or by means of a credit added to the 
    account.

- A button to apply a discount to a charge/debit

  - This button will appear against any charge/debit which has not already been
    offset by a credit/payment and you have the 
    :ref:`discount permission <patron-permissions-defined-label>`.
    The subsequent modal dialogue will allow you to add a discount upon the 
    charge.

.. _charging-fines/fees-label:

Charging fines/fees
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Most fees and fines will be charged automatically if the :ref:`fines cron
job <cron-fines-label>` is running.  Fines will also be charged when an overdue item is checked
in if the :ref:`CalculateFinesOnReturn` system preference is enabled. 

-  Fines will be charged based on your :ref:`circulation and fines
   rules <circulation-and-fines-rules-label>`

-  Hold fees will be charged based on the rules you set in the :ref:`Patron
   types and categories <patron-categories-label>` administration area

-  Rental fees will be charged based on the settings in your :ref:`Item
   iypes <item-types-label>` administration area

-  Marking an item 'Lost' via the cataloging module will automatically
   charge the patron the replacement cost for that item

-  Creating a patron in a :ref:`category <patron-categories-label>` 
   with an enrollment fee.

-  Renewing a patron account in a :ref:`category <patron-categories-label>` 
   with an enrollment fee.

.. _pay-and-writeoff-fines-label:

Pay and Writeoff fines
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Each line item can be paid in full (or written off) using the 'Pay charges' 
tab.  You can switch between 'Pay' and 'Write off' mode using the buttons located at  
the top of this tab if you are part way through a transaction.   

|image451|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: pay-fines-table).

-  Each line item can be paid in full, partially paid, or written off.

-  Pay a fine in full

   -  If you have a note about the payment please type that first then
      move on

   -  Click "Pay" next to the fine you want to pay in full

   -  The full amount of the fine will be populated for you in the
      "Collect from patron" box

   -  There is a change feature included in this payment process. An option to   
      specify how much money was collected when paying a fine, as well as defining how 
      much was paid on the fine. If these numbers are different (i.e. more money was 
      collected) a popup displaying the amount of change to be given will be displayed and  
      require confirmation before proceeding

   -  If one or more values are defined under the PAYMENT\_TYPE authorized value
      category a dropdown selection box will be displayed to specify a custom
      payment type.

   -  If the :ref:`UseCashRegisters` system preference is enabled, you will
      have a choice of cash register in which to enter the transaction

   -  Click "Confirm"

   -  The fine will be removed from outstanding fines, and displayed as
      fully paid.
 
   **Note**

   - If the :ref:`FinePaymentAutoPopup` system preference is enabled a print dialogue window
     will display.  If change was given for this trancaction the details will be included when 
     using this system preference. 

   - In addition to printing receipts you can enable email receipts for payment and writeoff transactions
     with the :ref:`UseEmailReceipts` system preference.


-  Pay a partial fine

   -  Click "Pay" next to the fine you want to partially pay

   -  Enter the amount you are collecting from the patron in the
      "Collect from patron" box

      |image453|

   -  Click "Confirm"

   -  The fine will be updated to show the original amount, and the
      current amount outstanding

-  Pay an amount towards all fines

   -  Click the "Pay amount" button

   -  Enter the amount you are collecting from the patron in "Collect
      from patron." The sum of all fines is shown in "Total amount
      outstanding"

      |image454|

   -  Click "Confirm"

   -  The fine totals will be updated with the payment applied to oldest
      fines first.

-  Pay selected fines

   -  Check the selection boxes next to the fines you wish to pay, click
      "Pay selected"

      |image455|

   -  Enter an amount to pay towards the fines.

      |image456|

   -  Click "Confirm"

   -  The fine totals will be updated with the payment applied to the
      oldest selected fines first.

-  Writeoff a single fine

   -  Click "Writeoff" next to the fine you wish to writeoff.

   -  A confirmation box will appear to specify a total amount to writeoff.
      This box allows a partial writeoff of fines.

   -  The fine will be removed from outstanding fines, and displayed as
      written off.

-  Writeoff selected fines

   -  Check the selection boxes next to the fines you wish to pay, click "Writeoff selected".

   -  Click "Confirm".

   -  The fine will be removed from outstanding fines, and displayed as written off.

-  Writeoff all fines

   -  Click the "Writeoff all" button

   -  All fines will be removed from outstanding fines, and displayed as written off.

.. _void-payments-label:

Void payments
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you accidentally mark and item as paid, you can reverse that line item 
by clicking 'Void' to the right of the line

   |image457|

-  Once clicked a new line item will be added to the account showing
   the payment as ‘Voided’.  The payment line is added back to
   the Pay fines tab as an outstanding charge.

   |image458|

.. _creating-manual-invoices-label:

Creating manual invoices
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For fees that are not automatically charged, librarians can create a
manual invoice

|image459|

-  First choose the type of invoice you would like to create

   -  To add additional values to the manual invoice type pull down
      menu, add them to the :ref:`debit types <add-debit-type-label>`
      in the Administration module.

-  If the fee is associated with an item you can enter its barcode so
   that the line item shows a link to that item

-  The description field is where you will enter the description of the
   charge

-  In the amount field, do not enter currency symbols, only numbers and
   decimals

.. _creating-manual-credits-label:

Creating manual credits
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Manual credits can be used to pay off parts of fines, or to forgive a
fine amount.

|image460|

-  First choose the type of credit you'd like to apply

-  If this credit is associated with an item you can enter that item's
   barcode so that the line item links to the right item

-  The description field is where you will enter the description of the
   credit

-  In the amount field, do not enter currency symbols, only numbers and
   decimals

.. _printing-invoices-label:

Printing invoices
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To the right of each account line there is a print link. Clicking that
link will print an invoice for the line item that includes the date and
description of the line item along with the total outstanding on the
account.

|image461|

.. _routing-lists-label:

Routing lists
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A list of all of the serial routing lists the patron belongs to will be
accessible via the 'Routing lists' tab on the patron record.

|image462|

On this tab you will be able to see and edit all of the routing lists
that this patron is on.

|image463|

.. _circulation-history-label:

Circulation history
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The circulation history tab will appear if you have set the
:ref:`intranetreadinghistory` preference to allow
it to appear. If you have the :ref:`OPACPrivacy` system
preference set to 'Allow' and the patron has decided that the library
cannot keep this information this tab will only show currently checked
out items.

|image464|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: checkouthistory-table).

If you would like to export a list of barcodes for the items checked in
today you can find that option under the More menu on the top right of
the page.

|image465|

This will generate a text file with one barcode per line.

.. _holds-history-label:

Holds history
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The holds history tab shows all the holds the patron has made, with their status.

|image1496|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: holdshistory-table).

.. _modification-log-label:

Modification log
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you have set your :ref:`BorrowersLog` to track changes
to patron records, then this tab will appear. The Modification log will
show when changes were made to the patron record. If you also have
turned on the :ref:`IssueLog` and :ref:`ReturnLog`
you will see checkins and outs on this screen as well.

|image466|

-  The Librarian field shows the patron number for the librarian who
   made the changes

-  The module lists 'MEMBERS' for the patron module

-  The action will tell you what action was being logged

-  The Object field lists the borrowernumber that is being modified (in
   the example above, it was my changing my own record)

.. _notices-label:

Notices
~~~~~~~~~~~~~~~~~~~~~~~~~

The `patron's messaging preferences <#setpatronmessaging>`__ are set
when :ref:`adding <add-a-new-patron-label>` or :ref:`editing <editing-patrons-label>` the
patron. This tab will show the messages that have been sent and those
that are queued to be sent:

|image467|

Clicking on the message title will expand the view to show you the full
text of the message that was sent.

|image468|

If the message has a status of sent or failed you will have the option
to 'resend' the message to the patron by clicking the 'resend' button
found under the status.

|image469|

.. _statistics-label:

Statistics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Depending on what you set for the values of your
:ref:`StatisticsFields` system preference, you can see
statistics for one patron's circulation actions.

|image470|

.. _files-label:

Files
~~~~~~~~~~~~~~~~~~~~~~~~

If you set the :ref:`EnableBorrowerFiles` preference
to 'Do' the Files tab will be visible on the patron information page.

|image471|

From here you can upload files to attach to the patron record.

|image472|

All files that are uploaded will appear above a form where additional
files can be uploaded from.

|image473|

.. _purchase-suggestions-label:

Purchase suggestions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If the patron has made any purchase suggestions you will see a purchase
suggestions tab on the patron record.

|image1247|

From here you can see all suggestions made by the patron and their
status, you can also create a purchase suggestion on the patron's behalf
by clicking the 'New purchase suggestion' button at the top.

Learn more about :ref:`managing purchase suggestions <managing-purchase-suggestions-label>` in the
`Acquisitions <#acqmodule>`__ chapter of this manual.

.. _patron-discharges-label:

Patron discharges
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A discharge is a certificate that says the patron has no current
checkouts, no holds and owe no money. To enable this opti`on on the
patron record you need to set the :ref:`useDischarge`
system preference to 'Allow'.

    **Note**

    In France a "quitus" ("discharge") is needed if you want to register
    for an account in a library or a university.

    **Note**

    Academic libraries often require that you have a clear record at the
    library before you can graduate.

Patrons can :ref:`request discharges via the OPAC <ask-for-a-discharge-label>`. Any
pending discharges will be listed below the menu buttons on the main
staff client page

|image1248|

Clicking the pending requests will open a screen where you can allow
those discharges

|image1249|

To generate a discharge for a specific patron click the 'Discharge' tab
on the left of the patron record

|image1250|

If the patron can have a discharge generated then it will have a button
that says 'Generate discharge'

|image474|

If not then you'll see an error explaining why you can't discharge the
patron.

|image475|

Once the letter is generated you will have a PDF to download

|image476|

    **Note**

    You can style the PDF using the :ref:`NoticeCSS`
    preference.

The patron will have a restriction added to their account

|image1251|

And a history of discharges will be added to the 'Discharge'
tab

|image1252|

.. _housebound-patrons-label:

Housebound patrons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There are three roles a patron can have in regard to housebound
circulation: borrower, chooser or deliverer.

    **Important**

    In order to use the housebound module, the :ref:`HouseboundModule`
    and :ref:`ExtendedPatronAttributes` system preferences must be
    enabled.

.. _housebound-chooser-label:

Chooser
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you have enabled the housebound module, with the
:ref:`HouseboundModule` system preference, you will see that
patrons now have a new section in their record called 'Housebound
roles'.

|image1349|

Click the 'Add' button to mark this
patron as a 'Chooser'.

|image1350|

The chooser is in charge of choosing the materials for the
housebound patron.

.. _housebound-deliverer-label:

Deliverer
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In the 'Housebound roles', click the 'Add' button to mark
this patron as a 'Deliverer'.

|image1351|

The deliverer is in charge of delivering the chosen materials
to the housebound patron on a specific day at a specific time.

.. _housebound-borrower-label:

Housebound borrowers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To create a housebound profile for an housebound patron, click on
the 'Housebound' tab in their record.

|image1347|

From there, you can edit their housebound profile information.

|image1348|

- Delivery day: choose which day (or 'Any') the patron prefers to
  receive their delivery.

- Frequency: choose the frequency at which they want to receive
  their deliveries.

    **Note**

    The frequencies are managed through the HSBND\_FREQ list of
    :ref:`authorized values <existing-values-label>`.

- Preferred materials: enter notes that will help the chooser
  choose appropriate documents for the housebound patron.

  For example: books, dvds, magazines, etc.

- Subjects: if the housebound patron has a preference for
  particular subjects, enter it here. This will help the
  chooser choose interesting documents for the patron.

  For example: romance, cookbooks, thrillers, etc.

- Authors: if the housebound patron has favorite authors,
  enter them here.

  For example: Danielle Steel, James Patterson, etc.

- Referral: if the housebound patron has a referral, enter
  it here.

- Notes: enter any other notes that may help the chooser or
  the deliverer.

Click the 'Save changes' button to save the housebound profile.

.. _housebound-deliveries-label:

Coordinating deliveries
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To plan visits, go to the housebound patron's record.

In their housebound tab, you will be able to create deliveries.

|image1352|

Click on 'Add a new delivery'.

|image1353|

Fill out the information :

  - Date: Enter the date of the delivery.

  - Time: Select a time of day for the delivery. The choices are
    morning, afternoon, or evening.

  - Chooser: Select a chooser who will be in charge of selecting
    the materials for this housebound patron.

  - Deliverer: Select a deliverer who will be in charge of picking
    up the materials and bringing them over to the housebound
    patron.

|image1354|

Choosers and Deliverers can be notified of planned deliveries via reports.  Example reports be found in the SQL Reports Library at https://wiki.koha-community.org/wiki/SQL_Reports_Patrons#Patron_Characteristics.

.. _patron-search-label:

Patron search
---------------------------------

Clicking on the link to the Patron module will bring you to a
search/browse screen for patrons. From here you can search for a patron
by any part of their name or their card number.

|image477|

Clicking the small plus sign [+] to the right of the search box will
open up an advanced patron search with more filters including the
ability to limit to a specific category and/or library.

|image478|

You can also filter your patron results using the search options on the
left hand side of the page.

|image1253|

Depending on what you have chosen for the 'Search fields' you can search
for patrons in various different ways.

|image479|

-  Standard:

   -  Enter any part of their name, username, email address or barcode

-  Email:

   -  Enter any part of their email address and choose 'Contains'
      instead of 'Starts with'

-  Borrower number:

   -  Enter the Koha borrower number

-  Phone number:

   -  Enter the phone number exactly as it is in the system or by using
      spaces between each batch of numbers.

   -  Example: To find (212) 555-1212 you can search for it exactly as
      it was entered or by searching for 212 555 1212

-  Street address:

   -  Enter any part of the patron's address (includes all address
      fields) and choose 'Contains' instead of 'Starts with' to find the
      string anywhere in the address

-  Date of birth

   -  Birth dates should be entered using the format set forth in the
      :ref:`dateformat` preference.

-  Sort field 1

   -  This is a custom field that libraries can use for any type of data
      about the patron.

-  Sort field 2

   -  This is a custom field that libraries can use for any type of data
      about the patron.

You can also choose to either search for fields that start with the
string you entered or contain the string. Choosing 'Contains' will work
like a wildcard search.

|image480|

You can also browse through the patron records by clicking on the linked
letters across the top.

|image481|

If your search only returns one result, you will be taken directly to the 
patron's file. If your search returns more than one result, you will be given 
a list from which to choose.

|image1495|

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: memberresultst).

.. _communication-with-patrons-label:

Communicating with patrons
-------------------------------------------------------------------------------

Koha offers several options for communicating with patrons, some of which have 
already been covered in this chapter.

.. _opac-notes-label:

OPAC notes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

OPAC notes are added to the patron's file through the 
:ref:`add patron form<add-a-new-patron-label>` or the 
:ref:`edit patron form <editing-patrons-label>`, in the 'Library set-up' 
section.

|image414|

They show up in the :ref:`'Your summary' section <your-summary-label>` of the 
patron's online account in the OPAC.

|image1504|

In the staff interface, OPAC notes will be in the 'Library use' section of the 
patron's file.

|image429|

.. _opac-messages-label:

OPAC messages
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

OPAC messages are added to the patron's file using the 'Add message' button.

|image427|

To leave a message that the patron will be able to see in the OPAC, choose 
"OPAC - Patron's name" in the 'Add a message for' field. Enter your message 
in the box, or choose a predefined message in the drop-down menu.

|image1505|

     **Note**

     Predefined messages are added in the BOR\_NOTES 
     :ref:`authorized value category <existing-values-label>`

Once saved, the patron will be able to see the message in the 
:ref:`'Your summary' section <your-summary-label>` of their online account.
The patron will also be able to see the date on which the message was added as 
well as the name of the branch.

|image1506|

In the staff interface, OPAC messages are shown on the patron's detail page, 
at the top of the page just under the row of action buttons.

|image1507|

It will also appear on the checkout page, to the right of the checkout box.

|image1508|

.. _advance-notices-and-hold-notices-label:

Advance notices and hold notices
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you have enabled the :ref:`EnhancedMessagingPreferences` system preference, 
you cat set advance notices as well as hold notices when 
:ref:`adding a new patron <add-a-new-patron-label>` or 
:ref:`editing a patron <editing-patrons-label>`.

If the :ref:`EnhancedMessagingPreferencesOPAC` system preference is set to 
'show', patrons will be able to modify their messaging preferences in their 
online account.

|image417|

-  Item due: A notice on the day and item is due back at the library

   -  Customize this notice by editing the DUE or DUEDGST notices in the 
      :ref:`Notices & slips tool <notices-and-slips-label>`

-  Advance notice: A notice in advance of the patron's items being due (the 
   patron can choose the number of days in advance)

   -  Customize this notice by editing the PREDUE or PREDUEDGST notices 
      in the :ref:`Notices & slips tool <notices-and-slips-label>`

-  Hold filled: A notice when you have confirmed the hold is waiting for the 
   patron

   -  Customize this notice by editing the HOLD notice in the 
      :ref:`Notices & slips tool <notices-and-slips-label>`

-  Item check-in: A notice that lists all the of the items the patron has just 
   checked in

   -  Customize this notice by editing the CHECKIN notice in the 
      :ref:`Notices & slips tool <notices-and-slips-label>`

-  Item checkout: A notice that lists all the of the items the patron has just 
   checked out and/or renewed, this is an electronic form of the checkout 
   receipt

   -  Customize this notice by editing the CHECKOUT notice in the 
      :ref:`Notices & slips tool <notices-and-slips-label>`

Patrons can choose to receive their notices as a digest by checking the 
'Digest only' box along with the delivery method. A digest is a combination of 
all the messages of that type (so all items due in 3 days in one email) in to 
one email instead of multiple emails for each alert.

The delivery methods currently supported are: 

-  Email
-  SMS (text messages)
-  Automated phone call system
-  Print

To generate the advance notices (advance notice and item due), you need to run the 
:ref:`advance\_notices.pl cronjob <cron-advanced-notice-label>`. Then, the 
:ref:`process\_message\_queue.pl cronjob <cron-message-queue-label>` will send 
the notices or the :ref:`gather\_print\_notices.pl cronjob <cron-print-hold-notices-label>` 
will gather them in a nice file you can print out and send out via regular mail.

.. _overdue-notices-label:

Overdue notices
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Overdue notices are managed in :ref:`Notices & slips <notices-and-slips-label>` 
and when they are sent is managed in 
:ref:`Overdue notice/status triggers <overdue-notice/status-triggers-label>`.

Patrons cannot opt out of receiving overdue notices like they can other 
notices (such as :ref:`advance notices or hold notices <advance-notices-and-hold-notices-label>`)

To generate the overdue notices , you need to run the 
:ref:`overdue\_notices.pl cronjob <cron-overdue-notice-label>`. Then, the 
:ref:`process\_message\_queue.pl cronjob <cron-message-queue-label>` will send 
the notices or the :ref:`gather\_print\_notices.pl cronjob <cron-print-hold-notices-label>` 
will gather them in a nice file you can print out and send out via regular mail.

.. _patron-emailer-label:

Custom emails
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

