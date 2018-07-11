result
======

``iati-activities/iati-activity/result``

This is the reference page for the XML element ``result``. 

.. index::
  single: result

Definition
~~~~~~~~~~


A container for reporting outputs, outcomes, impacts and other results that stem directly from the activity. This may be repeated for each type of result reported.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/.type:

@type
  An IATI code for the type of result being reported.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ResultType codelist </codelists/ResultType>`.



  
.. _iati-activities/iati-activity/result/.aggregation-status:

@aggregation-status
  Boolean flag indicating whether the data in the result set are suitable for aggregation.


  This value must be of type xsd:boolean.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1685>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/result.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   result/title
   result/description
   result/document-link
   result/reference
   result/indicator

