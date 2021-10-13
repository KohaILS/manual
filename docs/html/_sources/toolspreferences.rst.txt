.. include:: images.rst

.. _tools-system-preferences-label:

Tools
-------------------------------------------------------------------------------

*Get there:* More > Administration > Global System Preferences > Tools

.. _barcodes-label:

Barcodes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _barcodeseparators-label:

BarcodeSeparators
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Split barcodes on the following separator chars \_\_\_ in batch item
modification and inventory.

Default: \\s\\r\\n

Description:

-  When importing barcode files in the :ref:`inventory tool <inventory-tool-label>`
   or the :ref:`batch item modification tool <batch-item-modification-label>`
   you can decide which character separates each barcode.

.. Warning::

   You must use the regular expression codes for the characters.

   -  \\s is used for a whitespace

   -  \\r is used for a carriage return

   -  \\n is used for a new line

   -  \\t is used for a tab

   Make sure you escape the other characters you put in there by preceding
   them with a backslash

   -  \\. instead of a dot

   -  \\\\ instead of a backslash

   -  \\- instead of a hyphen

.. _batch-item-label:

Batch item
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These preferences are in reference to the 
:ref:`Batch item modification <batch-item-modification-label>` and 
:ref:`Batch item deletion <batch-item-deletion-label>` tools.

.. _maxitemstodisplayforbatchdel-label:

MaxItemsToDisplayForBatchDel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Display up to \_\_\_ items in a single item deletion batch.

Default: 1000

Description:

-  In the :ref:`batch item delete tool <batch-item-deletion-label>` this will
   prevent the display of more than the items you entered in this
   preference, but you will be able to delete more than the number you
   enter here.

.. Note::

   Displaying a large number of items may slow down the display.

.. _maxitemstodisplayforbatchmod-label:

MaxItemsToDisplayForBatchMod
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Display up to \_\_\_ items in a single item modification batch.

Default: 1000

Description:

-  In the :ref:`batch item modification tool <batch-item-modification-label>`
   this will prevent the display of more than the items you entered in this
   preference, but you will be able to modify more than the number you
   enter here (see :ref:`MaxItemsToProcessForBatchMod`).

.. Note::

   Displaying a large number of items may slow down the display.

.. _maxitemsforbatchmod-label:

MaxItemsToProcessForBatchMod
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Process up to \_\_\_ items in a single modification batch.

Default: 1000

Description:

-  In the :ref:`batch item modification tool <batch-item-modification-label>` 
   this preference will prevent the editing of more than the number entered 
   here.

.. Note::

   Processing a large number of items may slow down the process and it may 
   even time out.

.. _news-system-preferences-label:

News
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _additionalcontentseditor-label:

AdditionalContentsEditor
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: By default edit additional contents and news items with

Default: a WYSIWYG editor (TinyMCE)

Values:

-  a text editor (CodeMirror)

-  a WYSIWYG editor (TinyMCE)

Description:

-  This system preference allows you to choose which editor to use in the 
   :ref:`news tool <news-label>` and the 
   :ref:`additional contents tool <additional-contents-label>`.

-  A text editor will let you write HTML directly. Use this if you want more 
   control over how your content will be displayed. 

.. Note::

   You can use CSS id's and classes in your HTML and format them with the 
   :ref:`OPACUserCSS` or :ref:`IntranetUserCSS` system preferences.

-  A WYSIWYG (what you see is what you get) editor is a user-friendly editor 
   with functions similar to word processing software. Use this if you are 
   unfamiliar with HTML.

.. _newsauthordisplay-label:

NewsAuthorDisplay
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Show the author for news items: \_\_\_

Default: not at all

Values:

-  Both OPAC and staff interface

-  Not at all

-  OPAC only

-  Staff interface only

Description:

-  This system preference lets you choose whether or not the name of the author 
   of the news item is displayed and where.

.. _patron-cards-label:

Patron Cards
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These preferences are in reference to the 
:ref:`Patron card creator <patron-card-creator-label>` tool.

.. _imagelimit-label:

ImageLimit
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Limit the number of creator images stored in the database to
\_\_\_ images.

Default: 5

Description: 

-  This system preference determines the number of images that can be used in 
   the :ref:`patron card creator tool <patron-card-creator-label>`.

.. Note::

   A large number of images may take a lot of storage space.

.. _reports-system-preferences-label:

Reports
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These preferences are in reference to the :ref:`reports module <reports-label>`.

.. _numsavedreports-label:

NumSavedReports
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: By default, show \_\_\_ reports on the saved reports page.

Default: 20

Description:

-  This system preference lets you determine the number of reports that should 
   de displayed per page in the saved reports page.

.. Note::

   Displaying a large number of reports may slow down the display.

.. _upload-system-preferences-label:

Upload
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. _uploadpurgetemporaryfilesdays-label:

UploadPurgeTemporaryFilesDays
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Asks: Automatically delete temporary uploads older than \_\_\_ days in
cleanup\_database cron job.

Default: blank

Description: 

-  This system preference lets you determine how long temporary uploaded files 
   (files uploaded through the :ref:`upload tool <upload-label>` without any 
   category) are kept

.. Note::

   If you leave this field empty, the cron job will not delete any files.

   On the other hand, a value of 0 means 'delete all temporary files'. 

-  This value can be overridden with the --temp-uploads-days option of the 
   cleanup\_database script.