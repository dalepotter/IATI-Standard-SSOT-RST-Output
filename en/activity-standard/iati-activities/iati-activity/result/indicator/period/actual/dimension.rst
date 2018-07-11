dimension
=========

``iati-activities/iati-activity/result/indicator/period/actual/dimension``

This is the reference page for the XML element ``dimension``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: dimension

Definition
~~~~~~~~~~


A category used for disaggregating the result by gender, age, etc.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/actual/dimension/.name:

@name
  Freetext description of a category being disaggregated.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/result/indicator/period/actual/dimension/.value:

@value
  Description of the value being disaggregated.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example of ``dimension`` in context of an ``actual`` element (as part of a parent ``result``/``indicator`` element).

| This example declares ``@name`` as *sex*, with a ``@value`` of *female*:

.. code-block:: xml

    <dimension name="sex" value="female" />


| The ``dimension`` element can be repeated within any ``actual`` element:

.. literalinclude:: ../../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-period starts-->
	:end-before: <!--result-period ends-->

Changelog
~~~~~~~~~

2.02
^^^^
The optional ``dimension`` element was `added <http://support.iatistandard.org/entries/79499149-Support-disaggregation-of-performance-data>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2541>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/dimension.rst>`_

