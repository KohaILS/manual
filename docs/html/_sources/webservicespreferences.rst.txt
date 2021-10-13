.. include:: images.rst

.. _web-services-system-preferences-label:

Web services
-----------------------------------

*Get there:* More > Administration > Global system preferences > Web
services

.. _webservices-general-system-preferences-label:

General
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _accesscontrolalloworigin-label:

AccessControlAllowOrigin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Set the Access-Control-Allow-Origin header to \_\_\_

Description:

-  This is the header used for OPAC reports SVC routes.

.. _webservices-ils-di-system-preferences-label:

ILS-DI
~~~~~~~~~~~~~~~~~~~~~~~~

.. _ils-di-system-preference-label:

ILS-DI
^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ ILS-DI services for OPAC users

Values:

-  Disable

-  Enable

.. _ils-di-authorizedips-label:

ILS-DI:AuthorizedIPs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Allow IP addresses \_\_\_ to use the ILS-DI services (when enabled).

    **Note**

    Separate the IP addresses with commas and without spaces.
    For example: 15.78.193.62,197.85.10.1

    **Important**

    Leave the field blank to allow any IP address.

.. _idref-pref-label:

IdRef
~~~~~~~~~~~~~~~~~~~~~~~

.. _idref-label:

IdRef
^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ the IdRef webservice from the opac detail page. IdRef
allows to request authorities from the Sudoc database.

Values:

-  Disable

-  Enable

Description:

-  IdRef is a French service for Sudoc autorities. Using the `Sudoc
   database <http://www.sudoc.abes.fr/>`__, it allows to request /
   modify / add authorities. If a record comes from the Sudoc (so 009 is
   filled with an integer), at the OPAC you will see "Author: Idref" if
   a 7..$3 (unimarc author) if filled with a ppn. On clicking on the
   Idref link, a popup will display.

    |image1201|

   The Idref webservice is requested and all records (by roles) for this
   author will be displayed

   |image1202|

   There is 1 line / record and 2 links at the end. 1 will request Koha
   (cgi-bin/koha/opac-search.pl?q=ident:003381862), the other one will
   redirect to the sudoc page (http://www.sudoc.fr/003381862).

-  **Important**

       Please note that this feature is available only for libraries
       using UNIMARC.

-  **Note**

       The French Sudoc database should not be confused with the US
       Superintendent of Documents (SuDocs) Classification Scheme.

.. _mana-prefs-label:

Mana KB
~~~~~~~~~~~~~~~~~~~~~~~~

.. _autosharewithmana-label:

AutoShareWithMana
^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Fields automatically shared with Mana KB \_\_\_

Default: none

Values:

-  [Select all]

-  Subscriptions

Description:

-  This preference reflects the choice made in the :ref:`Mana KB configuration <share-with-mana-kb-label>` in the administration module.

-  Choosing to automatically share content with Mana KB means that every time you
   create that type of content, it will be automatically copied in the Mana KB
   repository, and it will be instantly available for other libraries to copy.

-  All content shared with Mana KB is shared under the CC0 license, meaning
   that there is no (zero) copyright. Anyone using Mana KB can copy, reuse
   and change (their copy of) your content. Read more on CC0 on the `Creative
   Commons Website <https://creativecommons.org/choose/zero/>`__. This will in
   no way change your data in your Koha installation.

.. _mana-pref-label:

Mana
^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ submissions to Mana KB.

Default: No, let me think about it

Values:

-  Disable

-  Enable

-  No, let me think about it

Description:

-  This preference reflects the choice made in the :ref:`Mana KB configuration <share-with-mana-kb-label>` in the administration module.

.. _mana-token-label:

ManaToken
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Security token used to authenticate on Mana KB: \_\_\_

Default: empty

Description:

-  This preference will be automatically populated with your unique Mana Token when
   you register for one on the :ref:`Mana KB configuration <share-with-mana-kb-label>`
   in the administration module.

-  The Mana Token is unique and associated with your Koha installation. It is used
   by Koha to log onto the Mana KB server and prevents intrusions on said server.

.. _oai-pmh-system-preferences-label:

OAI-PMH
~~~~~~~~~~~~~~~~~~~~~~~

.. _oai-pmh-pref-label:

OAI-PMH
^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ Koha's OAI-PMH server.

Values:

-  Disable

-  Enable

Description:

-  Once enabled you can visit http://YOURKOHACATALOG/cgi-bin/koha/oai.pl
   to see your file. For the Open Archives Initiative-Protocol for
   Metadata Harvesting (OAI-PMH) there are two groups of 'participants':
   Data Providers and Service Providers. Data Providers (open archives,
   repositories) provide free access to metadata, and may, but do not
   necessarily, offer free access to full texts or other resources.
   OAI-PMH provides an easy to implement, low barrier solution for Data
   Providers. Service Providers use the OAI interfaces of the Data
   Providers to harvest and store metadata. Note that this means that
   there are no live search requests to the Data Providers; rather,
   services are based on the harvested data via OAI-PMH. Koha at present
   can only act as a Data Provider. It can not harvest from other
   repositories. The biggest stumbling block to having Koha harvest from
   other repositories is that MARC is the only metadata format that Koha
   indexes natively. Visit
   http://www.oaforum.org/tutorial/english/page3.htm for diagrams of how
   OAI-PMH works.

Learn more about OAI-PMH at: http://www.openarchives.org/pmh/

.. _oai-pmh-archiveid-label:

OAI-PMH:archiveID
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: KOHA-OAI-TEST

Asks: Identify records at this site with the prefix \_\_\_ :

.. _oai-pmh-autoupdatesets-label:

OAI-PMH:AutoUpdateSets
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ automatic update of OAI-PMH sets when a bibliographic
record is created or updated.

Values:

-  Disable

-  Enable

.. _oai-pmh-autoupdatesetsembeditemdata-label:

OAI-PMH:AutoUpdateSetsEmbedItemData
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Disable

Asks: \_\_\_ embedding of item data when automatically updating OAI-PMH sets.
NOTE: This needs :ref:`OAI-PMH:AutoUpdateSets` syspref to be enabled.

Values:

-  Disable

-  Enable

.. _oai-pmh-conffile-label:

OAI-PMH:ConfFile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If this preference is left empty, Koha's OAI Server operates in normal
mode, otherwise it operates in extended mode. In extended mode, it's
possible to parameter other formats than marcxml or Dublin Core.
OAI-PMH:ConfFile specify a YAML configuration file which list available
metadata formats and XSL file used to create them from marcxml records.

For more information, see the :ref:`sample conf file <sample-oai-conf-file-label>`
section.

.. _oai-pmh-deletedrecord-label:

OAI-PMH:DeletedRecord
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: will never be emptied or truncated (persistent)

Asks: Koha's deletedbiblio table \_\_\_

Values:

-  will never have any data in it (no)

-  will never be emptied or truncated (persistent)

-  might be emptied or truncated at some point (transient)

.. _oai-pmh-maxcount-label:

OAI-PMH:MaxCount
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 50

Asks: Only return \_\_\_ records at a time in response to a ListRecords
or ListIdentifiers query.

Description:

-  This is the maximum number of records that would be returned based on
   ListRecord or ListIdentifier queries from harvesters. ListRecords
   harvest the entire records while the ListIdentifier is an abbreviated
   form of ListRecords, retrieving only headers rather than records.

.. _rest-api-prefs-label:

REST API
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _restbasicauth-label:

RESTBasicAuth
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ Basic authentication for the REST API.

Default: Disable

Values:

-  Disable

-  Enable

Description:

-  If enabled, Basic authentication is enabled for the REST API.

.. _restdefaultpagesize-label:

RESTdefaultPageSize
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Set the default number of results returned by the REST API endpoints
to \_\_\_ per page.

Default: 20

Description:

-  This preference lets you choose the number of endpoint results per page

.. _restoauth2clientcredentials-label:

RESTOAuth2ClientCredentials
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the OAuth2 client credentials grant for the REST API.

Default: Disable

Values:

-  Disable

-  Enable

Description:

-  If enabled, the OAuth2 client credentials flow is enabled for the REST API.

    **Note**

    Requires Net::OAuth2::AuthorizationServer installed.

    **Important**

    This system preference is experimental.

.. _restpublicanonymousrequests-label:

RESTPublicAnonymousRequests
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ anonymous access to public routes (that don't require 
authenticated access)

Default: Enable

Values:

-  Disable

-  Enable

Description:

-  If enabled, the API will allow anonymous access to public routes that don't 
   require authenticated access.

.. _restpublicapi-label:

RESTPublicAPI
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the \/public namespace of the API.

Default: Enable

Values: 

-  Disable

-  Enable

Description:

-  If enabled, the REST API will expose the \/public endpoints.

.. _reporting-label:

Reporting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _svcmaxreportrows-label:

SvcMaxReportRows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: 10

Asks: Only return \_\_\_ rows of a report requested via the reports web
service.

Description:

-  This value will be used to limit the number of results returned by
   `public reports <#publicreport>`__.
