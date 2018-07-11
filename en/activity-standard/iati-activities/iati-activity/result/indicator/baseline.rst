baseline
========

``iati-activities/iati-activity/result/indicator/baseline``

This is the reference page for the XML element ``baseline``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: baseline

Definition
~~~~~~~~~~


The baseline value for the indicator


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/baseline/.iso-date:

@iso-date
  


  This value must be of type xsd:date.



  
.. _iati-activities/iati-activity/result/indicator/baseline/.year:

@year
  The year the baseline value was taken (yyyy)

  This attribute is required.



  This value must be of type xsd:positiveInteger.



  
.. _iati-activities/iati-activity/result/indicator/baseline/.value:

@value
  The baseline value.
  
  This should be a numeric value if the measure is quantitative.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example of ``baseline`` in context of an ``indicator`` in a ``result`` element.

| This example declares ``@year`` as *2012*, ``@iso-date`` as *2012-01-01*,with a ``@value`` of *10*:

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-indicator starts-->
	:end-before: <!--result-indicator ends-->

Changelog
~~~~~~~~~

2.03
^^^^

The occurance rules of the ``baseline`` element were amended so that `it can be reported multiple times <https://discuss.iatistandard.org/t/results-improve-consistency-of-results-standard-included-2-03/874>`__.

The attribute ``@iso-date`` was `added <https://discuss.iatistandard.org/t/results-improve-consistency-of-results-standard-included-2-03/874>`__.

The attribute ``@value`` was made optional and rules for its use `added <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1775>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/baseline.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   baseline/location
   baseline/dimension
   baseline/document-link
   baseline/comment

