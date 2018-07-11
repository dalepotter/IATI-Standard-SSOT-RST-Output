period
======

``iati-activities/iati-activity/result/indicator/period``

This is the reference page for the XML element ``period``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: period

Definition
~~~~~~~~~~


The period covered for the results reported. Multiple periods can be reported for a single indicator.


Rules
~~~~~








This element may occur any number of times.








Example Usage
~~~~~~~~~~~~~
Example usage of ``period`` in context of an ``indicator`` in a ``result`` element.

| This element is a parent for other child elements.

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-indicator starts-->
	:end-before: <!--result-indicator ends-->


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1809>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   period/period-start
   period/period-end
   period/target
   period/actual

