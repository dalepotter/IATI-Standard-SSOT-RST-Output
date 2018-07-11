repayment-type
==============

``iati-activities/iati-activity/crs-add/loan-terms/repayment-type``

This is the reference page for the XML element ``repayment-type``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: repayment-type

Definition
~~~~~~~~~~


The type of loan repayment


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/crs-add/loan-terms/repayment-type/.code:

@code
  An IATI codelist tabulating CRS-specified values for the type of Repayment.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`LoanRepaymentType codelist </codelists/LoanRepaymentType>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``repayment-type`` within ``loan-terms`` in context of ``crs-add`` element.

| The ``@code`` attribute declares a valid code (*1*) from the *LoanRepaymentType* codelist.

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.

1.03
^^^^

| New in 1.03
| Added the optional ``crs-add`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2237>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/loan-terms/repayment-type.rst>`_

