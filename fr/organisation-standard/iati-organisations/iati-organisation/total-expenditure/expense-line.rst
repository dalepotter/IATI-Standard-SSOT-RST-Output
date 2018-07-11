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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L700>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/total-expenditure/expense-line.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   expense-line/value
   expense-line/narrative

