reference
=========

``iati-activities/iati-activity/result/indicator/reference``

This is the reference page for the XML element ``reference``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: reference

Definition
~~~~~~~~~~


A standardised means of identifying the indicator from a code in a recognised vocabulary. Multiple vocabularies may be specified, but each vocabulary may be specified only once for each indicator.


Rules
~~~~~








This element may occur any number of times.







There must be no more than one element or attribute matched at ``reference[1]`` or ``../reference[1]``.




Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/reference/.vocabulary:

@vocabulary
  A code for a recognised vocabulary of indicators. The value for this field should appear in the IndicatorVocabulary codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`IndicatorVocabulary codelist </codelists/IndicatorVocabulary>`.



  
.. _iati-activities/iati-activity/result/indicator/reference/.code:

@code
  A code for an indicator defined in the specified vocabulary specified.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/result/indicator/reference/.indicator-uri:

@indicator-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  



Example Usage
~~~~~~~~~~~~~
Example of ``reference`` in the context of an ``indicator`` of a ``result`` element.

| This example declares use of ``@vocabulary`` *1*, with a ``@code`` of *3429*:

.. code-block:: xml

    <reference vocabulary="1" code="3429" />


If a publisher uses a vocabulary of 99 (i.e. 'Reporting Organisation'), then the ``@indicator-uri`` attribute should also be used, for example:

.. code-block:: xml

	<reference vocabulary="99" code="B1" indicator-uri="http://example.com/indicators.html" />


| The ``reference`` element can be repeated in any ``indicator``.  If the ``reference`` element is reported at indicator level it must not be reported at result level:

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-indicator starts-->
	:end-before: <!--result-indicator ends-->

Changelog
~~~~~~~~~

2.03
^^^^
Definition of ``@indicator-uri`` attribute `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.

The rule for using the ``reference`` element was `added <https://discuss.iatistandard.org/t/results-vocabulary-attribute-option-included-2-03/879>`__.

2.02
^^^^
The optional ``reference`` element was `added <http://support.iatistandard.org/entries/79784435-Results-Require-unambiguous-indicator-reference>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1741>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/reference.rst>`_

