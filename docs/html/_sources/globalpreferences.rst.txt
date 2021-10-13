.. include:: images.rst

.. _global-system-preferences-label:

Global system preferences
=========================

Global system preferences control the way your Koha system works in
general. Set these preferences before anything else in Koha.

-  *Get there:* More > Administration > Global System Preferences

|image0|

System preferences can be searched (using any part of the preference
name or description) using the search box on the 'Administration' page
or the search box at the top of each system preferences page.

|image1|

When editing preferences a ^(modified)^ tag will appear next to items
you change until you click the 'Save All' button:

|image2|

After saving your preferences you'll get a confirmation message telling
you what preferences were saved:

|image3|

Each section of preferences can be sorted alphabetically by clicking the
small down arrow to the right of the word 'Preference' in the header
column

|image4|

If the preference refers to monetary values (like
:ref:`maxoutstanding`) the currency displayed will be the
default you set in your :ref:`Currencies and Exchange Rates`
administration area. In the examples to
follow they will all read USD for U.S. Dollars.

    **Important**

    For libraries systems with unique URLs for each site the system
    preference can be overridden by editing your koha-http.conf file
    this has to be done by a system administrator or someone with access
    to your system files. For example if all libraries but one want to
    have search terms highlighted in results you set the
    OpacHighlightedWords preference to 'Highlight' then edit the
    koha-http.conf for the library that wants this turned off by adding
    'SetEnv OVERRIDE\_SYSPREF\_OpacHighlightedWords "0"'. After
    restarting the web server that one library will no longer see
    highlighted terms. Consult with your system administrator for more
    information.

.. toctree::
    :maxdepth: 2
    :hidden:
    :glob:

    *preferences
