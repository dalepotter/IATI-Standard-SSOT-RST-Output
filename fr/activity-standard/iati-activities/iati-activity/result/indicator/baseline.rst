baseline
========

``iati-activities/iati-activity/result/indicator/baseline``

This is the reference page for the XML element ``baseline``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1775>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/result/indicator/baseline.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   baseline/location
   baseline/dimension
   baseline/document-link
   baseline/comment

