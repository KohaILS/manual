.. include:: images.rst

.. _accounting-system-preferences-label:

Accounting
-------------------------------------------------------------------------------

*Get there:* More > Administration > Global system preferences >
Acquisitions

.. _accounting-features-prefs-label:

Features
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _autocreditnumber-label:

AutoCreditNumber
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_

Default: Do not automatically generate credit numbers

Values:

-  Do not automatically generate credit numbers

-  Automatically generate credit numbers in the form <year>-0001

-  Automatically generate credit numbers in the form <branchcode>yyyymm0001

-  Automatically generate credit numbers in the form 1, 2, 3

Description:

-  For auditing purposes, it might be necessary to attach a unique number to each
   credit (payments, writeoffs, refunds, etc.). This system preference allows you 
   to choose the format of this unique number.

   **Important**

   Automatic generation also has to be enabled for each 
   :ref:`credit type <credit-types-label>`.

.. _enablepointofsale-label:

EnablePointOfSale
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ the point of sale feature to allow anonymous transactions with the 
accounting system.

Default: Disable

Values:

-  Disable

-  Enable

Description:

-  This system preference controls the :ref:`point of sale module <point-of-sale-label>`.

  **Important**

  If you enable this system preference, make sure to enable :ref:`UseCashRegisters` 
  as well.

.. _usecashregisters-label:

UseCashRegisters
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ cash registers with the accounting system to track payments.

Default: Don't use

Values:

-  Don't use

-  Use

Description:

-  This preference enables the :ref:`cash registers <cashregisters-label>`
   feature in the administration module.

.. _accounting-policy-label:

Policy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _accountautoreconcile-label:

AccountAutoReconcile
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ reconcile patron balances automatically on each transaction adding debits or credits.

Default: Do not

Values:

-  Do

-  Do not

Description:

-  This preference controls whether or not credits are automatically used to
   to reduce the owed amounts in a patron's account.

.. _finepaymentautopopup-label:

FinePaymentAutoPopup
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ automatically display a print dialog for a payment receipt when
making a payment.

Default: Don't

Values:

-  Do

-  Don't

Description:

-  If activated, when :ref:`making a payment <pay-and-writeoff-fines-label>` in
   a patron's account, a printing popup will be displayed automatically instead
   of having to click on the 'print' button.

.. _roundfinesatpayment-label:

RoundFinesAtPayment
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: \_\_\_ round fines to the nearest cent when collecting payments.

Default: Don't

Values:

-  Don't

-  Do

Description:

-  Enabling this preference allows paying fines of partial cents which may not 
   be visible in the interface.

