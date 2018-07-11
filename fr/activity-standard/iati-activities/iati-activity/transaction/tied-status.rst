tied-status
===========

``iati-activities/iati-activity/transaction/tied-status``

This is the reference page for the XML element ``tied-status``. 

.. index::
  single: tied-status

Definition
~~~~~~~~~~


Optional element to override the top-level default-tied-status element on a transaction-by-transaction basis if needed.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/tied-status/.code:

@code
  An IATI code interpreting the usage of Columns 36-38 of the CRS++ reporting format. (Amount tied, Amount partially untied, Amount tied)

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`TiedStatus codelist </codelists/TiedStatus>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1281>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction/tied-status.rst>`_

