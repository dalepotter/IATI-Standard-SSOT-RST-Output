target
======

``iati-activities/iati-activity/result/indicator/period/target``

This is the reference page for the XML element ``target``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: target

Definition
~~~~~~~~~~


The target milestone for this period


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/target/.value:

@value
  The target value.
  
  This should be a numeric value if the measure is quantitative.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``target`` within ``period``, in context of an ``indicator`` in a ``result`` element.

| The ``@value`` attribute declares an example value of *11*

.. literalinclude:: ../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-period starts-->
	:end-before: <!--result-period ends-->

Changelog
~~~~~~~~~

2.03
^^^^

The ``target`` element of a ``period`` in a ``indicator`` in a ``result`` element can be reported multiple times `added <https://discuss.iatistandard.org/t/results-allow-disaggregations-of-results-data-included-2-03/871>`__.

The attribute ``@value`` was made optional and rules for its use `added <https://discuss.iatistandard.org/t/results-represent-more-than-quantitative-data-included-2-03/872>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1845>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/target.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   target/location
   target/dimension
   target/comment
   target/document-link

