.. include:: images.rst

.. _cataloging-system-preferences-label:

Cataloging
--------------------------

*Get there:* More > Administration > Global System Preferences >
Cataloging

.. _display-label:

Display
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _acquisitiondetails-label:

AcquisitionDetails
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Display

Asks: \_\_\_ acquisition details on the biblio detail page.

Values:

-  Display

-  Don't display

Description:

-  This preference controls whether a tab will show on the detail page
   in the staff client that includes detailed acquisitions information
   for the title. This tab will include links to order information
   stored in the acquisitions module.

   |image1180|

.. _authorityseparator-label:

AuthoritySeparator
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Separate main entry and subdivisions with \_\_\_.

Default: --

Description:

-  This system preference allows you to choose the character or characters that 
   is used to separate the main entry and the subdivisions in authorities.

   For example, -- will make authorities appear like this:

   Cats--Fiction

-  This is used for non-XSLT views only. Whether or not you use XSLT views is 
   determined by the following system preferences:

   -  :ref:`OPACXSLTDetailsDisplay`

   -  :ref:`OPACXSLTListsDisplay`

   -  :ref:`OPACXSLTResultsDisplay`

   -  :ref:`XSLTDetailsDisplay`

   -  :ref:`XSLTListsDisplay`

   -  :ref:`XSLTResultsDisplay`

.. _hide-marc-label:

hide\_marc
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Display

Asks: \_\_\_ MARC tag numbers, subfield codes and indicators in MARC
views.

Values:

-  Display -- shows the tag numbers on the cataloging interface

   |image15|

-  Don't display -- shows just descriptive text when cataloging

   |image16|

.. _intranetbibliodefaultview-label:

IntranetBiblioDefaultView
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: ISBD form

Asks: By default, display biblio records in \_\_\_

Values:

-  ISBD form -- displays records in the staff client in the old card
   catalog format

   -  See :ref:`ISBD` preference for more information

-  Labelled MARC form -- displays records in the staff client in MARC
   with text labels to explain the different fields

-  MARC form -- displays records in the staff client in MARC

-  normal form -- visual display in the staff client (for the average
   person)

Description:

-  This setting determines the bibliographic record display when
   searching the catalog on the staff client. This setting does not
   affect the display in the OPAC which is changed using the
   :ref:`BiblioDefaultView` preference under the OPAC
   preference tab. This setting changes the look of the record when
   first displayed. The MARC and ISBD views can still be seen by
   clicking in the sidebar.

.. _isbd-label:

ISBD
^^^^^^^^^^^^^^^^^^^^

Default: See `ISBD view configuration
<https://wiki.koha-community.org/wiki/ISBD_view_configuration>` on the wiki.

Asks: Use the following as the ISBD template:

Description:

-  This determines how the ISBD information will display in the staff
   client. Elements in the list can be reordered to produce a different
   ISBD view. ISBD, the International Standard Bibliographic
   Description, was first introduced by IFLA (International Federation
   of Library Associations) in 1969 in order to provide guidelines for
   descriptive cataloging. The purpose of ISBD is to aid the
   international exchange of bibliographic records for a variety of
   materials.

.. _labelmarcview-label:

LabelMARCView
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't

Asks: \_\_\_ collapse repeated tags of the same type into one tag entry.

Values:

-  Do -- will combine all identical tag numbers under one heading in the
   MARC view in the OPAC and Staff Client

   |image17|

-  Don't -- will list all of the tags individually in the MARC view in
   the OPAC and Staff Client

   |image18|

.. _marcfielddocurl-label:

MARCFieldDocURL
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: blank

Asks: Use \_\_\_ as the URL for MARC field documentation. Possible substitutions are {MARC} (marc flavour, eg. "MARC21" or "UNIMARC"), {FIELD} (field number, eg. "000" or "048"), {LANG} (user language, eg. "en" or "fi-FI"). If left empty, the format documentation on http://loc.gov (MARC21) or http://archive.ifla.org (UNIMARC) is used. For example http://fielddoc.example.com/?marc={MARC}&field={FIELD}&language={LANG}

Description:

-  This preference lets you choose the source of the MARC documentation available through the "?" next to MARC fields.

.. _mergereportfields-label:

MergeReportFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ fields to display for deleted records after merge

Description:

-  When merging records together you can receive a report of the merge
   process once it's done, this preference lets you set the default
   values for this report.

Example: '001,245ab,600' displays:

-  value of 001

-  subfields a and b of fields 245

-  all subfields of fields 600

.. _notestohide-label:

NotesToHide
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Don't show these \_\_\_ note fields in title notes separator (OPAC
record details) and in the description separator (Staff client record
details).

Description:

-  This preference lets you define which of your note fields are hidden
   from the title notes (OPAC) and descriptions (Staff) tabs. Enter the
   values as a comma separated list. For example to hide the local note
   and the bibliography note in MARC21 enter 504, 590.

.. _opacsuppression-preferences-label:

OpacSuppression, OpacSuppressionByIPRange, OpacSuppressionRedirect, and OpacSuppressionMessage
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

OpacSuppression 
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Asks: \_\_\_ bibliographic records marked as suppressed from OPAC search results.

Default: Don't hide

Values:

-  Don't hide

   -  Will show records in OPAC search results even if they are marked as 
      suppressed

-  Hide

   -  Will not show records in OPAC search results if they're marked as
      suppressed

Description:

-  This preference controls hiding of bibliographic records in the OPAC. Enter 
   "1" in the field mapped to the suppress index (942$n in MARC21, no official 
   field in UNIMARC) in each bibliographic record you want to hide from
   the OPAC. The indexer then hides it from display in OPAC but will still 
   display it in the staff interface. 

.. Note::

   An :ref:`authorized value <authorized-values-label>` should be set for the 
   MARC21 942$n field (or the equivalent UNIMARC field) to eliminate errors. 
   You can use the YES\_NO authorized value category, or create a new one 
   titled SUPPRESS, for example, with a value of 0 for don't suppress and 1
   for suppress.

.. Warning::

   If this preference is set to 'hide' and you have the 942$n field set to 1, 
   it will hide the entire bibliographic record, not just an individual item.

.. Note::

   Suppressed records will show a note in the staff interface indicating that 
   they are suppressed from view in the OPAC.

   |suppressedstaff|

   This note can be styled by using the :ref:`IntranetUserCSS` preference to 
   stand out more if you'd like.

   |suppressedstyled|

   Fot the example above, the following snippet was added to 
   :ref:`IntranetUserCSS`

   .. code-block:: css

     .suppressed_opac {
       font-size: larger;
       color: red;
     }

OpacSuppressionByIPRange
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Asks: Restrict the suppression to IP addresses outside of the IP range \_\_\_
(Leave blank if not used. Define a range like 192.168..) 

Description:

-  If you want to further control suppression you can set an IP address range 
   to still show suppressed items to. Define a range like 192.168.. If you 
   don't want to limit suppression in this way, leave the IP field blank. 

OpacSuppressionRedirect 
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Asks: Redirect the opac detail page for suppressed records to \_\_\_

Values:

-  the 404 error page ('Not found').

-  an explanatory page ('This record is blocked').

Default: an explanatory page ('This record is blocked')

Description:

-  This preference lets you decide what the patrons will see in the OPAC when 
   a record is suppressed. You can either show the patron a 404 error page or 
   an explanatory page when they try to see a suppressed record. You can change 
   the message of the explanatory page with the 
   :ref:`OpacSuppressionMessage` system preference.

OpacSuppressionMessage
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Asks: Display the following message on the redirect page for suppressed 
bibliographic records \_\_\_.

Description:

-  If you chose to show an explanatory page when a patron tries to access a 
   suppressed bibliographic record, you can customize the message with HTML.

.. _separateholdings-and-separateholdingsbranch-label:

SeparateHoldings and SeparateHoldingsBranch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

SeparateHoldings default: Don't separate

SeparateHoldingsBranch default: home library

Asks: \_\_\_ items display into two tabs, where the first tab contains
items whose \_\_\_ is the logged in user's library. The second tab will
contain all other items.

SeparateHoldings values:

-  Don't separate

-  Separate

SeparateHoldingsBranch values:

-  holding library

-  home library

Description:

-  This preference lets you decide if you would like to have the holding
   information on the bibliographic detail page in the staff client
   split in to multiple tabs. The default is to show all holdings on one
   tab.

   |image19|

.. _urllinktext-label:

URLLinkText
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Online Resource

Asks: Show \_\_\_ as the text of links embedded in MARC records.

Description:

-  If the 856 field does not have a subfield 3 or y defined, the OPAC
   will say 'Click here to access online.^ If you would like the field
   to say something else enter that in this field.

.. _usecontrolnumber-label:

UseControlNumber
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't use

Asks: \_\_\_ record control number ($w subfields) and control number
(001) for linking of bibliographic records.

Values:

-  Don't use

   -  When clicking on links to titles that appear next to 'Continues'
      and 'Continued by' in the detail display Koha will perform a title
      search

-  Use

   -  When clicking on links to titles that appear next to 'Continues'
      and 'Continued by' in the detail display Koha will perform a
      control number (MARC field 001) search

    **Important**

    Unless you are going in and manually changing 773$w to match your
    rigorously-defined bibliographic relationships, you should set this
    preference to "Don't use" and instead set
    :ref:`EasyAnalyticalRecords` to "Display"

Description:

-  If you have a serial called "Journal of Interesting Things" which has
   a separate record from when it was called "Transactions of the
   Interesting Stuff Society," you could add linking fields to indicate
   the relationship between the two records. UseControlNumber allows you
   to use your local accession numbers for those links. In MARC21, the
   relevant sections of the two records might look like this:

   ::

           =001    12345
           =110  2_$aInteresting Stuff Society.
           =245  10$aTransactions of the Interesting Stuff Society.
           =785  00$aInteresting Stuff Society$tJournal of Interesting Things.$w12346

           =001    12346
           =110  2_$aInteresting Stuff Society.
           =245  10$aJournal of Interesting Things.
           =780  00$aInteresting Stuff Society$tTransactions of the Interesting Stuff Society.$w12345

   With UseControlNumber set to 'Use', the 78x links will use the
   Control Numbers is subfield $w, instead of doing a title search on
   "Journal of Interesting Things" and "Transactions of the Interesting
   Stuff Society" respectively.

.. _exporting-label:

Exporting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _bibtexexportadditionalfields-label:

BibtexExportAdditionalFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include following fields when exporting BibTeX

Description:

-  Use one line per tag in the format BT\_TAG: TAG$SUBFIELD ( e.g. lccn:
   010$a )

-  To specify multiple marc tags/subfields as targets for a repeating
   BibTex tag, use the following format: BT\_TAG: [TAG2$SUBFIELD1,
   TAG2$SUBFIELD2] ( e.g. notes: [501$a, 505$g] )

-  All values of repeating tags and subfields will be printed with the
   given BibTeX tag.

-  Use ^@^ ( with quotes ) as the BT\_TAG to replace the bibtex record
   type with a field value of your choosing.

.. Warning ::

   Requires YAML syntax to work

   This means

   -  Make sure there is NO space between the field name and the colon

   -  Make sure there IS a space between the colon and the value

   -  If there are more than one values for the same field, put them in
      square brakets, separated by comma and space

   -  Make sure each pair is on its own line

.. _risexportadditionalfields-label:

RisExportAdditionalFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Include following fields when exporting RIS

Description:

-  Use one line per tag in the format RIS\_TAG: TAG$SUBFIELD ( e.g. LC:
   010$a )

-  To specificy multiple marc tags/subfields as targets for a repeating
   RIS tag, use the following format: RIS\_TAG: [TAG2$SUBFIELD1,
   TAG2$SUBFIELD2] ( e.g. NT: [501$a, 505$g] )

-  All values of repeating tags and subfields will be printed with the
   given RIS tag.

-  Use of TY ( record type ) as a key will *replace* the default TY with
   the field value of your choosing.

.. Warning ::

   Requires YAML syntax to work

   This means

   -  Make sure there is NO space between the field name and the colon

   -  Make sure there IS a space between the colon and the value

   -  If there are more than one values for the same field, put them in
      square brakets, separated by comma and space

   -  Make sure each pair is on its own line

Requires YAML syntax to work

.. _importing-label:

Importing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _additionalFieldsInZ3950ResultSearch-label:

AdditionalFieldsInZ3950ResultSearch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Display the MARC field/subfields \_\_\_ in the 'Additional fields' column of Z39.50 search results (use comma as delimiter e.g.: "001, 082$ab, 090$ab").

Description:

-  This preference lets you define additional fields and subfields to display on the Z39.50 result list.

.. _aggressivematchonisbn-label:

AggressiveMatchOnISBN
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: don't

Asks: When matching on ISBN with the record import tool, \_\_\_ attempt
to match aggressively by trying all variations of the ISBNs in the
imported record as a phrase in the ISBN fields of already cataloged
records.

Values:

-  do

-  don't

Description:

-  This preference allows you to choose to alter the ISBN matching rule
   used when staging records for import to be more aggressive. This
   means that all text will be stripped from the ISBN field so that a
   pure number match is possible. If this preference is set to "Don't"
   then Koha will find a match only if the ISBN fields are identical.

.. _aggressivematchonissn-label:

AggressiveMatchOnISSN
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: don't

Asks: When matching on ISSN with the record import tool, \_\_\_ attempt
to match aggressively by trying all variations of the ISSNs in the imported
record as a phrase in the ISSN fields of already cataloged records.

.. _interface-label:

Interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _advancedmarceditor-label:

advancedMARCeditor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't display

Asks: \_\_\_ descriptions of fields and subfields in the MARC editor.

Description:

-  This preference determines whether or not MARC field names will be
   present when editing or creating MARC records.

Values:

-  Display

   |image20|

-  Don't display

   |image21|

.. _defaultclassificationsource-label:

DefaultClassificationSource
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Dewey Decimal System

Asks: Use \_\_\_ as the default classification source.

Values:

-  ANSCR (Sound Recordings)

-  Dewey Decimal Classification

-  Library of Congress Classification

-  Other/Generic Classification Scheme

-  SuDoc Classification (U.S. GPO)

-  Universal Decimal Classification

    **Note**

    Adding another classification under Administration > Classification Sources
    will make it show up in this list as well.

.. _defaultsaverecordfileid-label:

DefaultSaveRecordFileID
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: When saving in a MARC/MARCXML file in the advanced cataloging editor or
exporting from the detail page in the staff interface, use the \_\_\_ in the
file name.

Default: bibliographic record number

Values:

-  bibliographic record number

-  control number

Description:

-  This preference determines what is the default file name that is used when
   downloading a MARC record.

-  Choosing 'bibliographic record number' will result in a file name like
   bib-123456.mrc where 123456 is the biblionumber.

-  Choosing 'contol number' will result in a file name like record-123456.mrc
   where 123456 is the record control number (in MARC21, this is the 001 field).

.. _easyanalyticalrecords-label:

EasyAnalyticalRecords
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't Display

Asks: \_\_\_ easy ways to create analytical record relationships

Values:

-  Display

-  Don't Display

    **Important**

    If you decide to use this feature you'll want to make sure that your
    :ref:`UseControlNumber` preference is set to "Don't
    use" or else the "Show analytics" links in the staff client and the
    OPAC will be broken.

Description:

-  An analytic entry in a catalog is one that describes a part of a
   larger work that is also described in the catalog. In bibliographic
   cataloging, analytic entries may be made for chapters in books or
   special issues of articles in periodicals. In archival cataloging,
   analytic entries may be made for series or items within a collection.
   This feature in Koha allows for an easy way of linking analytic
   entries to the host records, and this system preference adds several
   new menu options to the staff cataloging detail pages to allow that
   to happen.

.. _enableadvancedcatalogingeditor-label:

EnableAdvancedCatalogingEditor
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Default: Don't enable

Asks: \_\_\_ the advanced cataloging editor.

Description:

-  This preference will allow you to choose between a basic editor and a
   advanced editor for cataloging.

    **Note**

    This feature does not currently include any support for
    UNIMARC or NORMARC fixed fields.

.. _record-structure-label:

Record Structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _alternateholdingsfield-and-alternateholdingsseparator-label:

AlternateHoldingsField and AlternateHoldingsSeparator
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Display MARC subfield \_\_\_ as holdings information for records
that do not have items, with the subfields separated by \_\_\_.

Description:

-  Sometimes libraries migrate to Koha with their holding info in the
   852 field (OCLC holdings information field) and choose not to
   transfer that information into the 952 (Koha holdings information
   field) because they don't plan on circulating those items. For those
   libraries or other libraries that have data in the 852 fields of
   their records that they want to display, these preferences let you
   choose to display holdings info from a field other than the 952
   field. The AlternateHoldingsField preference can contain multiple
   subfields to look in; for instance 852abhi would look in 852
   subfields a, b, h, and i.

-  With AlternateHoldingsField set to 852abhi and
   AlternateHoldingsSeparator set to a space the holdings would look
   like the following:

   |image22|

.. _autobarcode-label:

autoBarcode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: generated in the form <branchcode>yymm0001

Asks: Barcodes are \_\_\_

Values:

-  generated in the form <branchcode>yymm0001

-  generated in the form <year>-0001, <year>-0002

-  generated in the form 1, 2, 3

-  incremental EAN-13 barcodes

-  not generated automatically

Description:

-  This setting is for libraries wishing to generate barcodes from
   within Koha (as opposed to scanning in pre-printed barcodes or
   manually assigning them). The default behavior makes it so that when
   you click in the barcode field (952$p in MARC21) it will populate
   with the automatic barcode you have chosen. If you would rather it
   only enter an automatic barcode when you click on the plugin (the ...
   to the right of the field) you can change the plugin used for that
   field in the framework. Set the plugin for 952$p (if using MARC21 or
   equivalent field mapped to items.barcode in your local MARC format)
   for your frameworks to barcode\_manual.pl instead of barcode.pl.
   Learn more about editing frameworks under the :ref:`MARC Bibliographic
   Frameworks <marc-bibliographic-frameworks-label>` section of this manual.

.. _defaultcountryfield008-label:

DefaultCountryField008
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Empty defaults to xxu for United States

Asks: Fill in the default country code for field 008 Range 15-17 of MARC21 -
Place of publication, production, or execution. \_\_\_.

Description:

-  This preference will allow you to set the country code for your MARC21
   008 field by default. If this is left empty it will default to
   United States (xxu). See the `MARC Code List for
   Countries <http://www.loc.gov/marc/countries/countries_code.html>`__
   for additional values for this preference.

    **Note**

    This preference won't have any effect if your records are in
    UNIMARC.

.. _defaultlanguagefield008-label:

DefaultLanguageField008
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Empty defaults to eng

Asks: Fill in the default language for field 008 Range 35-37 of MARC21
records \_\_\_.

Description:

-  This preference will allow you to set the language for your MARC21
   008 field by default. If this is left empty it will default to
   English (eng). See the `MARC Code List for
   Languages <http://www.loc.gov/marc/languages/language_code.html>`__
   for additional values for this preference.

    **Note**

    This preference won't have any effect if your records are in
    UNIMARC.

.. _item-level_itypes-label:

item-level\_itypes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: specific item

Asks: Use the item type of the \_\_\_ as the authoritative item type
(for determining circulation and fines rules, etc).

Values:

-  biblio record

-  specific item

Description:

-  This preference determines whether the item type Koha uses for
   issuing rules will be an attribute of the bibliographic record or the
   item record. Most libraries refer to the item record for item types.
   It also determines if the item type icon appears on the OPAC search
   results. If you have the preference set to 'biblio record' then Koha
   displays the item type icon on the search results to the left of the
   result info.

   |image23|

.. _itemcallnumber-label:

itemcallnumber
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 082ab

Asks: Map the MARC subfield to an item's callnumber.

    **Note**

    This can contain multiple subfields to look in; for instance 082ab
    would look in 082 subfields a and b.

Description:

-  This setting determines which MARC field will be used to determine
   the call number that will be entered into item records automatically
   (952$o). The value is set by providing the MARC field code (050, 082,
   090, 852 are all common in MARC21) and the subfield codes without the
   delimiters ($a, $b would be ab).

-  The field can also contain several MARC fields in priority order.
   For example, 082ab,050ab,080ab,090ab will look in priority in 082ab, if
   082 is not filled in, it will look in 050ab, etc.

   **Important**
   When entering more than one MARC field, separate them with a comma, but do
   not put spaces after the commas.

Examples:

-  Dewey: 082ab or 092ab; LOC: 050ab or 090ab; from the item record:
   852hi

.. _marcfieldforcreatorid-label:

MarcFieldForCreatorId, MarcFieldForCreatorName, MarcFieldForModifierId, MarcFieldForModifierName
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Store record's creator borrowernumber in MARC subfield \_\_\_ and
record's creator name in MARC subfield \_\_\_ Store record's last modifier
borrowernumber in MARC subfield \_\_\_ and record's last modifier name in MARC
subfield \_\_\_ NOTE: Use a dollar sign between field and subfield like 123$a.

Description:

-  This preference allows you to define which MARC subfields to use to
   automatically save the details of the logged in user.  You can save details
   for the record creator and the most recent modifier.

.. _marcflavour-label:

marcflavour
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: MARC21

Asks: Interpret and store MARC records in the \_\_\_ format.

Values:

-  MARC21

   -  The standard style for the US, Canada, Australia, New Zealand,
      United Kingdom, Germany and other countries

-  UNIMARC

   -  The standard style used in France, Italy, Portugal, Russia, and
      other countries

-  NORMARC

   -  The standard style for Norway

Description:

-  This preference defines global MARC style (MARC21, UNIMARC or
   NORMARC) used for encoding.

    **Important**

    Changing the value of this preference will not convert your records
    from one MARC style to an other.

.. _marcorgcode-label:

MARCOrgCode
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: OSt

Asks: Fill in the MARC organization code \_\_\_ by default in new MARC21
records (leave blank to disable).

Description:

-  The MARC Organization Code is used to identify libraries with
   holdings of titles and more.

Learn more and find your library's MARC21 code on the `MARC Code list
for
Organizations <http://www.loc.gov/marc/organizations/orgshome.html>`__
or in Canada on the `Canadian Symbols
Directory <http://www.collectionscanada.gc.ca/illcandir-bin/illsear/l=0/c=1>`__.

    **Note**

    This preference won't have any effect if your records are in
    UNIMARC.

.. _newitemsdefaultlocation-label:

NewItemsDefaultLocation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: When items are created, give them the temporary location of \_\_\_
(should be a location code, or blank to disable).

Description:

-  This allows you to set a specific location for all new items.

-  Make sure to use location codes, from the 
   :ref:`LOC authorized values list<existing-values-label>`

-  You can use the :ref:`UpdateItemLocationOnCheckin` system preference along 
   with this one to update the location upon checkin

.. _prefillitem-label:

PrefillItem
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: the new item is not prefilled with last created item values.

Asks: When a new item is added \_\_\_

Values:

-  the new item is not prefilled with last created item values.

-  the new item is prefilled with last created item values.

Description:

-  This preference controls the behavior used when adding new items.
   Using the options here you can choose to have your next new item
   prefill with the values used in the last item was added to save time
   typing values or to have the item form appear completely blank. Using
   :ref:`SubfieldsToUseWhenPrefill` you can
   control specifically which fields are prefilled.

.. _subfieldstoallowforrestrictedbatchmod-label:

SubfieldsToAllowForRestrictedBatchmod
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Define a list of subfields for which editing is authorized when
`items\_batchmod\_restricted <#items_batchmod_restricted>`__ permission
is enabled, separated by spaces. \_\_\_

Examples:

-  UNIMARC: "995$f 995$h 995$j"

-  MARC21: "952$a 952$b 952$c"

Description:

-  This preference lets you define what fields can be edited via the
   :ref:`batch item modification tool <batch-item-modification-label>` if the
   items\_batchmod\_restricted permission is enabled.

       **Note**

       The FA framework is excluded from the permission. If the pref is
       empty, no fields are restricted.

.. _subfieldstoallowforrestrictedediting-label:

SubfieldsToAllowForRestrictedEditing
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Define a list of subfields for which editing is authorized when
edit\_items\_restricted permission is enabled, separated by spaces.
\_\_\_

Examples:

-  UNIMARC: "995$f 995$h 995$j"

-  MARC21: "952$a 952$b 952$c"

Description:

-  This preference lets you define what fields can be edited via
   cataloging if the
   `edit\_items\_restricted <#edit_items_restricted>`__ permission is
   enabled

       **Note**

       The Fast Add (FA) framework is excluded from the permission. If
       the pref is empty, no fields are restricted.

.. _subfieldstousewhenprefill-label:

SubfieldsToUseWhenPrefill
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Define a list of subfields to use when prefilling items \_\_\_

    **Important**

    Separate values with a space.

Description:

-  When the :ref:`PrefillItem` preference is set to prefill
   item values with those from the last added item, this preference can
   control which fields are prefilled (and which are not). Enter a space
   separated list of fields that you would like to prefill when adding a
   new item.

.. _unimarcfield100language-label:

UNIMARCField100Language
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: fre

Asks: Use the language (ISO 690-2) \_\_\_ as default language in the
UNIMARC field 100 when creating a new record or in the field plugin.

.. _z3950normalizeauthor-and-z3950authorauthfields-label:

z3950NormalizeAuthor and z3950AuthorAuthFields
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Defaults: Don't copy and 701,702,700

Asks: \_\_\_ authors from the UNIMARC \_\_\_ tags (separated by commas)
to the correct author tags when importing a record using Z39.50.

Description for z3950NormalizeAuthor:

-  This preference allows for 'Personal Name Authorities' to replace
   authors as the bibliographic authority. This preference should only
   be considered by libraries using UNIMARC.

Values for z3950NormalizeAuthor:

-  Copy

-  Don't copy

Description for z3950AuthorAuthFields:

-  This preference defines which MARC fields will be used for 'Personal
   Name Authorities' to replace authors as the bibliographic
   authorities. This preference only applies to those using UNIMARC
   encoding. The MARC fields selected here will only be used if
   'z3950NormalizeAuthor' is set to "Copy". The default field are 700,
   701, and 702.

.. _spine-labels-label:

Spine Labels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _spinelabelautoprint-label:

SpineLabelAutoPrint
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: don't

Asks: When using the quick spine label printer, \_\_\_ automatically pop
up a print dialog.

Values:

-  do

-  don't

.. _spinelabelformat-label:

SpineLabelFormat
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: <itemcallnumber><copynumber>

Asks: Include the following fields on a quick-printed spine label:
(Enter in columns from the biblio, biblioitems or items tables,
surrounded by < and >.)

.. _spinelabelshowprintonbibdetails-label:

SpineLabelShowPrintOnBibDetails
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't display

Asks: \_\_\_ buttons on the bib details page to print item spine labels.

Values:

-  Display

   |image24|

-  Don't display


