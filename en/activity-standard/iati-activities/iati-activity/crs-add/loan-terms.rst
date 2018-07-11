loan-terms
==========

``iati-activities/iati-activity/crs-add/loan-terms``

This is the reference page for the XML element ``loan-terms``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: loan-terms

Definition
~~~~~~~~~~


Loan repayment terms and interest rates


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/crs-add/loan-terms/.rate-1:

@rate-1
  Interest Rate. If an ODA loan with variable interest rate, report the variable rate here and the reference fixed rate as rate-2
  
  Enter the rate without the percentage sign.


  This value must be of type xsd:decimal.



  
.. _iati-activities/iati-activity/crs-add/loan-terms/.rate-2:

@rate-2
  Second Interest Rate.  If an ODA loan with variable interest rate, report the variable rate as rate-1 and the reference fixed rate here
  
  Enter the rate without the percentage sign.


  This value must be of type xsd:decimal.



  



Example Usage
~~~~~~~~~~~~~
The ``loan-terms`` element acts as a container for other elements.

| Example usage of ``loan-terms`` in context of ``crs-add`` element.

| The ``@rate-1`` attribute  declares an example value of *4*.
| The ``@rate-2`` attribute declares an example value of *3*.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->


Changelog
~~~~~~~~~

1.03
^^^^
| New in 1.03
| Added the optional ``crs-add`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2229>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/loan-terms.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   loan-terms/repayment-type
   loan-terms/repayment-plan
   loan-terms/commitment-date
   loan-terms/repayment-first-date
   loan-terms/repayment-final-date

