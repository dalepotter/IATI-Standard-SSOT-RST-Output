budget-line
===========

``iati-organisations/iati-organisation/total-budget/budget-line``

This is the reference page for the XML element ``budget-line``. 

.. index::
  single: budget-line

Definition
~~~~~~~~~~


A breakdown of the total budget into sub-totals. The
breakdown is determined by the reporting organisation
and described in the narrative. The period covered is
the same as that covered by the parent total-budget
element. The sum of budget-line values does not have to
equal the value given in the parent element.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/total-budget/budget-line/.ref:

@ref
  An internal reference for this budget line taken
  from the reporting organisation's own system.
  Optional.


  This value must be of type xsd:string.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L182>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/total-budget/budget-line.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   budget-line/value
   budget-line/narrative

