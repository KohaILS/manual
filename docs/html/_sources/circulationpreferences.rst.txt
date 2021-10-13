.. include:: images.rst

.. _circulation-system-preferences-label:

Circulation
----------------------------

*Get there:* More > Administration > Global System Preferences >
Circulation

.. _article-requests-sysprefs-label:

Article Requests
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _articlerequests-label:

ArticleRequests
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ patrons to place article requests.

Values:

-  Enable

-  Don't enable

Description:

-  This preference controls whether or not article requests are allowed to be placed by patrons in the OPAC.

.. _articlerequestslinkcontrol-label:

ArticleRequestsLinkControl
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Use algorithm to show or hide

Asks: \_\_\_ article request link on search results.

Values:

-  Always show

-  Use algorithm to show or hide

Description:

-  On the OPAC results page, either always show the 'Request article' link
   or check the branch, patron and item type combination to determine
   whether or not an article can be requested from this particular record
   before displaying the link.

.. _articlerequestsmandatoryfields-label:

ArticleRequestsMandatoryFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: None selected

Asks: For records that are record level or item level requestable, make the following fields mandatory \_\_\_

Values:

-  [Select all]

-  Author

-  Chapters

-  Date

-  Issue

-  Pages

-  Title

-  Volume

Description:

-  This preference controls what fields must be filled in before an article request can be placed
   for either a record level or item level request. Choosing [Select all] indicates that all fields
   listed (Author, Chapters, Date, Issue, Pages, Title, Volume) must be completed before the article
   request can be placed.

.. _articlerequestsmandatoryfieldsitemsonly-label:

ArticleRequestsMandatoryFieldsItemsOnly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: None selected

Asks: For records that are only item level requestable, make the following fields mandatory \_\_\_

Values:

-  [Select all]

-  Author

-  Chapters

-  Date

-  Issue

-  Pages

-  Title

-  Volume

Description:

-  This preference controls what fields must be filled in before an article request can be placed
   for an item level request only. Choosing [Select all] indicates that all fields
   listed (Author, Chapters, Date, Issue, Pages, Title, Volume) must be completed before the article
   request can be placed.

.. _articlerequestsmandatoryfieldsrecordonly-label:

ArticleRequestsMandatoryFieldsRecordOnly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: None selected

Asks: For records that are only record level requestable, make the following fields mandatory \_\_\_

Values:

-  [Select all]

-  Author

-  Chapters

-  Date

-  Issue

-  Pages

-  Title

-  Volume

Description:

-  This preference controls what fields must be filled in before an article request can be placed
   for a record level request only. Choosing [Select all] indicates that all fields
   listed (Author, Chapters, Date, Issue, Pages, Title, Volume) must be completed before the article
   request can be placed.

.. _batch-checkout-label:

Batch Checkout
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _batchcheckouts-label:

BatchCheckouts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ batch checkouts

Values:

-  Allow

-  Don't allow

.. _batchcheckoutsvalidcategories-label:

BatchCheckoutsValidCategories
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Patron categories allowed to checkout in a batch \_\_\_ (list of
patron categories separated with a pipe ^\|^)

.. _checkin-policy-label:

Checkin policy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _blockreturnoflostitems-label:

BlockReturnOfLostItems
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ returning of items that have been lost.

Default: Don't block

Values:

-  Block

-  Don't block

Description:

-  This preference controls whether and item with a lost status
   (952$1 in MARC21) can be checked in or not.

.. _blockreturnofwithdrawnitems-label:

BlockReturnOfWithdrawnItems
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ returning of items that have been withdrawn.

Default: Block

Values:

-  Block

-  Don't block

Description:

-  This preference controls whether and item with a withdrawn status
   (952$0 in MARC21) can be checked in or not.

.. _calculatefinesonbackdate-label:

CalculateFinesOnBackdate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ calculate and update overdue charges when an item is returned with 
a backdated return date.

Default: Do

Values:

-  Do

-  Don't

Description:

-  This system preference is similar to :ref:`CalculateFinesOnReturn` but is 
   used when checkins are backdated either through the book drop mode or the 
   specified return date (see :ref:`SpecifyReturnDate`).

.. _calculatefinesonreturn-label:

CalculateFinesOnReturn
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ calculate and update overdue charges when an item is
returned.

Default: Do

Values:

-  Do

-  Don't

Description:

-  If this preference is set to "Do" and the :ref:`fines cron
   job <cron-fines-label>` is off then Koha will calculate fines only
   when items are returned. If you have the fines cron job on and this
   preference set to "Do" then this preference will calculate fines
   based on the cron (usually run nightly) and then again when you check
   the item in. This option is best for those who are doing hourly
   loans. If this preference is set to "Don't" then fines will only be
   accrued if the fines cron job is running.

    **Important**

    If you are doing hourly loans then you should have this set to 'Do'.

    **Important**

    The :ref:`finesMode` system preference must be set to 'Calculate and charge' 
    in order for this system preference to have any effect.

.. _cumulativerestrictionperiods-label:

CumulativeRestrictionPeriods
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the restriction periods.

Default: Don't cumulate

Values:

-  Don't cumulate

-  Cumulate

Description:

-  This system preference controls whether or not restriction periods should be 
   served concurrently or consecutively.

-  If set to 'Don't cumulate', the patron will be restricted only for the 
   longest period. (For example, if a patron has a restriction of 10 days and
   another restriction of 15 days, they will be restricted for 15 days.)

-  If set to 'Cumulate', the patron will be restricted for the sum of all the 
   restriction period. (For example, if a patron has a restriction of 10 days 
   and another restriction of 15 days, they will be restricted for 25 days.)

.. _hidepersonalpatrondetailoncirculation-label:

HidePersonalPatronDetailOnCirculation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ hide patrons phone number, email address, street address
and city in the circulation page

Default: Don't

Values:

-  Don't

-  Do

Description:

-  This preference controls the display of the patron's phone number,
   email address, and physical address from the left side of the screen
   (under their picture, if they have one).

-  Set to 'Do' these informations will only be visible on the patron's
   detail page.

.. _holdsautofill-label:

HoldsAutoFill
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ automatically fill holds instead of asking the librarian.

Default: Don't

Values:

-  Do

-  Don't

Description:

-  If set to 'Do', the holds confirmation pop-up will not appear upon checking
   in a reserved item.

.. _holdsautofillprintslip-label:

HoldsAutoFillPrintSlip
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ automatically display the holds slip dialog for auto-filled holds.

Default: Don't

Values:

-  Do

-  Don't

Description:

-  If set to 'Do', the holds slip print pop-up will appear automatically
   upon checking in a reserved item.

-  :ref:`HoldsAutoFill` must be set to 'do' for this preference to have any
   effect.

.. _holdsneedprocessingsip-label:

HoldsNeedProcessingSIP
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ holds automatically if matching item is returned via SIP protocol.

Default: Fulfill

Values:

-  Fulfill

-  Don't fulfill

Description:

-  This system preference controls whether or not holds are automatically filled 
   by items returned via SIP (sorter, auto check-in stations, etc.)

.. _skipholdtraponnotforloanvalue-label:

SkipHoldTrapOnNotForLoanValue
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Never trap items with 'not for loan' values of \_\_\_ to fill holds.

Description:

-  This system preference is used to completely exclude items with 'not for loan' 
   values from filling holds.

-  Enter :ref:`NOT\_LOAN authorized values <existing-values-label>` separated 
   by pipes (\|).

.. _storelastborrower-label:

StoreLastBorrower
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the last patron to return an item.

Default: Don't store

Values:

-  Don't store

-  Store

Description:

-  This preference allows you to store the last patron to borrow an item
   even if the patron has chosen to have their reading history
   anonymized.

    **Note**

    This setting is independent of
    :ref:`opacreadinghistory` and/or
    :ref:`AnonymousPatron`.

.. _transfersblockcirc-label:

TransfersBlockCirc
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ staff from continuing to checkin items when a transfer is 
triggered.

Default: Block

Values:

-  Don't block

-  Block

Description:

-  This system preference controls whether or not the transfer pop-up blocks
   further checkins.

.. _trapholdsonorder-label:

TrapHoldsOnOrder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ items that are not for loan but holdable (notforlan < 0) to fill 
holds.

Default: Trap

Values:

-  Don't trap

-  Trap

Description: 

-  This system preference controls whether or not items that have a 
   :ref:`NOT_LOAN authorized value <existing-values-label>` smaller than 0 
   (which means that the item can be put on hold, but not checked out), should 
   be used to fill holds.

.. _updateitemlocationincheckin-label:

UpdateItemLocationOnCheckin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: This is a list of value pairs. The first value is followed immediately
by colon, space, then the second value.

Description:

-  This system preference affects the item's current and permanent locations
   when the item is checked in (whether it was checked out or not).

-  If the location value on the left of the colon (:) matches
   the item's current location, it will be updated to match the location value
   on the right of the colon (:).

-  The values are the LOC :ref:`authorised values <existing-values-label>`.

-  For example, 'STAFF: GEN' will move an item from the staff office to the
   general collection when the item is checked in.

-  Special terms

   -  PROC: Processing center. When using PROC, only the current location will
      be affected.

   -  CART: Shelving cart. When using CART, only the current location will be
      affected.

   -  \_PERM\_: This will use the item's permanent location, whatever that
      location is.

   -  \_BLANK\_: Used on the left as a first value, it will add a location if
       there is none. Used on the right as a second value, it will remove the
       location.

   -  \_ALL\_: Used on the left as a first value, it will affect all items and
      override all other rules.

.. Warning ::

   Requires YAML syntax to work

   This means

  -  Make sure there is NO space between the first value and the colon

  -  Make sure there IS a space between the colon and the second value

  -  Make sure each pair is on its own line

-  If using PROC or CART, use the 
   :ref:`cart\_to\_shelf cron job <cron-in-processing/book-cart-label>` to 
   return the items to their permanent location after a determined number of 
   hours.

.. _updatenotforloanstatusoncheckin-label:

UpdateNotForLoanStatusOnCheckin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: This is a list of value pairs. When an item is checked in, if the
not for loan value on the left matches the items not for loan value it
will be updated to the right-hand value.

Description:

-  This system preference affects the item's 'not for loan' status
   when the item is checked in (whether it was checked out or not).

-  If the status value on the left of the colon (:) matches
   the item's current status, it will be updated to match the status value
   on the right of the colon (:).

-  The values are the NOT\_LOAN :ref:`authorised values <existing-values-label>`.

-  For example, '-1: 0' will cause an item that was set to 'Ordered' to now be 
   available for loan

.. Warning ::

   Requires YAML syntax to work

   This means

   -  Make sure there is NO space between the first value and the colon

   -  Make sure there IS a space between the colon and the second value

   -  Make sure each pair is on its own line

.. _checkout-policy-label:

Checkout Policy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _agerestrictionmarker-label:

AgeRestrictionMarker
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Restrict patrons with the following target audience values from
checking out inappropriate materials: \_\_\_

Description:

-  This preference defines certain keywords that will trigger Koha to
   restrict checkout based on age. These restrictions can be overridden
   by the :ref:`AgeRestrictionOverride`
   preference. Enter in this field a series of keywords separated by bar
   (\|) with no spaces. For example PG\|R\|E\|EC\|Age\| will look for PG
   followed by an age number, R folllowed by an age number, Age followed
   by an age number, and so on. These values can appear in any MARC
   field, but Library of Congress recommends the 521$a (Target Audience
   Note). Whatever field you decide to use you must map the word
   agerestriction in the biblioitems table to that field in the :ref:`Koha to
   MARC Mapping <koha-to-marc-mapping-label>`. When cataloging you can enter
   values like PG 13 or E 10 in the 521$a and Koha will then notify
   circulation librarians that the material may not be recommended for
   the patron based on their age.

       **Important**

       You must map the word agerestriction in the biblioitems table to
       the MARC field where this information will appear via the :ref:`Koha
       to MARC Mapping <koha-to-marc-mapping-label>` administration area.

.. _agerestrictionoverride-label:

AgeRestrictionOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ staff to check out an item with age restriction.

Values:

-  Allow

   |image25|

-  Don't allow

   |image26|

Description:

-  When the :ref:`AgeRestrictionMarker` preference
   is set, Koha will try to warn circulation librarians before checking
   out an item that might have an age restriction listed in the MARC
   record. This preference asks if you would like the staff to be able
   to still check out these items to patrons under the age limit.

.. _allfinesneedoverride-label:

AllFinesNeedOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Require

Asks: \_\_\_ staff to manually override all fines, even fines less than
:ref:`noissuescharge`.

Values:

-  Don't require

-  Require

Description:

-  This preference let's you decide if you want to always be warned that
   the patron has fines when checking out. If you have it set to
   'Require' then no matter how much money the patron owes a message
   will pop up warning you that the patron owes money.

.. _allowfineoverride-label:

AllowFineOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ staff to manually override and check out items to patrons
who have more than :ref:`noissuescharge` in fines.

Values:

-  Allow

-  Don't allow

Description:

-  This preference lets you decide if you staff can check out to patrons
   who owe more money than you usually let them carry on their account.
   If set to 'Allow' staff will be warned that the patrons owes money,
   but it won't stop the staff from checking out to the patron.

.. _allowitemsonholdcheckoutsco-label:

AllowItemsOnHoldCheckoutSCO
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ checkouts of items reserved to someone else in the SCO module.
If allowed do not generate RESERVE_WAITING and RESERVED warning. This
allows self checkouts for those items.

Values:

-  Allow

-  Don't allow

    **Important**

    This system preference relates only to Koha's web based self checkout.

Description:

-  When this preference is set to 'Allow' patrons will be able to use
   Koha's web based self checkout to check out a book to themselves
   even if it's on hold for someone else. If you would like Koha to
   prevent people from checking out books that are on hold for someone
   else set this preference to "Don't allow".

.. _allowitemsonholdcheckout-label:

AllowItemsOnHoldCheckoutSIP
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ checkouts of items reserved to someone else via SIP checkout 
messages.

Default: Don't allow

Values:

-  Allow

-  Don't allow

    **Important**

    This system preference relates only to SIP-based self-checkout, not
    Koha's web based self checkout.

Description:

-  When this preference is set to 'Allow' patrons will be able to use
   your external self check machine to check out a book to themselves
   even if it's on hold for someone else.

-  If you would like Koha to prevent people from checking out books that are 
   on hold for someone else set this preference to 'Don't allow'.

.. _allowmultipleissuesonabiblio-label:

AllowMultipleIssuesOnABiblio
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ patrons to check out multiple items from the same record.

Values:

-  Allow

-  Don't allow

Description:

-  If this preference is set to 'Allow' then patrons will be able to
   check out multiple copies of the same title at the same time. If it's
   set to "Don't allow" then patrons will only be allowed to check out
   one item attached to a record at a time. Regardless of the option
   chosen in this preference records with subscriptions attached will
   allow multiple check outs.

       **Important**

       This will only effect records without a subscription attached.

.. _allownotforloanoverride-label:

AllowNotForLoanOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ staff to override and check out items that are marked as
not for loan.

Values:

-  Allow

-  Don't allow

Description:

-  This parameter is a binary setting which controls the ability of
   staff (patrons will always be prevented from checking these items
   out) to check out items that are marked as "not for loan". Setting it
   to "Allow" would allow such items to be checked out, setting it to
   "Don't allow" would prevent this. This setting determines whether
   items meant to stay in the library, such as reference materials, and
   other library resources can be checked out by patrons.

.. _allowrenewallimitoverride-label:

AllowRenewalLimitOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ staff to manually override the renewal limit and renew a
checkout when it would go over the renewal limit.

Values:

-  Allow

-  Don't allow

Description:

-  This preference is a binary setting which controls the ability of
   staff to override the limits placed on the number of times an item
   can be renewed. Setting it to "Allow" would allow such limits to be
   overridden, setting it to "Don't allow" would prevent this. This is a
   preference in which if it is set to "allow" it would allow the
   library staff to use their judgment for overriding the renew limit
   for special cases, setting it to "Don't allow" prevents an
   opportunity for abuse by the library staff.

.. _allowrenewalonholdoverride-label:

AllowRenewalOnHoldOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ staff to renew items that are on hold by manually specifying a due date.

Default: Don't allow

Values:

-  Allow

-  Don't allow

Description:

- This preference enables items that are on hold to be renewed with a due date specified by the user.

  It can appear in two locations:

  1. In the "Checkouts" table on the Patron Details screen. It is possible to select on loan items that would otherwise fulfil a hold request to be renewed. When such an item is selected, an additional date selection box is displayed to allow the user to specify the due date for all on hold items that are to be renewed.

  2. In the Circulation > Renew alert screen. When a barcode of an on loan item that would ordinarily fulfil a hold request is entered, the usual alert is displayed indicating that the item is on hold, it is still possible to override this, and renew. With this preference enabled it is also possible to specify a due date.

.. _allowreturntobranch-label:

AllowReturnToBranch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: to any library

Asks: Allow materials to be returned to \_\_\_

Values:

-  either the library the item is from or the library it was checked out
   from.

-  only the library the item is from.

-  only the library the item was checked out from.

-  to any library.

Description:

-  This preference lets the library system decide how they will accept
   returns. Some systems allow for items to be returned to any library
   in the system (the default value of this preference) others want to
   limit item returns to only specific branches. This preference will
   allow you to limit item returns (checkins) to the branch(es) set in
   the value.

.. _allowtoomanyoverride-label:

AllowTooManyOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ staff to override and check out items when the patron has
reached the maximum number of allowed checkouts.

Values:

-  Allow

   |image27|

-  Don't allow

   |image28|

Description:

-  If this preference is set to "Allow" then staff all will be presented
   with an option to checkout more items to a patron than are normally
   allowed in the :ref:`Circulation and fines rules`. If
   this preference is set to "Don't allow" then no staff member will be
   able to check out more than the circulation limit.

.. _automaticitemreturn-label:

AutomaticItemReturn
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Do

Asks: \_\_\_ automatically transfer items to their home branch when they
are returned.

Values:

-  Do

-  Don't

Description:

-  This preference is a binary setting which determines whether an item
   is returned to its home branch automatically or not. If set to
   "Don't", the staff member checking an item in at a location other
   than the item's home branch will be asked whether the item will
   remain at the non-home branch (in which case the new location will be
   marked as a holding location) or returned. Setting it to "Do" will
   ensure that items checked in at a branch other than their home branch
   will be sent to that home branch.

.. _autoremoveoverduesrestrictions-label:

AutoRemoveOverduesRestrictions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Do not

Asks: \_\_\_ allow OVERDUES restrictions triggered by sent notices to be
cleared automatically when all overdue items are returned by a patron.

Values:

-  Do

-  Do not

Description:

-  Using the :ref:`Overdue Notice/Status Triggers` you
   can restrict patrons after they receive an overdue notice. This
   preference lets you define whether Koha will automatically remove
   that restriction once the overdue items in question are returned or
   not.

.. _autoreturncheckedoutitems-label:

AutoReturnCheckedOutItems
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ require librarians to manually confirm a checkout where the item
is already checked out to another patron.

Values:

-  Do

-  Don't

Default: Do

Description:

-  This preference controls whether Koha asks for a confirmation when trying
   to check out an item that is already checked out to another patron.

-  Set to 'Do', Koha will ask the staff member to confirm the check out.

   |image1433|

-  Set to 'Don't', Koha will simply return the item from the previous
   patron's file and check it out to the actual patron and show a message.

   |image1434|

.. _circcontrol-label:

CircControl
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: the library the item is from

Asks: Use the checkout and fines rules of \_\_\_

Values:

-  the library the item is from

   -  The :ref:`circulation and fines policies <circulation-and-fines-rules-label>`
      will be determined by the item's library where :ref:`HomeOrHoldingBranch`
      chooses if item's home library is used or holding library is used.

-  the library the patron is from

   -  The :ref:`circulation and fines policies <circulation-and-fines-rules-label>`
      will be determined the patron's home library

-  the library you are logged in at

   -  The :ref:`circulation and fines policies <circulation-and-fines-rules-label>` will be
      determined by the library that checked the item out to the patron

.. _consideronsitecheckoutsasnormalcheckouts-label:

ConsiderOnSiteCheckoutsAsNormalCheckouts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ on-site checkouts as normal checkouts. If enabled, on-site 
checkouts will count toward the checkout limit for regular checkouts. The 
on-site limit will still apply for on-site checkouts. If disabled, both values 
will be checked separately.

Default: Consider

Values:

-  Consider

-  Don't consider

Description:

-  This preference allows you to decide if checkouts that are considered 
   :ref:`on-site checkouts <onsitecheckouts-label>` are counted toward the total
   checkouts a patron can have. You can also set your 
   :ref:`circulation and fines rules <circulation-and-fines-rules-label>` to 
   allow only a certain number of normal and on-site checkouts.

.. _defaultlongoverduechargevalue-label:

DefaultLongOverdueChargeValue
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Charge a lost item to the borrower's account when the LOST value
of the item changes to \_\_\_

Description:

-  Leave this field empty if you don't want to charge the user for lost
   items. If you want the user to be charged enter the `LOST authorized
   value <#lost>`__ you are using in the
   :ref:`DefaultLongOverdueLostValue <defaultlongoverduelostvalue-and-defaultlongoverduedays-label>`
   preference. This preference is used when the :ref:`longoverdue cron
   job <cron-long-overdues-label>` is called without the --charge parameter.

.. _defaultlongoverduelostvalue-and-defaultlongoverduedays-label:

DefaultLongOverdueLostValue and DefaultLongOverdueDays
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: By default, set the LOST value of an item to \_\_\_ when the item
has been overdue for more than \_\_\_ days.

Description:

-  These preferences are used when the :ref:`longoverdue cron
   job <cron-long-overdues-label>` is called without the --lost parameter. It
   allows users to set the values of the :ref:`longoverdue
   cron <cron-long-overdues-label>` without having to edit the crontab.
   Setting the values to 1 and 30 for example will mark the item with
   the `LOST authorized value <#lost>`__ of 1 after the item is 30 days
   overdue.

.. _holdsinnoissuescharge-label:

HoldsInNoissuesCharge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't include

Asks: \_\_\_ hold charges when summing up charges for noissuescharge.

Values:

-  Don't include

-  Include

.. _homeorholdingbranch-label:

HomeOrHoldingBranch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: the item's home library (homebranch).

Asks: Use the checkout and fines rules of \_\_\_

Values:

-  the item's home library (homebranch).

-  the item's holding library (holdingbranch).

Description:

-  This preference does several things.

   -  If :ref:`CircControl` is set to 'the library the item
      is from' then the :ref:`circulation and fines
      policies <circulation-and-fines-rules-label>` will be determined by the item's
      library where HomeOrHoldingBranch chooses if item's home library
      is used or holding library is used.

   -  If :ref:`IndependentBranches` is set to
      'Prevent' then the value of this preference is used in figuring
      out if the item can be checked out. If the item's home library
      does not match the logged in library, the item cannot be checked
      out unless you are a :ref:`superlibrarian <patron-permissions-defined-label>`.

    **Important**

    It is not recommend that this setting be changed after initial setup
    of Koha because it will change the behavior of items already checked
    out.

.. _issuelostitem-label:

IssueLostItem
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: display a message

Asks: When issuing an item that has been marked as lost, \_\_\_.

Values:

-  display a message

   |image29|

-  do nothing

   -  This option will just check the item out without notifying you
      that the item was marked lost.

-  require confirmation

   |image30|

Description:

-  This preference lets you define how library staff are notified that
   an item with a lost status is being checked out. This will help staff
   mark items as 'available' if you choose to 'display a message' or
   'require confirmation.^ If you choose to 'do nothing,^ there will be
   no notification that the item being checked out is marked as 'lost.^

.. _issuinginprocess-label:

IssuingInProcess
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't prevent

Asks: \_\_\_ patrons from checking out an item whose rental charge would
take them over the limit.

Values:

-  Don't prevent

-  Prevent

Description:

-  This preference determines if a patron can check items out if there
   is an overdue fine on the account and any of the materials the patron
   wishes to check out will potentially tip the account balance over the
   maximum fines policy the library has in place.

Example: Your library has a $5 limit set for 'fines' (ie, after
incurring $5 in fines, a patron can no longer check out items). A patron
comes to the desk with 5 items to check out (4 books and a video) The
patron has $4 in charges already on their account. One of the videos has
a rental charge of $1, therefore making the total fines on the patron's
account suddenly $5 (the limit).

.. _itemsdeniedrenewal-label:

ItemsDeniedRenewal
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Define custom rules to deny specific items from renewal.

Description:

-  This preference allows you to specify items that should not be renewed
   either from the OPAC or staff client.  You can enter any combination of
   fields (from the items table in the Koha database) followed by a colon
   then a space then a bracketed list of values separated by commas. e.g:

   ::

       ccode: [NEWFIC,NULL,DVD]
       itype: [NEWBK,""]

-  The word 'NULL' can be used to block renewal on undefined fields,
   while an empty string "" will block on an empty (but defined) field.

    **Note**

    If using automatic renewal notices your notice text should be updated to
    account for the new reason that renewals may be denied "item_denied_renewal".

.. _maninvinnoissuescharge-label:

ManInvInNoissuesCharge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Include

Asks: \_\_\_ custom debit types when summing up charges for
noissuescharge.

Values:

-  Don't include

-  Include

Description:

-  This preference lets you decide if charges entered as manual invoices
   are included when calculating the
   :ref:`noissuescharge`. If this is set to 'Include' then
   Koha will include all manual invoices when deciding if the patron
   owes too much money to check anything else out of the library. If
   it's set to 'Don't include' then Koha will ignore all manual invoice
   charges when figuring out if the patron owes too much money to
   checkout additional materials.

.. _marklostitemsasreturned-label:

MarkLostItemsAsReturned
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ items as returned when flagged as lost.

Default: Disable

Values:

-  [Select All]

-  From the :ref:`'holds to pull' <holds-to-pull-label>` list

-  From the :ref:`batch item modification tool <batch-item-modification-label>`

-  From the items tab of the catalog module

-  From the :ref:`longoverdue cronjob <cron-long-overdues-label>`

-  When cataloging an item

-  When marking an item as a return claim

-  When receiving a payment for the items

Description:

-  The library can choose which of these actions or all of these actions, does an
   item gets automatically returned from the patron's account or not.

.. _maxoutstanding-label:

maxoutstanding
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 5

Asks: Prevent patrons from making holds on the OPAC if they owe more
than \_\_\_ USD in fines.

.. _noissuescharge-label:

noissuescharge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 5

Asks: Prevent patrons from checking out books if they have more than
\_\_\_ USD in fines.

Description:

-  This preference is the maximum amount of money owed to the library
   before the user is banned from borrowing more items. Using the
   :ref:`ManInvInNoissuesCharge` and
   :ref:`RentalsInNoissuesCharge` preferences
   you can control which types of charges are considered in this total.
   This also coincides with :ref:`maxoutstanding` that
   limits patrons from placing holds when the maximum amount is owed to
   the library.

.. _noissueschargeguarantees-label:

NoIssuesChargeGuarantees
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Prevent a patron from checking out if the patron has guarantees
owing in total more than \_\_\_ USD in fines.

Description:

-  Allows a library to prevent patrons from checking out items if his or
   her guarantees owe too much in fines.

.. _norenewalbeforeprecision-label:

NoRenewalBeforePrecision
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: date

Asks: Calculate "No renewal before" based on \_\_\_.

Values:

-  date

-  exact time

    **Note**

    Only relevant for loans calculated in days, hourly loans are not
    affected.

Description:

-  This preference allows you to control how the 'No renewal before"
   option in the :ref:`Circulation and fines rules`
   administration area.

.. _noticebcc-label:

NoticeBcc
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Send all notices as a BCC to this email address \_\_\_

This preference makes it so that a librarian can get a copy of every
notice sent out to patrons.

    **Note**

    If you'd like more than one person to receive the blind copy you can
    simply enter in multiple email addresses separated by commas.

 .. _onsitecheckoutautocheck-label:

OnSiteCheckoutAutoCheck
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ onsite checkout by default if last checkout was an onsite one.

Values:

-  Don't enable

-  Enable

Description:

-  This preference allows you specify that if a preceding checkout was an onsite
   checkout, then the 'On-site checkout' checkbox will be ticked
   ready for the next checkout.

.. _onsitecheckouts-label:

OnSiteCheckouts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ the on-site checkouts feature.

Values:

-  Disable

-  Enable

   |image1184|

Description:

-  This preference lets you check out items that are 'not for loan' to
   patrons. A checkbox is added to the checkout screen when this
   preference is set to 'Enable' labeled 'On-site checkout'. This allows
   you to track who's using items that are normally not for loan or are
   in a closed stack setting.

.. _onsitecheckoutsforce-label:

OnSiteCheckoutsForce
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ the on-site for all cases (Even if a user is debarred,
etc.).

Values:

-  Disable

-  Enable

   |image31|

Description:

-  This preference lets the staff override any restrictions a patron
   might have and check out items for use within the library. The
   :ref:`OnSiteCheckouts` preference must first be set
   to 'Enable' for this preference to be considered.

.. _opacfinenorenewalsblockautorenew-label:

OPACFineNoRenewalsBlockAutoRenew
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: If a patron owes more than the value of :ref:`OPACFineNoRenewals`,
\_\_\_ his/her auto renewals.

Values:

-  Allow

-  Block

.. _overduenoticecalendar-label:

OverdueNoticeCalendar
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ when working out the period for overdue notices

Default: Ignore calendar

Values:

-  Ignore calendar

   -  Notices do not take holidays into account, so they will be sent
      even if holidays have meant the item is not actually overdue yet

-  Use calendar

   -  Notices take holidays into account, so they will not be sent if
      holidays mean the item is not actually overdue yet

.. _overduesblockcirc-label:

OverduesBlockCirc
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Ask for confirmation

Asks: \_\_\_ when checking out to a borrower that has overdues
outstanding

Values:

-  Ask for confirmation

   -  Will not let you check an item out to patrons with overdues until
      a librarian confirms that it is okay

-  Block

   -  Block all patrons with overdue items from being able to check out

-  Don't block

   -  Allow all patrons with overdue items to continue to check out

.. _overduesblockrenewing-label:

OverduesBlockRenewing
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: allow renewing

Asks: When a patron's checked out item is overdue, \_\_\_

Values:

-  allow renewing

-  block renewing for all the patron's items

-  block renewing for only this item

.. _printnoticesmaxlines-label:

PrintNoticesMaxLines
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include up to \_\_\_ item lines in a printed overdue notice.

    **Note**

    If the number of items is greater than this number, the notice will
    end with a warning asking the borrower to check their online account
    for a full list of overdue items.

    **Note**

    Set to 0 to include all overdue items in the notice, no matter how
    many there are.

    **Important**

    This preference only refers to the print notices, not those sent via
    email.

.. _renewaccruingiteminopac-label:

RenewAccruingItemInOpac
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: If a patron pays off all fines on an overdue item that is accruing fines 
in the OPAC via a payment plugin, \_\_\_ the item automatically.

Default: Don't renew

Values:

-  Don't renew

-  Renew

Description:

-  This system preference allows you to control whether or not overdue items 
   are renewed if the patron pays the fine online.

     **Note**

     If the :ref:`RenewalPeriodBase` system preference is set to 'due date', 
     renewed items may still be overdue even after renewal.

.. _renewaccruingitemwhenpaid-label:

RenewAccruingItemWhenPaid
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: If a patron pays off all fines on an overdue item that is accruing fines 
\_\_\_  the item automatically.

Default: Don't renew

Values:

-  Don't renew

-  Renew

Description:

-  This system preference allows you to control whether or not overdue items 
   are renewed if the fine is paid in the staff interface.

     **Note**

     If the :ref:`RenewalPeriodBase` system preference is set to 'due date', 
     renewed items may still be overdue even after renewal.

.. _renewalperiodbase-label:

RenewalPeriodBase
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: the old due date of the checkout

Asks: When renewing checkouts, base the new due date on \_\_\_

Values:

-  the old due date of the checkout

-  the current date

.. _renewalsendnotice-label:

RenewalSendNotice
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't send

Asks: \_\_\_\_ a renewal notice according to patron checkout alert
preferences.

Values:

-  Don't send

-  Send

Description:

-  If a patron has chosen to receive a check out notice in their
   messaging preferences and this preference is set to 'Send' then those
   patrons will also receive a notice when they renew materials. You
   will want to set up a :ref:`new notice <adding-notices-and-slips-label>` with the code of
   RENEWAL (if you don't already have it) with custom text for renewing
   items.

       **Important**

       This preference requires that you have
       :ref:`EnhancedMessagingPreferences`
       set to 'Allow'

.. _rentalfeescheckoutconfirmation-label:

RentalFeesCheckoutConfirmation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: do not ask

Asks: When checking out an item with rental fees, \_\_\_ for
confirmation.

Values:

-  ask

  |image1183|

-  do not ask

Description:

-  If you are charging rental fees for items this preference will make
   it so that you can show (or not show) a confirmation before checking
   out an item that will incur a rental charge.

.. _rentalsinnoissuescharge-label:

RentalsInNoissuesCharge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Include

Asks: \_\_\_ rental charges when summing up charges for noissuescharge.

Values:

-  Don't include

-  Include

Description:

-  This preference lets you decide if rental charges are included when
   calculating the :ref:`noissuescharge`. If this is set
   to include then Koha will include all rental charges when deciding if
   the patron owes too much money to check anything else out of the
   library. If it's set to Don't include then Koha will ignore all
   rental charges when figuring out if the patron owes too much money to
   checkout additional materials.

.. _restrictionblockrenewing-label:

RestrictionBlockRenewing
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: If patron is restricted, \_\_\_ renewing of items.

Values:

-  Allow

-  Block

.. _returnbeforeexpiry-label:

ReturnBeforeExpiry
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't require

Asks: \_\_\_ patrons to return books before their accounts expire (by
restricting due dates to before the patron's expiration date).

Values:

-  Don't require

-  Require

Description:

-  This is preference may prevent a patron from having items checked out
   after their library card has expired. If this is set to "Require",
   then a due date of any checked out item can not be set for a date
   which falls after the patron's card expiration. If the setting is
   left "Don't require" then item check out dates may exceed the
   expiration date for the patron's library card.

.. _staffsearchresultsdisplaybranch-label:

StaffSearchResultsDisplayBranch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: the library the item is held by

Asks: For search results in the staff client, display the branch of
\_\_\_

Values:

-  the library the item is from

-  the library the items is held by

.. _switchonsitecheckouts-label:

SwitchOnSiteCheckouts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't switch

Asks: \_\_\_ on-site checkouts to normal checkouts when checked out.

Values:

-  Don't switch

-  Switch

.. _transfersmaxdayswarning-label:

TransfersMaxDaysWarning
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 3

Asks: Show a warning on the "Transfers to Receive" screen if the
transfer has not been received \_\_\_ days after it is sent.

Description:

-  The TransferMaxDaysWarning preference is set at a default number of
   days. This preference allows for a warning to appear after a set
   amount of time if an item being transferred between library branches
   has not been received. The warning will appear in the :ref:`Transfers to
   Receive <transfers-to-receive-label>` report.

.. _usebranchtransferlimits-and-branchtransferlimitstype-label:

UseBranchTransferLimits and BranchTransferLimitsType
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Defaults: Don't enforce and collection code

Asks: \_\_\_ branch transfer limits based on \_\_\_

UseBranchTransferLimits Values:

-  Don't enforce

-  Enforce

BranchTransferLimitsType Values:

-  collection code

-  item type

BranchTransferLimitsType Description:

-  This parameter is a binary setting which determines whether items are
   transferred according to item type or collection code. This value
   determines how the library manager is able to restrict what items can
   be transferred between the branches.

.. _usedaysmode-label:

useDaysMode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ when calculating the date due.

Default: Use the calendar to skip days the library is closed

Values:

-  Use the calendar to skip days the library is closed

-  Use the calendar to push the due date to the next open day

-  Ignore the calendar

-  Use the calendar to push the due date to the next open matching weekday
   for weekly loan periods, or the next open day otherwise (Note: This preference
   setting only works with loan periods in multiples of 7).

Description:

-  This preference controls how scheduled library closures affect the
   due date of a material.

-  The 'Use the calendar to skip all days the library is closed' setting allows 
   for a scheduled closure not to count as a day in the loan period. 

-  The 'Ignore the calendar' setting would not consider the scheduled closure 
   at all

-  The 'Use the calendar to push the due date to the next open day' would only 
   affect the due date if the day the item is due would fall specifically on
   the day of closure.

-  The final option, 'Use the calendar to push the due date to the next open 
   matching weekday for weekly loan periods, or the next open day otherwise' 
   allows libraries to accommodate patrons who may only be able to visit the 
   library on a certain day of the week, such as part-time students or patrons 
   who rely on public transport.

Example:

-  The library has put December 24th and 25th in as closures on the
   calendar. A book checked out by a patron has a due date of December
   25th according to the circulation and fine rules.

   -  If this preference is set to 'Ignore the calendar' then the item will 
      remain due on the 25th.

   -  If the preference is set to 'Use the calendar to push the due date to the 
      next open day', then the due date will be December 26th.

   -  If the preference is set to 'Usethe calendar to skip all days the library 
      is closed' then the due date will be pushed to the 27th of December to 
      accommodate for the two closed days.

   -  If the preference is set to 'Use the calendar to push the due date to the 
      next open matching weekday for weekly loan periods, or the next open day 
      otherwise' the item would be due back on January 1st. If January 1st was 
      also a closed day then the item would be due back on the next available 
      open day.

The calendar is defined on a branch by branch basis. To learn more about
the calendar, check out the :ref:`Calendar<calendar-label>`
section of this manual.

.. _usetransportcostmatrix-label:

UseTransportCostMatrix
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't use

Asks: \_\_\_ Transport Cost Matrix for calculating optimal holds filling
between branches.

Values:

-  Don't use

-  Use

Description:

-  If the system is configured to use the :ref:`Transport cost
   matrix <transport-cost-matrix-label>` for filling holds, then when
   attempting to fill a hold, the system will search for the lowest cost
   branch, and attempt to fill the hold with an item from that branch
   first. Branches of equal cost will be selected from randomly. The
   branch or branches of the next highest cost shall be selected from
   only if all the branches in the previous group are unable to fill the
   hold.

   The system will use the item's current holding branch when
   determining whether the item can fulfill a hold using the Transport
   Cost Matrix.

.. _course-reserves-system-preferences-label:

Course Reserves
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _usecoursereserves-label:

UseCourseReserves
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't use

Asks: \_\_\_ course reserves

Values:

-  Don't use

-  Use

Description:

-  The `Course Reserves <#coursereserves>`__ module in Koha allows you
   to temporarily move items to 'reserve' and assign different
   circulation rules to these items while they are being used for a
   specific course.

.. _fines-policy-label:

Fines Policy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _finescalendar-label:

finesCalendar
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ when calculating the period for fines.

Default: Use the calendar

Values:

-  Ignore the calendar

-  Use the calendar

Description:

-  This preference will determine whether or not fines will be accrued
   on days where the library is closed. Examples include holidays, library 
   in-service days, etc. 

-  If set to 'Use the calendar', Koha will skip closed days when calculating 
   the overdue fines.

-  If set to 'Ignore the calendar', fines will be calculated directly, with 
   no consideration of closed days.

  **Important**

  To make use of this setting your system administrator must first access 
  Koha's :ref:calendar<calendar-label>` and mark closed days as 'holidays'
  ahead of time.

The calendar is defined on a branch by branch basis. To learn more about
the calendar, check out the :ref:`calendar <calendar-label>`
section of this manual.

.. _finesincludegraceperiod-label:

FinesIncludeGracePeriod
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Include

Asks: \_\_\_ the grace period when calculating the fine for an overdue
item.

Values:

-  Don't include

-  Include

Description:

-  This preference lets you control how Koha calculates fines when there
   is a grace period. If you choose to include the grace period when
   calculating fines then Koha will charge for the days in the grace
   period should the item be overdue more than those days. If you choose
   not to include the grace period then Koha will only charge for the
   days overdue after the grace period.

.. _finesmode-label:

finesMode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Asks: \_\_\_ fines

Default: Don't calculate

Values:

-  Don't calculate

-  Calculate and charge

    **Important**

    If this system preference is set to 'Calculate and charge', you must either 
    add the :ref:`fines cron job <cron-fines-label>` to your crontab, or enable 
    :ref:`CalculateFinesOnReturn`

    If the cronjobs/fines.pl cronjob is being run, accruing and final fines will 
    be calculated when the cron runs and accruing fines will be finalized when 
    an item is returned. If CalculateFinesOnReturn is enabled, final fines will 
    be calculated when an item is returned.     

.. _holdfeemode-label:

HoldFeeMode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: only if all items are checked out and the record has at least one hold already.

Asks: Charge a hold fee \_\_\_

Values:

-  any time a hold is collected.

-  any time a hold is placed.

-  only if all items are checked out and the record has at least one hold already.

.. _norefundonlostreturneditemsage-label:

NoRefundOnLostReturnedItemsAge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Don't refund lost fees if a lost item is checked in more than \_\_\_ days 
after it was marked lost. 

Description:

-  Enter a number of days after which lost items are not refunded.

**Note**

Set the refund policy in the :ref:`default lost item fee refund on return policy <item-fee-refund-on-return-label>` 
rule in the :ref:`circulation and fines rules <circulation-and-fines-rules-label>`.

.. _processingfeenote-label:

ProcessingFeeNote
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Set the text to be recorded in the column 'note', table 'accountlines' when the processing fee (defined in item type) is applied.

.. _refundlostonreturncontrol-label:

RefundLostOnReturnControl
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: If a lost item is returned, apply the refunding rules defined
in the \_\_\_

Default: check-in library.

Values:

-  check-in library.

-  item holding branch.

-  item home branch.

Description:

-  This refers to the :ref:`default lost item fee refund on return policy <item-fee-refund-on-return-label>` 
   rule in the :ref:`circulation and fines rules <circulation-and-fines-rules-label>`.

**Note** 

You can limit the number of days after which a lost item is not refunded using 
the :ref:`NoRefundOnLostReturnedItemsAge` system preference.

.. _suspensionscalendar-label:

SuspensionsCalendar
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: not including the days the library is closed

Asks: Calculate suspension expiration based on days overdue \_\_\_

Values:

-  Ignore the calendar

-  Use the calendar

Description:

-  This system preference determines whether the :ref:`calendar <calendar-label>` is taken into
   account when making suspension calculations.  Suspension rules can be
   configured within the :ref:`circulation rules <circulation-and-fines-rules-label>`.
   If set to ‘directly’ the suspension period will ignore any closed days
   that have been added to the calendar.  If set to ‘not including the
   days the library is closed’ any days marked as closed within the calendar
   will be skipped when calculating the end date for the suspension.

.. _usedefaultreplacementcost-label:

useDefaultReplacementCost
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't use

Asks: \_\_\_ the default replacement cost defined in item type.

Values:

-  Don't use

-  Use

Description:

-  This preference enables the use of the replacement cost set on the item type level

.. _whenlostchargereplacementfee-label:

WhenLostChargeReplacementFee
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Charge

Asks: \_\_\_ the replacement price when a patron loses an item.

Values:

-  Charge

-  Don't charge

Description:

-  This preference lets you tell Koha what to do with an item is marked
   lost. If you want Koha can 'Charge' the patron the replacement fee
   listed on the item they lost or it can do nothing in reference to the
   patron and just mark the item lost in the catalog.

.. _whenlostforgivefine-label:

WhenLostForgiveFine
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't forgive

Asks: \_\_\_ the fines on an item when it is lost.

Values:

-  Don't forgive

-  Forgive

Description:

-  This preference allows the library to decide if fines are charged in
   addition to the replacement fee when an item is marked as lost. If
   this preference is set to 'Forgive' then the patron won't be charged
   fines in addition to the replacement fee.

.. _holds-policy-label:

Holds Policy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _allowholddateinfuture-label:

AllowHoldDateInFuture
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ hold requests to be placed that do not enter the waiting
list until a certain future date.

Values:

-  Allow

-  Don't allow

.. _allowholditemtypeselection-label:

AllowHoldItemTypeSelection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ hold fulfillment to be limited by itemtype.

Values:

-  Allow

-  Don't allow

.. _allowholdpolicyoverride-label:

AllowHoldPolicyOverride
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ staff to override hold policies when placing holds.

Values:

-  Allow

-  Don't allow

Description:

-  This preference is a binary setting which controls whether or not the
   library staff can override the circulation and fines rules as they
   pertain to the placement of holds. Setting this value to "Don't
   allow" will prevent anyone from overriding, setting it to "Allow"
   will allow it. This setting is important because it determines how
   strict the libraries rules for placing holds are. If this is set to
   "Allow", exceptions can be made for patrons who are otherwise
   normally in good standing with the library, but there is opportunity
   for the staff to abuse this function. If it is set to "Don't allow",
   no abuse of the system is possible, but it makes the system entirely
   inflexible in respect to holds.

.. _allowholdsondamageditems-label:

AllowHoldsOnDamagedItems
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ hold requests to be placed on damaged items.

Values:

-  Allow

-  Don't allow

Description:

-  This parameter is a binary setting which controls whether or not hold
   requests can be placed on items that are marked as "damaged" (items
   are marked as damaged by editing subfield 4 on the item record).
   Setting this value to "Don't allow" will prevent anyone from placing
   a hold on such items, setting it to "Allow" will allow it. This
   preference is important because it determines whether or not a patron
   can place a request for an item that might be in the process of being
   repaired or not in good condition. The library may wish to set this
   to "Don't allow" if they were concerned about their patrons not
   receiving the item in a timely manner or at all (if it is determined
   that the item is beyond repair). Setting it to "Allow" would allow a
   patron to place a hold on an item and therefore receive it as soon as
   it becomes available.

.. _allowholdsonpatronspossessions-label:

AllowHoldsOnPatronsPossessions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_\_ a patron to place a hold on a record where the patron
already has one or more items attached to that record checked out.

Values:

-  Allow

-  Don't allow

Description:

-  By setting to "Don't allow," you can prevent patrons from placing
   holds on items they already have out, thus preventing them from
   blocking anyone else from getting an item.

.. _allowrenewalifotheritemsavailable-label:

AllowRenewalIfOtherItemsAvailable
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ a patron to renew an item with unfilled holds if other
available items can fill that hold.

Values:

-  Allow

-  Don't allow

.. _autoresumesuspendedholds-label:

AutoResumeSuspendedHolds
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ suspended holds to be automatically resumed by a set date.

Values:

-  Allow

-  Don't allow

Description:

-  If this preference is set to 'Allow' then all suspended holds will be
   able to have a date at after which they automatically become
   unsuspended. If you have this preference set to 'Allow' you will also
   need the :ref:`Unsuspend Holds` cron job running.

    **Important**

    The holds will become unsuspended the date after that entered by the
    patron.

.. _canmarkholdstopullaslost-label:

CanMarkHoldsToPullAsLost
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ from the 'Holds to pull' screen

Default: Do not allow to mark items as lost

Values:

-  Allow to mark items as lost

-  Allow to mark items as lost and notify the patron

-  Do not allow to mark items as lot

Description:

-  This preference lets you choose whether the staff can mark items
   as lost directly from the 'Holds to pull' list if they can't
   find the item on the shelf.

-  The actual lost value that will be assigned to the item is defined in the 
   :ref:`UpdateItemWhenLostFromHoldList` system preference.

.. _canreservefromotherbranches-label:

canreservefromotherbranches
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ a user from one library to place a hold on an item from
another library

Description:

-  This preference is a binary setting which determines whether patrons
   can place holds on items from other branches. If the preference is
   set to "Allow" patrons can place such holds, if it is set to "Don't
   allow" they cannot. This is an important setting because it
   determines if users can use Koha to request items from another
   branch. If the library is sharing an installation of Koha with other
   independent libraries which do not wish to allow interlibrary
   borrowing it is recommended that this parameter be set to "Don't
   allow".

Values:

-  Allow

-  Don't allow (with :ref:`IndependentBranches`)

.. _confirmfutureholds-label:

ConfirmFutureHolds
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 0

Asks: Confirm future hold requests (starting no later than \_\_\_ days
from now) at checkin time.

Description:

-  When confirming a hold at checkin time, the number of days in this
   preference is taken into account when deciding which holds to show
   alerts for. This preference does not interfere with renewing,
   checking out or transferring a book.

    **Note**

    This number of days will be used too in calculating the default end
    date for the Holds to pull-report. But it does not interfere with
    issuing, renewing or transferring books.

    **Important**

    This preference is only looked at if you're allowing hold dates in
    the future with :ref:`AllowHoldDateInFuture`
    or :ref:`OPACAllowHoldDateInFuture`

.. _decreaseloanhighholds-preferences-label:

decreaseLoanHighHolds, decreaseLoanHighHoldsDuration, decreaseLoanHighHoldsValue, decreaseLoanHighHoldsControl, and decreaseLoanHighHoldsIgnoreStatuses
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the reduction of loan period \_\_\_ to days for items with
more than \_\_\_ holds \_\_\_ . Ignore items with the following statuses
when counting items \_\_\_

decreaseLoanHighHolds default: Don't enable

decreaseLoanHighHoldsControl default: on the record

decreaseLoanHighHolds values:

-  Enable

decreaseLoanHighHoldsControl values:

-  over the number of holdable items on the records

-  on the record

decreaseLoanHighHoldsIgnoreStatuses values:

-  [Select All]

-  Damages

-  Lost

-  Not for loan

-  Withdrawn

Description:

-  These preferences let you change the loan length for items that have
   many holds on them. This will not effect items that are already
   checked out, but items that are checked out after the
   decreaseLoanHighHoldsValue is met will only be checked out for the
   number of days entered in the decreaseLoanHighHoldsDuration
   preference.

   |image32|

.. _displaymultiplacehold-label:

DisplayMultiPlaceHold
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ the ability to place holds on multiple biblio from the
search results

Values:

-  Don't enable

-  Enable

.. _emaillibrarianwhenholdisplaced-label:

emailLibrarianWhenHoldIsPlaced
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ sending an email to the Koha administrator email address
whenever a hold request is placed.

Values:

-  Don't enable

-  Enable

Description:

-  This preference enables Koha to email the library staff whenever a
   patron requests an item to be held. While this function will
   immediately alert the librarian to the patron's need, it is extremely
   impractical in most library settings. In most libraries the hold
   lists are monitored and maintained from a separate interface. That
   said, many libraries that allow on shelf holds prefer to have this
   preference turned on so that they are alerted to pull an item from
   the shelf.

    **Important**

    In order for this email to send you must have a
    :ref:`notice <notices-and-slips-label>` template with the code of HOLDPLACED

    **Important**

    This notice will only be sent if the :ref:`process\_message\_queue.pl
    cron job <cron-message-queue-label>` is being run periodically to send the
    messages.

.. _excludeholidaysfrommaxpickupdelay-label:

ExcludeHolidaysFromMaxPickUpDelay
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ when calculating the period for reserves max pickup delay.

Default: Ignore the calendar

Values:

-  Ignore the calendar

-  Use the calendar

Description:

-  This system preference determines whether or not closed days in the 
   :ref:`calendar<calendar-label>` are taken into account when calculating the 
   time period for patrons to pick up their holds (see 
   :ref:`ReservesMaxPickUpDelay`).

-  If set to 'Ignore the calendar', the pickup delay will be calculated 
   directly.

-  If set to 'Use the calendar', holidays will be excluded from the pickup 
   delay.

.. _expirereservesmaxpickupdelay-label:

ExpireReservesMaxPickUpDelay
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ holds to expire automatically if they have not been picked
by within the time period specified in
:ref:`ReservesMaxPickUpDelay`

Values:

-  Allow

-  Don't allow

Description:

-  If set to 'allow' this will cancel holds that have been waiting for
   longer than the number of days specified in the
   :ref:`ReservesMaxPickUpDelay` system
   preference. Holds will only be cancelled if the :ref:`Expire Holds cron
   job <cron-expired-holds-label>` is runnning.

.. _expirereservesmaxpickupdelaycharge-label:

ExpireReservesMaxPickUpDelayCharge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 0

Asks: If using
:ref:`ExpireReservesMaxPickUpDelay`, charge
a borrower who allows his or her waiting hold to expire a fee of \_\_\_
USD

Description:

-  If you are expiring holds that have been waiting too long you can use
   this preference to charge the patron for not picking up their hold.
   If you don't charge patrons for items that aren't picked up you can
   leave this set to the default which is 0. Holds will only be
   cancelled and charged if the :ref:`Expire Holds cron
   job <cron-expired-holds-label>` is running.

.. _expirereservesonholidays-label:

ExpireReservesOnHolidays
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ expired holds to be cancelled on days the library is
closed.

Values:

-  Allow

-  Don't allow

.. _holdssplitqueue-label:

HoldsSplitQueue
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: nothing

Asks: In the staff client, split the holds queue into separate tables by \_\_\_

Values:

-  pickup library

-  pickup library and itemtype

-  hold itemtype

-  nothing

Description:

-  This feature allows you to separate holds by pickup library or itemtype in the
   holds page of a record (not in the global holds queue found on the circulation
   page).

-  When using the up and down arrows the priorities will be changed only
   in the group the holds belongs to.

.. _holdssplitqueuenumbering-label:

HoldsSplitQueueNumbering
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: the actual priority, which may be out of order

Asks: If the holds queue is split, show librarians \_\_\_

Values:

-  the actual priority, which may be out of order

-  'virtual' priorities, where each group is numbered separately

Description:

-  This system preference is only effective if :ref:`HoldsSplitQueue` is set to
   any value except 'nothing'.

-  This system preference controls the priority numbering on the holds page
   of a record (not in the global holds queue found on the circulation page).

.. _localholdspriority-preferences-label:

LocalHoldsPriority, LocalHoldsPriorityPatronControl, LocalHoldsPriorityItemControl
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ priority for filling holds to patrons whose \_\_\_ matches
the item's \_\_\_

LocalHoldsPriority Values:

-  Don't give

-  Give

LocalHoldsPriorityPatronControl Values:

-  home library

-  pickup library

LocalHoldsPriorityItemControl Values:

-  holding library

-  home library

Description:

-  This feature will allow libraries to specify that, when an item is
   returned, a local hold may be given priority for fulfillment even
   though it is of lower priority in the list of unfilled holds.

.. _maxreserves-label:

maxreserves
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 50

Asks: Patrons can only have \_\_\_ holds at once.

.. _opacallowholddateinfuture-label:

OPACAllowHoldDateInFuture
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ patrons to place holds that don't enter the waiting list
until a certain future date.

Values:

-  Allow

   -  :ref:`AllowHoldDateInFuture` must also be
      enabled for this to work

-  Don't allow

.. _opacallowusertochoosebranch-label:

OPACAllowUserToChooseBranch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ a user to choose the library to pick up a hold from.

Values:

-  Allow

-  Don't allow

Description:

-  Changing this preference will not prevent staff from being able to
   transfer titles from one library to another to fill a hold, it will
   only prevent patrons from saying they plan on picking a book up at a
   library other than their home library.

-  The list of available pickup locations will include all libraries that
   have 'Pickup location' set to 'Yes' on the library configuration page.

.. _opacholdsifavailableatpickup-label:

OPACHoldsIfAvailableAtPickup
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ to pickup holds at libraries where the item is available.

Values:

-  Don't allow

-  Allow

Description:

-  Prevents borrowers from requesting items that are on the shelf
   at the same branch at which they wish to pick up those items.

.. _opacholdsifavailableatpickupexceptions-label:

OPACHoldsIfAvailableAtPickupExceptions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: blank

Asks: Patron categories not affected by :ref:`OPACHoldsIfAvailableAtPickup`
\_\_\_ (list of patron categories separated with a pipe ^|^)

Description:

-  Patron category codes listed here separated by a pipe ^|^ are unaffected by
   :ref:`OPACHoldsIfAvailableAtPickup`.

.. _reservescontrolbranch-label:

ReservesControlBranch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: item's home library

Asks: Check the \_\_\_ to see if the patron can place a hold on the
item.

Values:

-  item's home library.

-  patron's home library.

.. _reservesmaxpickupdelay-label:

ReservesMaxPickUpDelay
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 7

Asks: Mark a hold as problematic if it has been waiting for more than
\_\_\_ days.

Description:

-  This preference (based on calendar days, not the
   :ref:`Koha holiday calendar <calendar-label>`) puts an expiration date on an item a
   patron has on hold. After this expiration date the staff will have
   the option to release the unclaimed hold which then may be returned
   to the library shelf or issued to the next patron on the item's hold
   list. Items that are 'expired' by this preference are moved to the
   'Holds Over' tab on the :ref:`Holds Awaiting Pickup <holds-awaiting-pickup-label>`
   report.

.. _reservesneedreturns-label:

ReservesNeedReturns
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't automatically

Asks: \_\_\_ mark holds as found and waiting when a hold is placed
specifically on them and they are already checked in.

Values:

-  Automatically

-  Don't automatically

Description:

-  This preference refers to 'item specific' holds where the item is
   currently on the library shelf. This preference allows a library to
   decide whether an 'item specific' hold is marked as "Waiting" at the
   time the hold is placed or if the item will be marked as "Waiting"
   after the item is checked in. This preference will tell the patron
   that their item is 'Waiting' for them at their library and ready for
   check out.

.. _holds-queue-system-preferences-label:

StaticHoldsQueueWeight, HoldsQueueSkipClosed and RandomizeHoldsQueueWeight
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

StaticHoldsQueueWeight Default: 0

HoldsQueueSkipClosed Default: open or closed

RandomizeHoldsQueueWeight Default: in that order

Asks: Satisfy holds using items from the libraries \_\_\_ (as
branchcodes, separated by commas; if empty, uses all libraries) when
they are \_\_\_ \_\_\_.

HoldsQueueSkipClosed Values:

-  open or closed

-  open

RandomizeHoldsQueueWeight Values:

-  in random order

   -  If StaticHoldsQueueWeight is left at the default Koha will
      randomize all libraries, otherwise it will randomize the libraries
      listed.

-  in that order

   -  If StaticHoldsQueueWeight is left at the default then this will
      use all of your branches in alphabetical order, otherwise it will
      use the branches in the order that you entered them in the
      StaticHoldsQueueWeight preference.

Descriptions:

-  These preferences control how the :ref:`Holds Queue
   report <holds-queue-label>` is generated using :ref:`a cron
   job <cron-holds-queue-report-label>`.

   If you do not want all of your libraries to participate in the
   on-shelf holds fulfillment process, you should list the the libraries
   that \*do\* participate in the process here by inputting all the
   participating library's branchcodes, separated by commas ( e.g.
   "MPL,CPL,SPL,BML" etc. ).

   By default, the holds queue will be generated such that the system
   will first attempt to hold fulfillment using items already at the
   pickup library if possible. If there are no items available at the
   pickup library to fill a hold, build\_holds\_queue.pl will then use
   the list of libraries defined in StaticHoldsQueueWeight. If
   RandomizeHoldsQueueWeight is disabled ( which it is by default ), the
   script will assign fulfillment requests in the order the branches are
   placed in the StaticHoldsQueueWeight system preference.

   For example, if your system has three libraries, of varying sizes (
   small, medium and large ) and you want the burden of holds
   fulfillment to be on larger libraries before smaller libraries, you
   would want StaticHoldsQueueWeight to look something like
   "LRG,MED,SML".

   If you want the burden of holds fulfillment to be spread out equally
   throughout your library system, simply enable
   RandomizeHoldsQueueWeight. When this system preference is enabled,
   the order in which libraries will be requested to fulfill an on-shelf
   hold will be randomized each time the list is regenerated.

    **Important**

    The :ref:`Transport Cost Matrix <transport-cost-matrix-label>` takes
    precedence in controlling where holds are filled from, if the matrix
    is not used then Koha checks the StaticHoldsQueueWeight. To use the
    Transport Cost Matrix simply set your
    :ref:`UseTransportCostMatrix` preference to
    'Use'

.. _suspendholdsintranet-label:

SuspendHoldsIntranet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ holds to be suspended from the intranet.

Values:

-  Allow

-  Don't allow

Description:

-  The holds suspension feature can be turned on and off in the staff
   client by altering this system preference. If this is set to 'allow'
   you will want to set the
   :ref:`AutoResumeSuspendedHolds` system
   preference.

.. _suspendholdsopac-label:

SuspendHoldsOpac
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ holds to be suspended from the OPAC.

Values:

-  Allow

-  Don't allow

Description:

-  The holds suspension feature can be turned on and off in the OPAC by
   altering this system preference. If this is set to 'allow' you will
   want to set the
   :ref:`AutoResumeSuspendedHolds` system
   preference.

.. _transferwhencancelallwaitingholds-label:

TransferWhenCancelAllWaitingHolds
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't transfer

Asks: \_\_\_ items when cancelling all waiting holds.

Values:

-  Don't transfer

-  Transfer

Description:

-  When TransferWhenCancelAllWaitingHolds is set to "Don't transfer", no
   branch transfer records are created. Koha will not allow the holds to
   be transferred, because that would orphan the items at the library
   where the holds were awaiting pickup, without any further instruction
   to staff as to what items are at the library or where they need to
   go. When that system preference set to "Transfer", branch transfers
   are created, so the holds may be cancelled.

.. _updateitemwhenlostfromholdlist-label:

UpdateItemWhenLostFromHoldList
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Update item's values when marked as lost from the hold to pull screen.

Description:

-  This is a list of values to update an item when it is marked as lost from
   the holds to pull screen. For example, write "itemlost: 1" to set the items.
   itemlost value to 1 when the item is marked as lost. This will use the authorized
   value 1 from the :ref:`LOST authorized value list<existing-values-label>`.

-  Examples of keywords:

   -  itemlost: lost status, uses the 
      :ref:`LOST authorized values list<existing-values-label>`

   -  notforloan: not for loan status, uses the 
      :ref:`NOT_LOAN authorized values list<existing-values-label>`

   -  withdrawn: withdrawn status, uses the 
      :ref:`WITHDRAWN authorized values list<existing-values-label>`

   -  damaged: damaged status, uses the 
      :ref:`DAMAGED authorized values list<existing-values-label>`

   -  location: location code, uses the 
      :ref:`LOC authorized values list<existing-values-label>`

   -  ccode: collection code, uses the 
      :ref:`CCODE authorized values list<existing-values-label>`

-  This preference requires that the :ref:`CanMarkHoldsToPullAsLost` system
   preference be set to either 'Allow' option


.. Warning ::

   Requires YAML syntax to work

   This means

   -  Make sure there is NO space between the field name and the colon

   -  Make sure there IS a space between the colon and the value

   -  Make sure each pair is on its own line

.. _housebound-module-label:

Housebound module
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _houseboundmodule-label:

HouseboundModule
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ housebound module

Values:

-  Disable

-  Enable

Description:

-  This preference enables or disables the Housebound module which
   handles management of circulation to Housebound readers.

.. _housebound-interface-label:

Interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _allowallmessagedeletion-label:

AllowAllMessageDeletion
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ staff to delete messages added from other libraries.

Values:

-  Allow

-  Don't allow

.. _allowcheckoutnotes-label:

AllowCheckoutNotes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ patrons to submit notes about checked out items.

Values:

-  Don't allow

-  Allow

This preference if set to allow will give your patrons the option to add
a note to an item they have checked out on the OPAC side.  This note will be
seen on the staff side when the item is checked in.

.. _allowofflinecirculation-label:

AllowOfflineCirculation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Do not enable

Asks: \_\_\_ offline circulation on regular circulation computers.

Values:

-  Do not enable

-  Enable

Description:

-  Setting this preference to 'Enable' allows you to use the Koha
   interface for :ref:`offline circulation <offline-circulation-utilities-label>`. This system
   preference does not affect the :ref:`Firefox
   plugin <firefox-plugin-label>` or the :ref:`desktop
   application <offline-circ-tool-for-windows-label>`, any of these three options can
   be used for offline circulation without effecting the other.

.. _autoswitchpatron-label:

AutoSwitchPatron
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ the automatic redirection to another patron when a patron
barcode is scanned instead of a book. This should not be enabled if you
have overlapping patron and book barcodes.

Values:

-  Don't enable

-  Enable

Description:

-  Enabling this system preference allows staff to scan a patron barcode instead
   of an item barcode in the checkout box to switch patron records.

.. _circautoprintquickslip-label:

CircAutoPrintQuickSlip
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: open a print quick slip window

Asks: When an empty barcode field is submitted in circulation \_\_\_

Values:

-  clear the screen

-  open a print quick slip window

-  open a print slip window

Description:

-  If this preference is set to open a quick slip
   (:ref:`ISSUEQSLIP <existing-notices-and-slips-label>`) or open a slip
   (:ref:`ISSUESLIP <existing-notices-and-slips-label>`) for printing it will eliminate the
   need for the librarian to click the print button to generate a
   checkout receipt for the patron they're checking out to. If the
   preference is set to clear the screen then "checking out" an empty
   barcode will clear the screen of the patron you were last working
   with.

.. _circsidebar-label:

CircSidebar
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Deactivate

Asks: \_\_\_ the navigation sidebar on all Circulation pages.

Values:

-  Deactivate

-  Activate

.. _displayclearscreenbutton-label:

DisplayClearScreenButton
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Show

Asks: \_\_\_ a button to clear the current patron from the screen on the
circulation screen.

Values:

-  Don't show

   |image36|

-  Show

   |image37|

.. _exportcirchistory-label:

ExportCircHistory
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't show

Asks: \_\_\_ the export patron checkout history options.

Values:

-  Don't show

-  Show

.. _exportremovefields-label:

ExportRemoveFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: The following fields should be excluded from the patron checkout
history CSV or iso2709 export \_\_\_

Description:

-  This space separated list of fields (e.g. 100a 245b) will
   automatically be excluded when exporting the patron's current
   checkout history.

   |image38|

.. _filterbeforeoverduereport-label:

FilterBeforeOverdueReport
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't require

Asks: \_\_\_ staff to choose which checkouts to show before running the
overdues report.

Description:

-  Koha's overdue report shows you all of the overdue items in your
   library system. If you have a large library system you'll want to set
   this preference to 'Require' to force those running the report to
   first limit the data generated to a branch, date range, patron
   category or other such filter. Requiring that the report be filtered
   before it's run prevents your staff from running a system heavy
   report and slowing down other operations in the system.

   |image34|

Values:

-  Don't require

-  Require

.. _finenotifyatcheckin-label:

FineNotifyAtCheckin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't notify

Asks: \_\_\_ librarians of overdue fines on the items they are checking
in.

Values:

-  Don't notify

-  Notify

Description:

-  With this preference set to 'Notify' all books that have overdue
   fines owed on them will pop up a warning when checking them in. This
   warning will need to acknowledged before you can continue checking
   items in. With this preference set to 'Don't notify,^ you will still
   see fines owed on the patron record, you just won't have an
   additional notification at check in.

   |image35|

.. _holdstopullstartdate-label:

HoldsToPullStartDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 2

Asks: Set the default start date for the Holds to pull list to \_\_\_
day(s) ago.

Description:

-  The :ref:`Holds to Pull <holds-to-pull-label>` report in circulation defaults to
   filtering holds placed 2 days ago. This preference allows you to set
   this default filter to any number of days.

.. _itembarcodefallbacksearch-label:

itemBarcodeFallbackSearch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ the automatic use of a keyword catalog search if the phrase
entered as a barcode on the checkout page does not turn up any results
during an item barcode search.

Values:

-  Don't enable

-  Enable

   |image40|

Description:

-  Sometimes libraries want to checkout using something other than the
   barcode. Enabling this preference will do a keyword search of Koha to
   find the item you're trying to check out. You can use the call
   number, barcode, part of the title or anything you'd enter in the
   keyword search when this preference is enabled and Koha will ask you
   which item you're trying to check out.

    **Important**

    While you're not searching by barcode a barcode is required on every
    title you check out. Only titles with barcodes will appear in the
    search results.

.. _itembarcodeinputfilter-label:

itemBarcodeInputFilter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't filter

Asks: \_\_\_ scanned item barcodes.

Values:

-  Convert from CueCat format

-  Convert from Libsuite8 form

-  Don't filter

-  EAN-13 or zero-padded UPC-A from

-  Remove spaces from

-  Remove the first number from T-prefix style

   -  This format is common among those libraries migrating from Follett
      systems

.. _noticecss-label:

NoticeCSS
^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the stylesheet at \_\_\_ on Notices.

    **Important**

    This should be a complete URL, starting with http://

Description:

-  If you would like to style your notices with a consistent set of
   fonts and colors you can use this preference to point Koha to a
   stylesheet specifically for your notices.

.. _numreturneditemstoshow-label:

numReturnedItemsToShow
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 20

Asks : Show the \_\_\_ last returned items on the checkin screen.

.. _patronautocomplete-label:

PatronAutoComplete
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ to guess the patron being entered while typing a patron search 
for circulation or patron search. Only returns the first 10 results at a time.

Default: Try

Values:

-  Try

-  Don't try

Description:

-  This system preference enables the auto-complete feature in the 
   :ref:`patron search <patron-search-label>` in the Patrons and Circulation 
   modules.

-  Setting it to "Try" would enable a staff member to begin typing a name or 
   other value into the field and have a menu pop up with suggestions for 
   completing it. Setting it to "Don't try" would disable this feature. 

-  This preference can make staff members' jobs easier or it could potentially 
   slow down the page loading process.

   |image33|

.. _previousissuesdefaultsortorder-label:

previousIssuesDefaultSortOrder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Sort previous checkouts on the circulation page from \_\_\_ due
date.

Default: earliest to latest

Values:

-  earliest to latest

-  latest to earliest

Description:

-  This system preference controls how you want the previous checkouts to appear 
   in the patron's :ref:`Checkout tab. <checking-items-out-label>`

-  If you choose 'earliest to latest', the oldest checkout will be at the top.

-  If you choose 'latest to earliest', the most recent checkout will be at the 
   top.

.. _recordlocaluseonreturn-label:

RecordLocalUseOnReturn
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't record

Asks: \_\_\_ local use when an unissued item is checked in.

Values:

-  Don't record

-  Record

Description:

-  When this preference is set to "Don't record" you can record local
   use of items by checking items out to the statistical patron. With
   this preference set to "Record" you can record local use by checking
   out to the statistical patron and/or by checking in a book that is
   not currently checked out.

.. _showallcheckins-label:

ShowAllCheckins
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Do not show

Asks: \_\_\_ all items in the "Checked-in items" list, even items that
were not checked out.

Values:

-  Do not show

-  Show

Description:

-  When items that are not currently checked out are checked in they
   don't show on the list of checked in items. This preference allows
   you to choose how you'd like the log of checked in items displays.

.. _specifyduedate-label:

SpecifyDueDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Allow

Asks: \_\_\_ staff to specify a due date for a checkout.

Due dates are calculated using your circulation and fines rules, but
staff can override that if you allow them to specify a due date at
checkout.

Description:

-  This preference allows for circulation staff to change a due date
   from the automatic due date to another calendar date. This option
   would be used for circumstances in which the due date may need to be
   decreased or extended in a specific circumstance. The "Allow" setting
   would allow for this option to be utilized by staff, the "Don't
   allow" setting would bar staff from changing the due date on
   materials.

Values:

-  Allow

   |image41|

-  Don't allow

   |image42|

.. _specifyreturndate-label:

SpecifyReturnDate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't allow

Asks: \_\_\_ staff to specify a return date for a check in.

Values:

-  Allow

  |image1185|

-  Don't allow

  |image1186|

Description:

-  This preference lets you decide if staff can specify an arbitrary
   return date when checking in items. If an arbitrary return date is
   specified then fines are recalculated accordingly.

.. _todaysissuesdefaultsortorder-label:

todaysIssuesDefaultSortOrder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Sort today's checkouts on the circulation page from \_\_\_ due
date.

Default: latest to earliest

Values:

-  earliest to latest

-  latest to earliest

Description:

-  This system preference controls how you want today's checkouts to appear 
   in the patron's :ref:`Checkout tab. <checking-items-out-label>`

-  If you choose 'earliest to latest', the oldest checkout will be at the top.

-  If you choose 'latest to earliest', the most recent checkout will be at the 
   top.

.. _updatetotalissuesoncirc-label:

UpdateTotalIssuesOnCirc
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Do not

Asks: \_\_\_ update a bibliographic record's total issues count whenever
an item is issued

Values:

-  Do

       **Important**

       This increases server load significantly; if performance is a
       concern, use the :ref:`cron job <cron-track-total-checkouts-label>` to update the total issues count instead.

-  Do not

Description:

-  Koha can track the number of times and item is checked out and store
   that on the item record in the database. This information is not
   stored by default. Setting this preference to 'Do' will tell Koha to
   track that info everytime the item is checked out in real time.
   Otherwise you could use the :ref:`cron job <cron-track-total-checkouts-label>` to have
   Koha update that field nightly.

.. _usecirculationdesks-label:

UseCirculationDesks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ circulation desks with circulation

Default: Don't use

Values:

-  Don't use

-  Use

Description:

-  This preference enables the ability to manage various circulation desks 
   within a single library.

.. _waitingnotifyatcheckin-label:

WaitingNotifyAtCheckin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't notify

Asks: \_\_\_ librarians of waiting holds for the patron whose items they
are checking in.

Values:

-  Don't notify

-  Notify

   |image43|

Description:

-  When checking in books you can choose whether or not to have a notice
   pop up if the patron who returned the book has a hold waiting for
   pick up. If you choose 'Notify' for WaitingNotifyAtCheckin then every
   time a hold is found for the patron who had the book out last a
   message will appear on your check in screen.

.. _interlibrary-loans-label:

Interlibrary Loans
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _circulateill-label:

CirculateILL
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ the circulation of ILL requested items.

Values:

-  Disable

-  Enable

Description:

-  This preference controls whether you have the option to checkout ILL items directly 
   from an ILL request.  More details can be found in the :ref:`Circulating ILL materials <circulating-ILL-material-label>` section.

.. _illcheckavailability-label:

ILLCheckAvailability
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't check

Asks: \_\_\_ external sources for availability during the request process.

Values:

-  Dont' check

-  Check

Description:

-  This preference controls whether specific external resources will be searched prior 
   to a request being placed.  The resources available are installed using plugins.  These can
   be located on the Koha plugins wiki page at https://wiki.koha-community.org/wiki/Koha_plugins.
   Currently there are plugins for EDS (Ebsco Discovery Service), Z39.50 and Unpaywall.  
   When a patron submits an ILL request the item metadata in the form is used to search the external resource.  
   The patron can then click on the title links in the displayed results. If they find the item they were requesting 
   the request can be abandoned. If not, the patron can continue with the request in the normal way.

.. _illdefaultstaffemail-label:

ILLDefaultStaffEmail
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: 	
Fallback email address for staff ILL notices to be sent to in the absence of a library address: \_\_\_ .

Description:

-  By default replies to ILL request emails will go to the library email address, if you would like to specify 
   a different email address you can do that here.

.. _illhiddenrequeststatuses-label:

ILLHiddenRequestStatuses
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: ILL statuses that are considered finished and should not be displayed in the ILL 
module: \_\_\_ (separated with \|). If left empty, all ILL requests will be displayed.

Description:

-  This preference allows libraries to hide requests from the View ILL requests list based on the status 
   of the request.  Available ILL statuses are configured in the ILLSTATUS 
   :ref:`authorized value <authorized-values-label>` category. 

.. _illmodule-label:

ILLModule
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ the interlibrary loans module (master switch).

Values:

-  Disable

-  Enable

Description:

-  This preference is used to enable Koha's ILL module which is used to manage ILL requests.

.. _illmodulecopyrightclearance-label:

ILLModuleCopyrightClearance
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Adding text will enable the copyright clearance stage in request creation.
The text you enter will be the text displayed.

.. _illmoduleunmediated-label:

ILLModuleUnmediated
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ unmediated interlibrary loan requests. If enabled and the ILL backend 
supports it, the newly created requests are immediately requested by backend.

Values:

-  Disable

-  Enable

Description:

-  This preference allows ILL requests placed by patrons on the OPAC to be directly sent to ILL suppliers
   without mediation by library staff.  Not all ILL backends can support this feature.

.. _illbpacbackends-label:

ILLOpacbackends
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Enabled ILL backends for OPAC initiated requests: \_\_\_ (separated with \|). If left empty, all 
installed backends will be enabled.

Description:

-  This preference controls which ILL backend request forms are available for OPAC requests.  You will need to 
   refer to the backend configuration guidance for the correct terminology to enter here, for example, FreeForm, BLDSS.

.. _illsendstaffnotices-label:

ILLSendStaffNotices
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Send these ILL notices to staff when appropriate: \_\_\_ (separated with \|). 
e.g. ILL_REQUEST_CANCEL|ILL_REQUEST_MODIFIED If left empty, no staff ILL notices will be sent.

Description:

-  You can configure which ILL notices should be sent to staff.  More details can be found 
   in the :ref:`ILL email notifications <ILL-email-notification-label>` section.


.. _returnclaims-label:

Return claims
~~~~~~~~~~~~~~~~~

The return claims feature tracks items that patrons claim to have returned.

To use this feature:

1.  Add a new authorized value to the LOST category to represent items claimed as returned.

2.  Enter the authorized value in the ClaimReturnedLostValue system preference - this enables the return claims feature.

3.  Set a value for the ClaimReturnedChargeFee system preference - the default is ask if a lost fee should be charged.

4.  Optional: Set a value for ClaimReturnedWarningThreshold system preference to alert librarians when a patron exceeds a set number of return claims.

Returning a claimed item will notify the librarian that the item has a claim on it. The librarian can then mark checked out items as return claims from the checkout and patron details pages, and modify them from the new claims tab on these pages.

ClaimReturnedChargeFee
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: When marking a checkout as "claims returned”,

Values:

-  Ask if a lost fee should be charged (default)

-  Charge a lost fee

-  Don't charge a lost fee

Description:

-  This preference allows a library to choose if a lost fee is charged at the time an item being claimed is returned. If set to ask, there is a checkbox to either charge or don’t charge per transaction. If set to charge, Koha will charge the patron the replacement price of the item. If set to don’t charge, Koha will not charge the patron.

ClaimReturnedLostValue
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Use the LOST authorised value  \_\_\_ to represent returns claims.

Description:

-  Add a LOST authorized value - this enables the return claims feature. Add a new authorized value to the LOST category to represent the library's return claims.

ClaimReturnedWarningThreshold
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Warn librarians that a patron has excessive return claims if the patron has claimed the return of more than \_\_\_ items.

Description:

-  Enter a number if a library would like to set a limit to the number of returns claims that the patron can have before showing a warning on the patron's screen.

Self check-in module (sci-main.pl)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _selfcheckinmainuserblock-label:

SelfCheckInMainUserBlock
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following HTML on the self check-in screen

Description:

-  HTML entered in this field will appear in the center of the main page
   of your self checkin screen

.. _selfscheckinmodule-label:

SelfCheckInModule
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't enable

Asks: \_\_\_ the standalone self check-in module (available at:
/cgi-bin/koha/sci/sci-main.pl

Values:

-  Don't enable

-  Enable

Description:

-  This system preference will activate (or deactivate) the self check-
   in module

.. _selfcheckintimeout-label:

SelfCheckInTimeout
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 120

Asks: Reset the current self check-in screen after \_\_\_ seconds

Description:

-  Enter the number of seconds after which you want the self check-in
   screen to refresh and go back to the main page (for example, if a
   patron forgot to log out).

.. _selfcheckinusercss-label:

SelfCheckInUserCSS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following CSS on all the self check-in screens

Description:

-  The CSS code entered here will override any CSS on the self check-in
   screens

.. _selfcheckinuserjs-label:

SelfCheckInUserJS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following JavaScript on all the self check-in screens

Description:

-  The JavaScript entered here will override any other JavaScript on
   the self check-in screens

.. _self-checkout-system-preferences-label:

Self check-out module (sco-main.pl)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _scouserjs-label:

SCOUserJS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following JavaScript on all pages in the web-based self 
checkout:

Description:

-  The JavaScript entered in this preference will affect all of your
   Koha self check-out screens.

.. _scomainuserblock-label:

SCOMainUserBlock
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following HTML on the web-based self checkout screen:

Description:

-  The HTML entered in this preference will be used on the main self check-out 
   screen.

.. _scousercss-label:

SCOUserCSS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following CSS on all pages in the web-based self checkout:

Description:

-  The CSS entered in this preference will be used on all of your Koha self 
   check-out screens.

.. _showpatronimageinwebbasedselfcheck-label:

ShowPatronImageInWebBasedSelfCheck
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the patron's picture (if one has been added) when they use the 
web-based self check-out.

Default: Don't show

Values:

-  Don't show

-  Show

Description:

-  If this system preference is set to 'Show', the patron will see their own 
   picture when logging into the web-based self check-out module.

.. _webbasedselfcheck-label:

WebBasedSelfCheck
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the web-based self checkout system.

Default: Don't enable

Values:

-  Don't enable

-  Enable

Description:

-  Enabling this preference will allow access to the :ref:`self check-out 
   <self-checkout-label>` module in Koha.

-  Your self check-out module is available at: https://YOUR.OPAC.URL/cgi-bin/koha/
   sco/sco-main.pl

.. _selfcheckoutbylogin-label:

SelfCheckoutByLogin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Have patrons login into the web-based self checkout system with
their \_\_\_

Default: Cardnumber

Values:

-  Cardnumber

   |image44|

-  Username and password

   |image45|

Description:

-  This preference lets you decide how your patrons will log in to the
   self checkout machine. Either the patron's card number (barcode) or their
   username and password set using the opac/staff username and
   password fields on the :ref:`patron record <add-a-new-patron-label>`.

.. _selfchecktimeout-label:

SelfCheckTimeout
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Time out the current patron's web-based self checkout system login
after \_\_\_ seconds.

Default: 120

Description:

-  After the machine is idle for the time entered in this preference the
   self check out system will log out the current patron and return to
   the starting screen.

.. _scoallowcheckin-label:

SCOAllowCheckin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ patrons to return items through web-based self checkout
system.

Default: Don't allow

Values:

-  Allow

-  Don't allow

Description:

-  This preference is used to determine if you want patrons to be
   allowed to return items through your self check machines. By default
   Koha's self check-out interface is simply for checking items out.

.. _selfcheckhelpmessage-label:

SelfCheckHelpMessage
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include the following HTML in the Help page of the web-based self
checkout system:

Description:

-  Clicking the 'Help' link in the top right of the self check-out
   interface opens up a three step process for using the self check-out
   module. Adding HTML to this system preference will show that
   additional help text above what's already included.

.. _autoselfcheck-preferences-label:

AutoSelfCheckAllowed, AutoSelfCheckID and AutoSelfCheckPass
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    **Important**

    Most libraries will want to leave this set to 'Don't allow'. This
    preference turns off the requirement to log into the self checkout
    machine with a staff username and password by storing the username
    and password for automatic login.

Asks: \_\_\_ the web-based self checkout system to automatically login
with this staff login \_\_\_ and this password \_\_\_ .

AutoSelfCheckAllowed default: Don't allow

AutoSelfCheckAllowed values:

-  Allow

-  Don't allow

AutoSelfCheckID value:

-  The username of a staff patron with the 'self\_checkout\_module'
   :ref:`permission <patron-permissions-defined-label>`.

AutoSelfCheckPass value:

-  The password of a staff patron with the 'self\_checkout\_module'
   :ref:`permission <patron-permissions-defined-label>`.

.. _selfcheckreceiptprompt-label:

SelfCheckReceiptPrompt
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the print receipt popup dialog when self checkout is finished.

Default: Show

Values:

-  Don't show

-  Show

Description:

-  This preference controls whether a prompt shows up on the web based
   self check-out when the patron clicks the 'Finish' button.

.. _selfcheckallowbyipranges-label:

SelfCheckAllowByIPRanges
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_

Description:

-  This system preference is used to limit access to the self check-out module 
   by IP ranges.

-  Use ranges or simple IP addresses separated by spaces, like 
   '192.168.1.1 192.168.0.0/24'.

-  If you do not want to limit access by IP range, leave this system preference 
   blank.

.. _stock-rotation-system-preferences-label:

Stock rotation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _stockrotation-module-label:

StockRotation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ the stock rotation module

Values:

-  Disable

-  Enable

Description:

-  If set to 'Enable' then the stock rotation module will appear under Tools.


