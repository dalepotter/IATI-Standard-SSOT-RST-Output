legacy-data
===========

``iati-activities/iati-activity/legacy-data``

This is the reference page for the XML element ``legacy-data``. 

.. index::
  single: legacy-data

Definition
~~~~~~~~~~


The legacy data element allows for the reporting of values held in a field in the reporting organisation's system which is similar, but not identical to an IATI element.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/legacy-data/.name:

@name
  The original field name in the reporting organisation's system

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/legacy-data/.value:

@value
  The original field value in the reporting organisation's system

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/legacy-data/.iati-equivalent:

@iati-equivalent
  The name of the equivalent IATI element.


  This value must be of type xsd:NMTOKEN.



  



Example Usage
~~~~~~~~~~~~~
Example ``legacy-data`` of an ``iati-activity``.

| This example declares two non-IATI values for ``activity-status`` and ``transaction``.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--legacy-data starts-->
	:end-before: <!--legacy-data ends-->


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1651>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/legacy-data.rst>`_

