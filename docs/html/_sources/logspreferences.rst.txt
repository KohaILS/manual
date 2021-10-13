.. include:: images.rst

.. _logs-label:

Logs
----------------

Logs keep track of transaction on the system. You can decide which
actions you want to log and which you don't using these preferences.
Logs can then be viewed in the :ref:`Log Viewer` under Tools.

*Get there:* More > Administration > Global System Preferences > Logs

.. _debugging-label:

Debugging
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _dumpsearchquerytemplate-label:

DumpSearchQueryTemplate
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ dump search query as a template parameter.

Default: Don't

Value:

-  Don't

-  Do

Description:

-  This enhancement allows you to view the search query used by Zebra or 
   Elasticsearch, to help with troubleshooting.

-  Make sure to enable :ref:`DumpTemplateVarsIntranet` and/or 
   :ref:`DumpTemplateVarsOpac` otherwise this system preference will have no 
   effect.

-  The dumped query will be in the page source under 'search_query'.

.. _dumptemplatevarsintranet-label:

DumpTemplateVarsIntranet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't

Asks: \_\_\_ dump all Template Toolkit variable to a comment in the HTML
source for the staff intranet.

Value:

-  Don't

-  Do

.. _dumptemplatevarsopac-label:

DumpTemplateVarsOpac
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't

Asks: \_\_\_ dump all Template Toolkit variable to a comment in the HTML
source for the OPAC.

Value:

-  Don't

-  Do

.. _logging-label:

Logging
~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _authfailurelog-label:

AuthFailureLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ authentication failures

Default: Don't log

Values:

-  Don't log

-  Log

Description:

-  This system preference controls whether or not Koha should log when a patron 
   fails to successfully authenticate on the OPAC (or a staff member in the 
   staff interface).

.. _authoritieslog-label:

AuthoritiesLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't log

Asks: \_\_\_ changes to authority records.

Values:

-  Don't log

-  Log

.. _authsuccesslog-label:

AuthSuccessLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ successful authentications 

Default: Don't log

Values:

-  Don't log

-  Log

Description:

-  This system preference controls whether or not Koha should log when a patron 
   successfully authenticates on the OPAC (or a staff member in the staff 
   interface)

.. _borrowerslog-label:

BorrowersLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Log

Asks: \_\_\_ changes to patron records.

Values:

-  Don't log

-  Log

       **Note**

       Enabling this preference allows the tracking of cardnumber changes for patrons

.. _cataloguinglog-label:

CataloguingLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't log

Asks: \_\_\_ any changes to bibliographic or item records.

Values:

-  Don't log

-  Log

    **Important**

    Since this occurs whenever a book is cataloged, edited, or checked
    in or out it can be very resource intensive - slowing down your
    system.

.. _cronjoblog-label:

CronjobLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't log

Asks: \_\_\_ information from cron jobs.

Values:

-  Don't log

-  Log

.. _fineslog-label:

FinesLog
^^^^^^^^^^^^^^^^^^^^^^^^

Default: Log

Asks: \_\_\_ when overdue fines are charged or automatically forgiven.

Values:

-  Don't log

-  Log

.. _holdslog-label:

HoldsLog
^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't log

Asks: \_\_\_ any actions on holds (create, cancel, suspend, resume, etc.).

Values:

-  Don't log

-  Log

.. _issuelog-label:

IssueLog
^^^^^^^^^^^^^^^^^^^^^^^^

Default: Log

Asks: \_\_\_ when items are checked out.

Values:

-  Don't log

-  Log

.. _letterlog-label:

LetterLog
^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Log

Asks: \_\_\_ when an automatic claim notice is sent.

Values:

-  Don't log

-  Log

    **Note**

    This log tracks all notices that go to patrons including the overdue
    notices.

.. _renewallog-label:

RenewalLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default:  Don't log

Asks: \_\_\_ when items are renewed.

Values:

- Don't log

- Log

.. _reportslog-label:

ReportsLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Don't log

Asks: \_\_\_ when reports are added, deleted or changed.

Values:

-  Don't log

-  Log

.. _returnlog-label:

ReturnLog
^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Log

Asks: \_\_\_ when items are returned.

Values:

-  Don't log

-  Log

.. _subscriptionlog-label:

SubscriptionLog
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Default: Log

Asks: \_\_\_ when serials are added, deleted or changed.

Values:

-  Don't log

-  Log


