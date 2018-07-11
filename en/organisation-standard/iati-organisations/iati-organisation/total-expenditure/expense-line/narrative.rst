narrative
=========

``iati-organisations/iati-organisation/total-expenditure/expense-line/narrative``

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








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/total-expenditure/expense-line/narrative/.xml:lang:

@xml:lang
  A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
The ``narrative`` child element can be used to declare freetext for the ``expense-line`` element.

.. literalinclude:: ../../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--total-expenditure starts-->
	:end-before: <!--total-expenditure ends-->

| Note: The ``narrative`` element can be repeated for any language additional to the default language set in ``iati-organisation``, by using the ``@xml:lang`` attribute.  Example not shown.

Changelog
~~~~~~~~~
2.02
^^^^
The optional ``total-expenditure`` element was `added <http://support.iatistandard.org/entries/83404469-Add-Total-Expenditure-Element-To-Organisation-File>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L27>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/total-expenditure/expense-line/narrative.rst>`_

