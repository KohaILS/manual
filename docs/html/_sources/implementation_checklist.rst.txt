.. include:: images.rst

.. _implementation-checklist-label:

Implementation checklist
===============================================================================

The following guide will walk you through the areas of Koha you need to
look at in order to prepare to start using the system.

It is not an exhaustive list of everything you need to do. Please consider your 
own library practices and what other checks are necessary for your own libary 
and context.

.. _data-migration-label:

Data migration
-------------------------------------------------------------------------------

Before you can start using Koha you'll need to have some data. This can
be done by entering it all by hand, but most people already have their
data in electronic format of some sort and just need to reformat it a
bit for importing into Koha.

-  Create a list of libraries and enter their info and codes into
   :ref:`libraries <libraries-label>`

-  Define your list of :ref:`item types <item-types-label>`

-  Define your patron categories and enter the categories and their
   codes into :ref:`patron categories <patron-categories-label>`

-  Enter any additional patron information fields you use in your
   library in the :ref:`patron attributes <patron-attribute-types-label>`

   -  This requires that you first enable the :ref:`ExtendedPatronAttributes` 
      system preference if you have custom fields

-  Define all of your :ref:`authorized values <authorized-values-label>`

   -  Collection codes (:ref:`CCODE <existing-values-label>`)

   -  Shelving locations (:ref:`LOC <existing-values-label>`)

   -  Item statuses

      -  Lost status (:ref:`LOST <existing-values-label>`)

      -  Not for loan status (:ref:`NOT\_LOAN <existing-values-label>`)

      -  Damaged status (:ref:`DAMAGED <existing-values-label>`)

      -  Withdrawn status (:ref:`WITHDRAWN <existing-values-label>`)

   -  Plus any others that are needed in your library

-  Optionally define :ref:`cities and towns <cities-and-towns-label>`

-  :ref:`Map your bibliographic data <koha-to-marc-mapping-label>` from your legacy
   system to Koha fields and migrate (remembering to use the collection,
   shelving, item type and library codes you entered in the above
   setting areas)

-  :ref:`Map your patron data <patron-import-label>` from your legacy system to
   the Koha fields and migrate (remembering to use the patron and
   library codes you defined above)

-  Test your migrated data to be sure that everything is as you expect
   it to be, some things to test include:

   -  Check some of your titles with diacritics and make sure that they
      migrated properly.

   -  Check titles in a series and make sure that series information
      migrated properly.

   -  Make sure that your patrons have their contact information in the
      right fields.

   -  If your serials data was migrated search for these records in the
      catalog and confirm that they look right.

   -  If your serials data was migrated search for these records in the
      serials module and confirm that they look right.

   -  Check marc records to verify a variety of items are cataloged
      correctly

   -  Check cataloging process to see if all necessary fields are
      available

   -  If fines are migrated, check to see that they are applied
      correctly

   -  If holds are migrated, check to see they are accurate in catalog
      and patron record

.. _admin-configuration-label:

Admin configuration
-------------------------------------------------------------------------------

Most of these preferences won't need to be changed to use your Koha
system, but there are a few that you might want to customize.

-  If your library uses CAS authentication, you'll want to set the
   various :ref:`CAS system preferences <cas-authentication-label>`

-  Administration system preferences

   -  :ref:`KohaAdminEmailAddress` : This is the
      email address that will be used by the system in 'from' lines and
      to send errors to if there is no email set for the branch

   -  :ref:`noItemTypeImages` : Decide if you want to
      show item type icons in the staff client and opac

   -  :ref:`csvdelimiter` : This value will be put in between
      fields when exporting data from Koha

   -  :ref:`virtualshelves` : Decide if you want the
      staff and/or patrons to use lists in Koha

   -  :ref:`AutoLocation` : Require staff to log in to the
      staff client from a specific IP range

   -  :ref:`IndependentBranches` : Prevent
      librarians from editing content that belongs to other branches

-  Go through the :ref:`log system preferences <logs-label>` and decide which
   actions you want to keep track of in the :ref:`logs <log-viewer-label>`

-  Decide if you'd like to share your library's information with the
   Koha community by setting the :ref:`sharing system
   preferences <share-anonymous-usage-statistics-label>`.

-  Decide what :ref:`cron jobs <cron-jobs-label>` you need to run and when.

   -  If you're using the :ref:`long overdue cron job <cron-long-overdues-label>` 
      be sure to set your :ref:`DefaultLongOverdueChargeValue`,
      :ref:`DefaultLongOverdueLostValue <defaultlongoverduelostvalue-and-defaultlongoverduedays-label>` and
      :ref:`DefaultLongOverdueDays <defaultlongoverduelostvalue-and-defaultlongoverduedays-label>`
      preferences.

.. _localization-configuration-label:

Localization configuration
-------------------------------------------------------------------------------

Koha is used worldwide and so you need to make sure you set your
localization preferences so that options throughout Koha appear properly
for your location/language.

-  Localization/internationalization system preferences

   -  :ref:`dateformat` : Decide how dates are displayed throughout Koha

   -  :ref:`opaclanguagesdisplay` : Decide if patrons can choose what language 
      the OPAC appears in

      -  :ref:`OPACLanguages` : Decide which languages the patrons can choose 
         from

   -  :ref:`language` : Decide which languages appear in the staff interface

   -  :ref:`CalendarFirstDayOfWeek` : Define your first day of the week

.. _circulation-configuration-label:

Circulation configuration
-------------------------------------------------------------------------------

Before you start circulating your collection you'll need to set up your
rules and preferences for circulation.

-  Define your :ref:`circulation and fines rules <circulation-and-fines-rules-label>`

-  Enter the :ref:`days your library is closed <calendar-label>` for fines
   and due date calculations

-  Circulation system preferences

   -  :ref:`CircControl` : Define whether circ rules are based on item's 
      location, patron's location or transaction location

   -  :ref:`useDaysMode` : Define how due dates are calculated

   -  :ref:`finesCalendar` : Define how fines are calculated (for every late 
      date or only for days the library is open)

   -  :ref:`SpecifyDueDate` : Decide if staff are allowed to override due dates 
      on checkout

   -  :ref:`SpecifyReturnDate` : Decide if you want to let the staff specify 
      an arbitrary return date on checkin

   -  :ref:`itemBarcodeFallbackSearch` :
      Decide if you want staff to be able to checkout using a keyword
      search (title, call number, etc)

   -  :ref:`AutomaticItemReturn` : Decide if items are sent back to the owning 
      branch when checked in

   -  :ref:`todaysIssuesDefaultSortOrder` :
      Decide how items checked out today display on the patron record

   -  :ref:`previousIssuesDefaultSortOrder` : Decide how items checked out 
      prior to today display on the patron record

   -  :ref:`noissuescharge` : Define the maximum amount a patron can owe 
      before checkouts are blocked

   -  :ref:`ReturnBeforeExpiry` : Decide if patrons need to return items 
      before their accounts expire

   -  :ref:`AllowHoldsOnDamagedItems` : Decide
      if patrons can place holds on items that are marked as damaged

      -  :ref:`AllowHoldPolicyOverride` : Decide if you want the staff to be 
         able to override this setting

   -  :ref:`maxreserves` : Decide how many items a patron
      can have on hold at once

      -  :ref:`AllowHoldPolicyOverride` : Decide if you want the staff to be 
         able to override this setting

   -  :ref:`maxoutstanding` : Define the maximum amount a
      patron can owe before holds are blocked

      -  :ref:`AllowHoldPolicyOverride` : Decide if you want the staff to be 
         able to override this setting

   -  :ref:`ReservesMaxPickUpDelay` : Define the number of days before a hold 
      expires

   -  :ref:`WebBasedSelfCheck` : Decide if you want to use the built in 
      web-based self-checkout system

      -  :ref:`AutoSelfCheckAllowed <autoselfcheck-preferences-label>` : Decide 
         if the self-checkout system requires login

      -  :ref:`ShowPatronImageInWebBasedSelfCheck`: Decide if you want patron 
         images to show on the self checkout screen

   -  :ref:`AllowNotForLoanOverride` : Decide if you want the staff to be able 
      to checkout items marked as 'not for loan'

   -  :ref:`AllowRenewalLimitOverride` : Decide if you want staff to override 
      the limit put on renewals

   -  :ref:`AllowFineOverride` : Decide if you want staff to be able to 
      override fine limits

   -  :ref:`AllowTooManyOverride` : Descide if you want staff to be able to 
      check out more than the limit to a patron

   -  :ref:`RenewalPeriodBase` : Decide what date renewals are based on

   -  :ref:`finesMode` : Switch to 'Calculate and Charge' before you go live if 
      you charge fines

   -  :ref:`NoticeBcc`: If you want to receive a copy of every notice, enter your 
      email address

   -  :ref:`emailLibrarianWhenHoldIsPlaced`: Decide if you want an email every 
      time a hold is placed

   -  :ref:`ReservesControlBranch` : Decide which branch's hold rules are 
      considered first

   -  :ref:`AudioAlerts`: Decide if you want to have sounds for circulation 
      actions

      -  Set the sounds and actions in the :ref:`audio alerts <audio-alerts-label>` 
         section of the administration module

   -  :ref:`FilterBeforeOverdueReport` : If you have a large amount of 
      overdues, you might want to turn this preference on so as to allow you to 
      filter before results appear

   -  :ref:`DisplayClearScreenButton` : If you have a lot of staff members 
      sharing one circulation computer you might want to enable this so that 
      staff can clear the screen in between checkouts to protect patrons' 
      privacy

   -  :ref:`CircAutoPrintQuickSlip` : Decide how you want Koha to react if you 
      scan in a blank barcode on the checkout screen

   -  :ref:`SuspendHoldsIntranet` and/or :ref:`SuspendHoldsOpac` : Decide if 
      you want patrons and/or staff to be able to suspend holds

      -  :ref:`AutoResumeSuspendedHolds` : If you allow holds to be suspended 
         decide if you want them to automatically resume on the date entered 
         by the staff and/or patron

   -  :ref:`OnSiteCheckouts` : Decide if you want to allow items to be checked 
       out for use within the library

   -  :ref:`RecordLocalUseOnReturn` : Set this to record local use of items 
      when you check them in

-  Customize your :ref:`Notices and slips <notices-and-slips-label>`

-  Define your :ref:`overdue notice triggers <overdue-notice/status-triggers-label>`

-  Set up your :ref:`cron jobs <cron-jobs-label>`

   -  Populate :ref:`your holds queue <holds-queue-label>` (every 1-4 hours)

   -  Decide :ref:`when holds expire <cron-expired-holds-label>` (daily)

   -  :ref:`Calculate fines due <cron-fines-label>` (daily)

      -  Fines on hourly loans will calculate when you check the items
         in

   -  :ref:`Mark long overdue items as lost <cron-long-overdues-label>` (daily)

   -  Decide when the system :ref:`sends out messages <cron-message-queue-label>` (1-4
      hours)

   -  Decide when the system :ref:`queues overdue notices <cron-overdue-notice-label>` 
      (daily)

   -  Set up :ref:`hold notices that didn't send for printing <cron-print-hold-notices-label>` 
      (daily after overdues and message queue)

   -  Decide when the system :ref:`queues the advanced notice of items due <cron-advanced-notice-label>` 
      (daily)

   -  Find holds that need to be :ref:`resumed and remove suspension <cron-unsuspend-holds-label>` 
      (daily)

   -  If you're allowing automatic renewal of items :ref:`set them to renew <cron-automatic-renewal-label>` 
      (nightly)

.. _patron-configuration-label:

Patron configuration
-------------------------------------------------------------------------------

You have already imported patron data from your old system, but there
are plenty of options available to you regarding patrons and their
accounts.

-  Enter your :ref:`staff members as patrons <add-a-staff-patron-label>`

   -  Define :ref:`staff members access permissions <patron-permissions-label>`

-  Patron system preferences

   -  :ref:`autoMemberNum` : Decide if the patron barcodes are auto-generated 
      or if you enter them yourself

   -  :ref:`MaxFine` : Determine the maximum amount that people can owe in fines

   -  :ref:`NotifyBorrowerDeparture` : Decide when to warn staff that the 
      patron account is about to expire

   -  :ref:`intranetreadinghistory` : Decide if the staff can see the patron's 
      reading/checkout history

   -  :ref:`BorrowerMandatoryField` : List fields that you want to appear as 
      mandatory on the patron add/edit form

   -  :ref:`BorrowersTitles` : Add or change the titles for your patrons

   -  :ref:`borrowerRelationship` : Add or change borrower relationships 
      (child to adult and professional to organization)

   -  :ref:`AutoEmailPrimaryAddress` : Determine if the patrons get an email 
      confirming the creation of their account

   -  :ref:`EnhancedMessagingPreferences` : Decide if staff can choose from a 
      series of notices (other than overdues) for patrons

   -  :ref:`EnhancedMessagingPreferencesOPAC`: Decide if patrons can choose 
      from a series of notices (other than ovedues) for themselves

   -  :ref:`patronimages` : Decide if you want to save patron pictures in your 
      system

   -  :ref:`ExtendedPatronAttributes` : Decide if you want to enable custom 
      patron fields

   -  :ref:`minPasswordLength` : Enter the minimum number of characters you 
      want passwords to have

   -  :ref:`BorrowerUnwantedField` : Decide what fields your library doesn't 
      need to see on the patron entry form

-  Set up your :ref:`cron jobs <cron-jobs-label>`

   -  Decide if you would like children to automatically become adults by setting up the
      :ref:`Update patron categories <cron-update-patron-categories-label>` cron job.

.. _cataloging-configuration-label:

Cataloging configuration
-------------------------------------------------------------------------------

Before you start cataloging in Koha you'll want to set up your
preferences and other rules.

-  Define your cataloging templates, or 
   :ref:`MARC bibliographic frameworks <marc-bibliographic-frameworks-label>`

   -  Run the :ref:`MARC bibliographic framework test <marc-bibliographic-framework-test-label>` 
      to be sure your changes are valid

-  Define any :ref:`authorized values <authorized-values-label>` you might want
   to use in cataloging

-  Set up :ref:`custom classification sources <classification-sources-label>` (if
   you use something other than the defaults)

-  Set up :ref:`MARC matching rules <record-matching-rules-label>` for importing
   records from .mrc files

-  Set up the :ref:`Z39.50 targets <z39.50/sru-servers-label>` you want to 
   search for cataloging (and acquisitions)

-  Cataloging system preferences

   -  :ref:`URLLinkText` : Enter text to display when 856 fields do not have 
      pre-defined labels

   -  :ref:`hide\_marc <hide-marc-label>` : If you are unfamiliar with MARC you
      can have the MARC fields number hidden

   -  :ref:`LabelMARCView` : Choose how you want duplicate fields to appear on 
      the editor

   -  :ref:`DefaultClassificationSource` : Choose which classification source 
      is the default in your library

   -  :ref:`advancedMARCeditor` : Decide if you want to use the advanced MARC 
      editor

   -  :ref:`marcflavour` : Choose your MARC format

   -  :ref:`itemcallnumber` : Enter which field and subfields to look into for 
      the call number

   -  :ref:`MARCOrgCode` : Enter your MARC organizational code (not the same as 
      your OCLC number)

   -  :ref:`autoBarcode` : Decide if Koha generates item barcodes for you

   -  :ref:`OpacSuppression <opacsuppression-preferences-label>` : Decide if 
      you want to hide records marked as suppressed from the OPAC search results

-  Set up your :ref:`cron jobs <cron-jobs-label>`

   -  Decide when the system :ref:`checks URLs in catalog records <cron-check-url-quick-label>` 
      to see if they are still valid

.. _authorities-configuration-label:

Authorities configuration
-------------------------------------------------------------------------------

Koha has the ability to keep track of your authority records and how
they're linked to your bibliographic records. Before using authorities
you should configure several preferences.

-  Set :ref:`authority frameworks <authority-types-label>`, or templates

-  Authority system preferences

   -  :ref:`BiblioAddsAuthorities` : Decide if Koha creates authorities when 
      cataloging

   -  :ref:`AuthorityMergeLimit`: Decide if updates to authorities trigger 
      updates to the bibliographic records that link to them

   -  :ref:`AutoCreateAuthorities` : Decide when authorities are created

   -  :ref:`LinkerModule` : Decide which match the authority linker should use

   -  :ref:`LinkerOptions` : Decide if you want authority linking to be broader 
      or more specific

   -  :ref:`CatalogModuleRelink` : Decide if you want to enable authority 
      linking while cataloging

-  Set up your :ref:`cron jobs <cron-jobs-label>`

   -  Choose when the system looks for authorities updates to 
      :ref:`merge changes into bibliographic records <cron-update-authorities-label>`

.. _searching-configuration-label:

Searching configuration
-------------------------------------------------------------------------------

There are several system preferences related to searching, it is not
always recommended to make too many changes to these preferences since
they are set to get you the most relevant results. If you would like to
change the default way that Koha handles searching, view the 
:ref:`searching system preferences <searchingsystem-preferences-label>` tab.

-  Set up your :ref:`cron jobs <cron-jobs-label>`

-  Searching system preferences

   -  :ref:`AdvancedSearchTypes` : Decide which authorized value fields you 
      want patrons and staff to be able to limit their advanced searches by

   -  :ref:`AdvancedSearchLanguages` : Decide which languages you want people 
      to be able to limit to via the search engine

   -  :ref:`UseAuthoritiesForTracings` : Decide how you want Koha to handle 
      subject searches in the OPAC

      -  :ref:`TraceCompleteSubfields` : Decide how you want Koha to handle 
         subject searches in the OPAC

      -  :ref:`TraceSubjectSubdivisions` : Decide how you want Koha to handle 
          subject searches in the OPAC

   -  :ref:`displayFacetCount` : Decide whether to show facet counts on search 
      results

.. _opac-configuration-label:

OPAC configuration
-------------------------------------------------------------------------------

There are a lot of ways you can customize your OPAC in Koha.

-  Decide how you want your OPAC to look & what content you want on the
   main page

-  Create a library branded stylesheet using CSS

   **Important**

   Do not edit the default CSS files, instead create a new one,
   that way the system can always fall back on the original CSS.

-  Create a custom XSLT stylesheet to change the way search results and
   bib records appear in the OPAC

-  OPAC system preferences

   -  :ref:`OPACBaseURL` : Enter your library's URL

   -  :ref:`opacuserlogin` : Decide if you want to allow patrons to login to 
      the OPAC to access customized functionality (searching will be allowed 
      without logging in)

      -  :ref:`RequestOnOpac` : Decide if patrons can place holds via the OPAC

      -  :ref:`OpacPasswordChange` : Decide if patrons can change their 
         password (don't allow this if you're using LDAP)

      -  :ref:`OpacRenewalAllowed` : Decide if patrons can renew their checked 
         out items via the OPAC

      -  :ref:`opacreadinghistory` : Decide if patrons can view their reading/
         checkout history via the OPAC

      -  :ref:`OPACComments` : Decide if you want to allow patrons to comment on 
         bibliographic records via the OPAC

      -  :ref:`OpacStarRatings` : Decide if patrons can leave star ratings

      -  :ref:`virtualshelves` : Decide if you want patrons to be able to 
         create lists

      -  :ref:`OpacAllowPublicListCreation`: If patrons can create lists then 
         decide if they are allowed to create public lists

      -  :ref:`suggestion` : Decide if you want patrons to be able to submit 
         purchase suggestions

      -  :ref:`OPACViewOthersSuggestions` : Decide if you want patrons to be 
         able to see purchase suggestions made by other patrons

   -  :ref:`opacbookbag` : Decide if patrons can save items into their cart

   -  :ref:`AnonSuggestions` : Decide if you want non logged in users to be 
      able to make purchase suggestions

   -  :ref:`LibraryName` : Enter your library name for display in the <title> 
      tag and on the top of the OPAC

   -  :ref:`OpacNav` : Enter HTML that will appear to the left on the main OPAC 
      page

   -  :ref:`OpacNavBottom` : Enter HTML that will appear below OpacNav

   -  :ref:`OPACNoResultsFound` : Enter the HTML that will appear when no 
      results are found

   -  :ref:`OPACResultsSidebar` : Enter the HTML that will appear below the 
      facets on your search results

   -  :ref:`OPACMySummaryHTML` : Enter the HTML that will appear in the far 
      right of the circulation summary in the OPAC

   -  Customize your stylesheets:

      -  :ref:`OPACUserCSS` : Enter any additional fields you want to define 
         styles for

      -  :ref:`opaclayoutstylesheet` : Point to a CSS file on your Koha server

   -  :ref:`OpacHighlightedWords <opachighlightedwords-and-nothighlightedwords-label>` : 
      Decide if you want search terms to be highlighted on the search results

   -  :ref:`hidelostitems` : Decide if you want to show patrons items you have 
      marked as lost

   -  :ref:`BiblioDefaultView` : Decide what view is the default for 
      bibliographic records on the OPAC

   -  :ref:`OPACShelfBrowser` : Decide if you want to enable the shelf browse 
      functionality

   -  :ref:`OPACURLOpenInNewWindow` : Decide if URLs clicked in the OPAC are 
      opened in a new window

   -  :ref:`SearchMyLibraryFirst` : If you have a multi-branch system decide if 
      you want patrons to search their library first

   -  :ref:`OpacAuthorities` : Decide if you want patrons to be able to search 
      your authority file

   -  :ref:`OpacBrowser` : Decide if you want patrons to browse your authority 
      file (French libraries only)

   -  :ref:`OPACSearchForTitleIn` : Choose which libraries you want patrons to 
      be able to re-run their search in

   -  :ref:`OpacAddMastheadLibraryPulldown` : If you're a multi-branch system 
      you can add a pull down to the search bar for patrons to search which 
      library to search

   -  :ref:`EnableOpacSearchHistory` : Decide if you want the system to keep a 
      search history

-  Set up your :ref:`cron jobs <cron-jobs-label>`

   -  If you have the :ref:`OpacBrowser` preference set decide 
      :ref:`when you want the contents to rebuild <cron-authorities-browser-label>` 
      (French libraries only)

   -  If you have :ref:`custom RSS feeds <custom-rss-feeds-label>`, decide 
      when you want the :ref:`feed to be populated <cron-rss-feeds-label>`

.. _editable-opac-regions-label:

Editable OPAC regions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Using the :ref:`news tool <news-label>` you can customize various blocks of the 
OPAC. The following graphic shows what each display location updates in the 
Bootstrap theme.

|image1068|

|image1069|

Some of the regions are system preferences:

-  :ref:`OpacNav`

-  :ref:`OpacNavBottom`

And 'quotes of the day' are managed in the 
:ref:`Quote of the day editor <quote-of-the-day-(qotd)-editor-label>`

.. _enhanced-content-configuration-label:

Enhanced content configuration
-------------------------------------------------------------------------------

Koha allows you to pull in content from outside sources to enhance your
bibliographic records. All of this content can be toggled on and off using the
:ref:`enhanced content system preferences <enhanced-content-system-preferences-label>`.

-  :ref:`FRBR/Editions <frbrizeeditions-label>`

   -  If you would like to have your OPAC and/or staff interdace show an
      'Editions' tab on the bibliographic record, you want to enable one or the
      other FRBR preferences and then the ISBN service :ref:`ThingISBN`.

-  :ref:`Amazon <amazon-system-preferences-label>` : This service is free and 
   just requires that you visit http://aws.amazon.com to sign up

   -  Using the Amazon preferences you can choose to show cover images
      from Amazon.

-  :ref:`Babelthèque <babeltheque-system-preferences-label>`

   -  This is a paid service. Contact Babelthèque to learn how to enable
      this content in the OPAC.

-  :ref:`Baker and Taylor <baker-and-taylor-label>`

   -  This is a paid service from Baker & Taylor. Contact Baker & Taylor
      for the information to enter into these preferences.

-  :ref:`HTML5 media <html5-media-label>`

   -  This allows libraries to embed streaming media in their catalog

-  :ref:`Google <googlejackets-label>`

   -  This service is free and does not require registration, simply
      enable :ref:`GoogleJackets` and you're set to go.

-  :ref:`LibraryThing <librarything-label>`

   -  With the exception of :ref:`ThingISBN`, you will need to contact
      LibraryThing for the information to enter into these preferences

   -  Enabling :ref:`ThingISBN` will help to populate the editions tab on the
      bibliographic record display if you have enabled FRBR.

-  :ref:`Novelist Select <novelist-select-label>`

   -  This is a paid service from Ebsco. Contact Ebsco for the
      information to enter into these preferences

-  :ref:`Open Library <open-library-label>`

   -  Open Library project is an open system that you can pull cover
      images (and in the future additional content) from

-  :ref:`Overdrive <overdrive-label>`

   -  This is a paid service that libraries can subscribe to for ebook
      content. If the library subscribes to Overdrive they can integrate
      that content in to Koha for free.

-  :ref:`Syndetics <syndetics-label>`

   -  This is a paid service from Syndetics to add content for your 
      bibliographic records. Contact Syndetics for the information to enter 
      into these preferences.

-  :ref:`Tagging <tagging-label>`

   -  Choose whether or not you want to allow patrons to add tags to
      records in Koha.

.. _acquisitions-configuration-label:

Acquisitions configuration
-------------------------------------------------------------------------------

When using acquisitions in Koha you first need to define some defaults.

-  Set up your :ref:`funds and budgets <budgets-label>`

-  Choose your :ref:`default currency <currencies-and-exchange-rates-label>` 
   and enter others if you order from multiple countries

-  Enter in your :ref:`vendor information <vendors-label>`

-  Create an :ref:`framework with the code ACQ <marc-bibliographic-frameworks-label>` 
   (if you're going to enter item records at the time of ordering or receiving)

-  Acquisitions system preferences

   -  :ref:`AcqCreateItem` : Decide if an item record is created during 
      acquisition

   -  :ref:`CurrencyFormat` : Decide how you want monetary amounts to display

   -  :ref:`TaxRates` : Enter your sales tax (if you are billed for tax)

   -  :ref:`OrderPdfFormat` : Decide what format you want your print orders to 
      use

.. _serials-configuration-label:

Serials configuration
-------------------------------------------------------------------------------

When you use serials there are a few options you can set before hand.

-  Serials system preferences

   -  :ref:`RenewSerialAddsSuggestion` : Decide if you want renewing serials 
      to add a suggestion for easy purchasing

   -  :ref:`RoutingSerials` : Decide if you want to route serials around your 
      library

   -  :ref:`RoutingListAddReserves` : Decide if holds are placed on serials 
      when there is a routing list in place

-  Cataloging system references

   -  :ref:`StaffSerialIssueDisplayCount` : Decide how many of the most recent 
      issues to display in the staff interface

   -  :ref:`OPACSerialIssueDisplayCount` : Decide how many of the most recent 
      issues to display in the OPAC

   -  :ref:`SubscriptionHistory` : Decide how you want the subscription 
      information to display in the OPAC

.. _planning-for-go-live-label:

Planning for go-live
-------------------------------------------------------------------------------

Once you have all of your settings ready, you need to prepare for making
your system live:

-  Decide if you need training by an outside service provider or if your staff
   can do the training themselves.

-  Make sure that there is time for your staff to play with your test
   system and get comfortable with it

-  If this is a migration, work with your previous company to extract
   data right before you go-live

-  Decide on URLs for your new Koha OPAC and staff interface and arrange for 
   these to be cut-over if using existing system URLs, or created if they are 
   new URLs

-  Make sure that if you're hosting your own system you have a process in place 
   to back-up your system data.
