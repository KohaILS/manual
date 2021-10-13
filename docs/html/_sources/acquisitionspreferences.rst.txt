.. include:: images.rst

.. _acquisitions-system-preferences-label:

Acquisitions
-------------------------------------------------------------------------------

*Get there:* More > Administration > Global system preferences > Acquisitions

.. _acquisitions-edifact-system-preferences-label:

EDIFACT
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _edifactinvoiceimport-label:

EdifactInvoiceImport 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ automatically import EDIFACT invoice message files when they are 
downloaded. 

Default: Do

Values:

-  Do

-  Don't

Description:

-  This feature allows libraries to delay the importing of EDI invoices until a 
   time of their choosing. If the syspref is set to 'Don't' the invoices are imported 
   into the database but the invoice processing is skipped. Instead, any invoice file 
   listed in EDIfact messages with a status of 'New' will have an 'Import' button to process the invoice manually.

.. _acquisitions-policy-label:

Policy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _acqcreateitem-label:

AcqCreateItem
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Create an item when \_\_\_.

Default: placing an order

Values:

-  cataloging a record

-  placing an order

-  receiving an order

Description:

-  This preference lets you decide when you'd like to create an item record in 
   Koha. 

-  If you choose to add an item record when 'placing an order', you will enter 
   item information in as you :ref:`add records in your basket <create-a-basket-label>`. 

-  If you choose to add the item when 'receiving an order' you will be asked 
   for item record information when you're :ref:`receiving orders <receiving-orders-label>` 
   in acquisitions.

-  If you choose to add the item when 'cataloging a record' then item records 
   will not be created in acquisitions at all. You will need to go to the 
   :ref:`cataloging module <cataloging-label>` to
   :ref:`add the items <adding-items-label>`.

-  Note that this setting can be overridden when 
   :ref:`creating a basket <create-a-basket-label>`.

.. _acqenablefiles-label:

AcqEnableFiles
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ enable the ability to upload and attach arbitrary files to
invoices.

Default: Don't

Values:

-  Do

-  Don't

Description:

-  This preference controls whether or not you allow the 
   :ref:`uploading of invoice files <attaching-files-to-invoices-label>` via 
   the acquisitions module.

.. _acqitemsetsubfieldswhenreceiptiscancelled-label:

AcqItemSetSubfieldsWhenReceiptIsCancelled
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Upon cancelling a receipt, update the item's subfields if they
were created when placing an order (e.g. o=5\|a="bar foo""). \_\_\_

Description:

-  This preference is used in conjunction with the
   :ref:`AcqItemSetSubfieldsWhenReceived`
   preference. If you have the system set to enter default values when
   you receive you will want to have those values revert back if the
   receipt is cancelled. This preference allows you to do that.

.. _acqitemsetsubfieldswhenreceived-label:

AcqItemSetSubfieldsWhenReceived
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Upon receiving items, update their subfields if they were created
when placing an order (e.g. o=5\|a="foo bar"). \_\_\_

Description:

-  This preference allows you to set default values for items that you
   receive via acquisitions. Enter the data as subfield=value and split
   your values with a bar ( \| ). For example you can remove the Ordered
   status on the item automatically when you receive it just by entering
   7=0 in this preference. That will set the Not for Loan status
   (subfield 7) to 0 which is available.

.. _acqviewbaskets-label:

AcqViewBaskets
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Show baskets \_\_\_

Default: created or managed by staff member

Values:

-  in system, regardless of owner

-  from staff member's library

-  created or managed by staff member

Description:

-  When in acquisitions, this preference allows you to control whose
   baskets you can see when looking at a vendor. 

-  The default value of 'created or managed by staff member' makes it so that 
   you only see the baskets you created. 

-  Choosing to see baskets 'from staff member's library' will show you the 
   baskets created by anyone at the branch you're logged in at. 

-  Finally, you can choose to set this preference to show you all baskets 
   regardless of who created it ('in system, regardless of owner'). 

-  Regardless of which value you choose for this preference,
   superlibrarians can see all baskets created in the system.

.. _acqwarnonduplicateinvoice-label:

AcqWarnOnDuplicateInvoice
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ when the librarian tries to create an invoice with a
duplicate number.

Default: Do not warn

Values:

-  Do not warn

-  Warn

Description:

-  When set to 'Warn', Koha will let staff know if an invoice with the same 
   number has already been created. The staff member will have a choice to 
   either receive on the existing invoice or create a new one with the same 
   number.

|acqwarnonduplicateinvoice|

.. _basketconfirmations-label:

BasketConfirmations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: When closing or reopening a basket, \_\_\_.

Default: always ask for confirmation

Values:

-  always ask for confirmation

-  do not ask for confirmation

Descriptions:

-  This preference adds the option to skip confirmations on closing and
   reopening a basket. If you skip the confirmation, you do not create a
   new basket group.

.. _claimsbcccopy-label:

ClaimsBccCopy
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ blind copy (BCC) to logged in user when sending serial or
acquisitions claims notices.

Default: Don't send

Values:

-  Don't send

-  Send

Description:

-  This system preference allows you to choose whether or not you want to send 
   a copy of the claim email to the staff member when 
   :ref:`claiming a late serial issue <claim-late-serials-label>` or a
   :ref:`late acquisitions order <claims-and-late-orders-label>`.

.. _currencyformat-label:

CurrencyFormat
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Display currencies using the following format \_\_\_

Default: 360,000.00 (US)

Values:

-  360'000.00 (CH)

-  360 000,00 (FR)

-  360,000.00 (US)

Description:

-  This system preference controls how prices are displayed in Koha.

.. _emailpurchasesuggestions-and-emailaddressforsuggestions-label:

EmailPurchaseSuggestions and EmailAddressForSuggestions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Choose email address that new purchase suggestions will be sent to: 
\_\_\_. If you choose EmailAddressForSuggestions you have to enter a valid 
email address: \_\_\_

Default: none

Values:

-  none

-  email address of branch

-  EmailAddressForSuggestions

-  KohaAdminEmailAddress

Description:

-  If you want Koha to send purchase suggestions via email, choose which email 
   address it should send them to

   -  none will deactivate this feature

   -  email address of branch will use the email address entered in the 
      :ref:`libraries settings <libraries-label>`

   -  if you choose EmailAddressForSuggestions, enter the email address in the 
      input field

   -  if you choose KohaAdminEmailAddress, the email will be sent to the main
      email address, as entered in :ref:`KohaAdminEmailAddress`

-  You can customize the message that is sent with the 
   :ref:`Notices and slips tool <notices-and-slips-label>`, the letter code is 
   NEW\_SUGGESTION

.. _marcfieldstoorder-label:

MarcFieldsToOrder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Set the mapping values for a new order line created from a MARC
record in a staged file.

Description:

-  This preference includes MARC fields to check for order information
   to use when you :ref:`order from a new .mrc file <order-from-a-new-file-label>` 
   or when you :ref:`order from a staged file <order-from-a-staged-file-label>` in
   acquisitions. You can use the following fields: 

   -  price, 

   -  quantity,

   -  budget\_code, 

   -  discount, 

   -  sort1, and

   -  sort2.

   For example:

   ::

       price: 947$a|947$c
       quantity: 969$h
       budget_code: 922$a

.. Warning ::

   Requires YAML syntax to work

   This means

   -  Make sure there is NO space between the field name and the colon

   -  Make sure there IS a space between the colon and the value

   -  Make sure each pair is on its own line

.. _marcitemfieldstoorder-label:

MarcItemFieldsToOrder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Set the mapping values for new item records created from a MARC record
in a staged file.

Description:

-  This preference automatically generates items in Koha with populated
   information based on a 9XX field and subfield. You can use the following
   fields: 

   -  homebranch, 

   -  holdingbranch, 

   -  itype, 

   -  nonpublic\_note, 

   -  public\_note, 

   -  loc,

   -  ccode, 

   -  notforloan, 

   -  uri, 

   -  copyno, 

   -  price, 

   -  replacementprice, and 

   -  itemcallnumber.
   
-  You can also use the following special fields: 

   -  quantity, and 

   -  budget_code.

For example:

::

       homebranch: 975$a
       holdingbranch: 975$b
       public_note: 975$z
       loc: 975$c

.. Warning ::

   Requires YAML syntax to work

   This means

   -  Make sure there is NO space between the field name and the colon

   -  Make sure there IS a space between the colon and the value

   -  Make sure each pair is on its own line

.. _orderpricerounding-label:

OrderPriceRounding
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ to nearest cent.

Default: Don't round

Values:

-  Don't round

-  Round

Description:

-  This system preference determines whether full precision values or rounded 
   values should be used in price calculations. 

-  This is particularly important when your tax rates have more decimals than 
   your currency

.. _purgesuggestionsolderthan-label:

PurgeSuggestionsOlderThan
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Keep accepted or rejected purchase suggestions for a period of \_\_\_ 
days.

.. Warning ::

    Leave this field empty if you don't want to activate this automatic 
    feature.

Description:

-  Enter the number of days after which you want to automatically
   delete accepted or rejected purchase suggestions.

-  For example: [30] Sets purgation of suggestions for those older than 30 days.

.. Note ::

    This system preference is used when the cronjob 
    :ref:`purge_suggestions.pl <cron-clean-up-old-suggestions-label>` is
    active and called without a specific number of days.

.. _taxrates-label:

TaxRates
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Tax rates are \_\_\_

Default: 0

Description:

-  This preference allows the library to define goods and services tax rates 
   for acquisitions.

-  The first item in the list will be selected by default.

.. Note ::

   Enter this value as a number (.06) versus a percent (6%).

   For more than one value, separate with \| (pipe).

   For example

   0|0.05|0.1496

   will give you choices of tax rates of 0%, 5% and 14.96%

.. Warning ::

   The database only accepts values up to 4 decimals, further values will be 
   rounded. 

.. _uniqueitemfields-label:

UniqueItemFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: The following database columns should be unique in an item: \_\_\_

Default: barcode

Description:

-  If this preference is left blank when adding items in acquisitions
   there will be no check for uniqueness. This means that a duplicate
   barcode can be created in acquisitions which will cause errors later
   when checking items in and out.

.. _useacqframeworkforbibliorecords-label:

UseACQFrameworkForBiblioRecords
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the framework 'ACQ' for bibliographic records fields

Default: Don't use

Values:

-  Don't use

-  Use

Description:

-  This system preference allows you to use the 
   :ref:`ACQ bibliographic framework <marc-bibliographic-frameworks-label>` to 
   customize the bibliographic record fields that are shown when ordering from 
   acquisitions

-  Note that this does not affect the item fields (in MARC21, field 952), which 
   are always taken from the ACQ framework regardless of this system preference

.. _acquisitions-printing-system-preferences-label:

Printing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _orderpdfformat-label:

OrderPdfFormat
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Use the \_\_\_ layout when printing basket groups.

Default: English 3-page

Values:

.. Note ::

   Values will depend on the installed languages in your Koha installation.

-  2-page

-  3-page

Description:

-  This preference determines how :ref:`basket groups <create-a-basket-group-label>` 
   are printed when exported as PDFs.

-  A 2-page layout will have vendor information on the first page and ordered 
   titles on the second page

-  A 3-page layout will additionally have a page with basket informations

