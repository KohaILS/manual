.. include:: images.rst

.. _cash-management-label:

Cash management
===============================================================================

Koha includes a number of options for dealing with monetary transactions and 
actions to allow for fine grained tracking of these processes for audit and
analytic processes.

.. _cash-management-registers-label:

Cash registers
-------------------------------------------------------------------------------

Cash registers can be used to track transactions to a specific location in your
library. This can be especially helpful for detailing where cash has been taken
for payments and then when this cash is subsequently removed and taken to the 
bank.

Setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To enable the use of cash registers, you must turn on the :ref:`UseCashRegisters` 
system preference. 

You can then configure cash registers for your library from the 
:ref:`cash registers <cashregisters-label>` page in the administration module.

.. _cash-management-library-details-label:

Library details
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- *Get there:* Home > Tools > Cashup registers

A summary of transaction amounts associated to a libraries cash registers can 
be found under the 'Cashup registers' tool. The summary will list registers 
associated with your logged in branch alongside information about how much 
money should be found in each register, what is available to take to the bank
and a breakdown of income vs outgoings.

*Note:* You can also access this page from the left hand menu available on the
:ref:`Point of sale <point-of-sale-label>` page when that module is enabled.

.. _cash-management-register-details-label:

Register details
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- *Get there:* Home > Tools > Cashup registers > Register name

A list of all transactions to have taken place at a register is available by 
clicking on the cash register name from the 
:ref:`library details <cash-management-library-details-label>` page.

If you have the correct permissions, you can re-print receipts, issue refunds
and record :ref:`cashups <cash-management-register-cashup-label>` from this page.

.. _cash-management-register-cashup-label:

Cashup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The action of 'cashing up' can be recorded against a cash register from both 
the :ref:`library details <cash-management-library-details-label>` and 
:ref:`register details <cash-management-register-details-label>` pages.

Clicking the `Record cashup` button will simply record the date and time that
the action has taken place and is intended to allow the regular record of when 
money is collected from the cash register and taken to the bank.

Both of the above pages utilize the cashup record to limit the display of 
transactions/summaries to only pertinent information, since the last cashup.

Once a cashup has taken place, a summary of the transactions taken during that
cashup period is available for display, and printing, via the `Summary` link 
found next to the last cashup date on the register details page.

|image1515|

.. _point-of-sale-label:

Point of sale
-------------------------------------------------------------------------------

Point of sale is a module designed for selling items to people who are not 
registered at the library or to make sales that do not need to be linked to a 
patron account.

For example, you can sell used books or promotional items. These items can be 
sold to anyone and you don't need to link the sale to a particular patron.

For invoices that need to be linked to a patron's account (like a lost item or 
new card fee), use :ref:`manual invoicing <creating-manual-invoices-label>`.

-  *Get there:* More > Point of sale

.. _setup-point-of-sale-label:

Setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To enable the point of sale module, you must turn on the :ref:`EnablePointOfSale` 
system preference. 

If it's not already done, you must also enable the :ref:`UseCashRegisters` 
system preference.

Make sure you :ref:`configure your cash registers <cashregisters-label>` in the 
administration module.

Finally, you must add items that you will be selling in the :ref:`debit types 
<debit-types-label>` section of the administration module.

.. _making-a-sale-label:

Making a sale
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When you first go in the point of sale module, the left side will show all the 
items for sale. These are :ref:`debit types <debit-types-label>` that were
marked as 'Can be sold'.

     **Note**

     -  You can customize the columns of this table in the 
        :ref:`'Table settings'<column-settings-label>` section of the 
        Administration module (table id: invoices).

On the right side is the current sale.

|image1497|

Click on the 'Add' button next to the items to add to the current sale.

If you need to change the cost or the quantity, click on the amount on the 
right side and it will become an input box where you can enter the correct 
amount.

|image1459|
