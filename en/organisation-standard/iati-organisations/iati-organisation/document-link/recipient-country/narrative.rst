narrative
=========

``iati-organisations/iati-organisation/document-link/recipient-country/narrative``

This is the reference page for the XML element ``narrative``. 

.. index::
  single: narrative

Definition
~~~~~~~~~~


The free text name or description of the item being described. This can
be repeated in multiple languages.


Rules
~~~~~

The text in this element must be of type xsd:string.








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/document-link/recipient-country/narrative/.xml:lang:

@xml:lang
  A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
The ``narrative`` child element can be used to declare freetext for the ``recipient-country`` element.

| Note: Both the ``recipient-region`` and ``recipient-country`` elements still allow both a ``@code`` and descriptive text to be specified. This is to cover the isolated cases where the organisation publishing the data may not agree with name of a country or region given by the lookup codelists IATI uses.

.. code-block:: xml

	<recipient-country code="XK">
		<narrative>Kosovo (As per UNSCR 1244)<narrative>
	</recipient-country>

| Note: The ``narrative`` element can be repeated for any language additional to the default language set in ``iati-organisation``, by using the ``@xml:lang`` attribute.  Example not shown.

Changelog
~~~~~~~~~

2.01
^^^^
| The ``recipient-country`` element was introduced in 2.01.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L27>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/document-link/recipient-country/narrative.rst>`_

