reference
=========

``iati-activities/iati-activity/result/reference``

This is the reference page for the XML element ``reference``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: reference

Definition
~~~~~~~~~~


A reference element to allow for the coded identification of a results framework.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/reference/.code:

@code
  A code from the codelist identified in vocabulary that identifies a results framework.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/result/reference/.vocabulary:

@vocabulary
  A code for the results framework vocabulary. The code must be a valid value in the ResultVocabulary codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ResultVocabulary codelist </codelists/ResultVocabulary>`.



  
.. _iati-activities/iati-activity/result/reference/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  



Example Usage
~~~~~~~~~~~~~
Example of ``reference`` in the context of a ``result`` element.

| This example declares use of ``@vocabulary`` *99*, with a ``@code`` of *B1*.  The ``@vocabulary-uri`` attribute should also be used:

.. code-block:: xml

    <reference vocabulary="99" code="B1" vocabulary-uri="http://example.com/indicators.html" />

| The ``reference`` element can be repeated in any ``result``. If the ``reference`` element is reported at result level it must not be reported at indicator level:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-reference starts-->
	:end-before: <!--result-reference ends-->

Changelog
~~~~~~~~~

2.03
^^^^
The optional ``reference`` element was `added <https://discuss.iatistandard.org/t/results-vocabulary-attribute-option-included-2-03/879>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1696>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/reference.rst>`_

