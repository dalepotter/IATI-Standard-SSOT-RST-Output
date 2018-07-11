category
========

``iati-organisations/iati-organisation/document-link/category``

This is the reference page for the XML element ``category``. 

.. index::
  single: category

Definition
~~~~~~~~~~


IATI Document Category Code


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/document-link/category/.code:

@code
  An IATI code defining the category of the document.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`DocumentCategory codelist </codelists/DocumentCategory>`.



  



Example Usage
~~~~~~~~~~~~~
| Example  usage of ``category`` of a ``document-link`` in an ``iati-organisation``.

| This examples declares the ``DocumentCategory`` code *B01*, using the ``@code`` attribute.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--document-link starts-->
	:end-before: <!--document-link ends-->

| The ``category`` element can be repeated in any ``document-link``.
| Example declaring multiple ``DocumentCategory`` codes for the same ``document-link``:

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--multi-cat-document-link starts-->
	:end-before: <!--multi-cat-document-link ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L197>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/document-link/category.rst>`_

