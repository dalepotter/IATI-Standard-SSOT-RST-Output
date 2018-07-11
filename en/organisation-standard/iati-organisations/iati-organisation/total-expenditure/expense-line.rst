expense-line
============

``iati-organisations/iati-organisation/total-expenditure/expense-line``

This is the reference page for the XML element ``expense-line``. 

.. index::
  single: expense-line

Definition
~~~~~~~~~~


A breakdown of the total expenditure into sub-totals.
The breakdown is determined by the reporting
organisation and described in the narrative. The period
covered is the same as that covered by the parent
total-expenditure element. The sum of expenditure-line
values does not have to equal the value given in the
parent element.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/total-expenditure/expense-line/.ref:

@ref
  An internal reference for this expenditure line taken
  from the reporting organisation’s own system. Optional.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example ``expense-line`` for ``total-expenditure`` of an ``iati-organisation``.

| An example ``@ref`` attribute is included.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--total-expenditure starts-->
	:end-before: <!--total-expenditure ends-->

| The ``expense-line`` element can be repeated in any ``total-expenditure``.


Changelog
~~~~~~~~~
2.02
^^^^
The optional ``total-expenditure`` element was `added <http://support.iatistandard.org/entries/83404469-Add-Total-Expenditure-Element-To-Organisation-File>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L700>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/total-expenditure/expense-line.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   expense-line/value
   expense-line/narrative

