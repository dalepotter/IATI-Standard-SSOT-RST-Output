recipient-country
=================

``iati-organisations/iati-organisation/document-link/recipient-country``

This is the reference page for the XML element ``recipient-country``. 

.. index::
  single: recipient-country

Definition
~~~~~~~~~~


The recipient country that is the focus of the document.
May be repeated for multiple countries.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/document-link/recipient-country/.code:

@code
  ISO 3166-1 alpha-2 code for the country.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`Country codelist </codelists/Country>`.



  



Example Usage
~~~~~~~~~~~~~
| Example usage of ``recipient-country`` of a ``document-link`` in an ``iati-organisation``.

| The ``@code`` attribute declares a valid code (*AF*) from the *Country* codelist.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--document-link starts-->
	:end-before: <!--document-link ends-->

| The ``recipient-country`` element can be repeated in any ``document-link``.
| Example declaring multiple ``recipient-country`` elements for the same ``document-link``:

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--multi-country-document-link starts-->
	:end-before: <!--multi-country-document-link ends-->


Changelog
~~~~~~~~~

2.01
^^^^
| The ``recipient-country`` element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#document-link-new-child-element>`__ as a child element of ``document-link``.



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L774>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/document-link/recipient-country.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-country/narrative

