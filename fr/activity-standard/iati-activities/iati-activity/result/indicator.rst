indicator
=========

``iati-activities/iati-activity/result/indicator``

This is the reference page for the XML element ``indicator``. 

.. index::
  single: indicator

Definition
~~~~~~~~~~


The indicator(s) that meet the results. There can be multiple indicators for each result.


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/.measure:

@measure
  An IATI code defining the unit of measure in which the value is reported.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`IndicatorMeasure codelist </codelists/IndicatorMeasure>`.



  
.. _iati-activities/iati-activity/result/indicator/.ascending:

@ascending
  A boolean describing the behaviour of the indicator.
  It is "true" if the indicator improves from small to large (e.g. clinics built); false if it improves from large to small (e.g. cases of a disease).


  This value must be of type xsd:boolean.



  
.. _iati-activities/iati-activity/result/indicator/.aggregation-status:

@aggregation-status
  Boolean flag indicating whether the data in the result set are suitable for aggregation.


  This value must be of type xsd:boolean.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1730>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/result/indicator.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   indicator/title
   indicator/description
   indicator/document-link
   indicator/reference
   indicator/baseline
   indicator/period

