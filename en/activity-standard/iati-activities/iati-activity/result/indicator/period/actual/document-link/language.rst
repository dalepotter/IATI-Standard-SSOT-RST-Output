language
========

``iati-activities/iati-activity/result/indicator/period/actual/document-link/language``

This is the reference page for the XML element ``language``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: language

Definition
~~~~~~~~~~


The ISO 639-1 language code in which target document is written, e.g. "en". Can be repeated to describe multi-lingual documents.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/actual/document-link/language/.code:

@code
  ISO 639-1 language code

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
| Example usage of ``language`` of a ``document-link`` in a ``actual`` in a ``period`` in a ``indicator`` in a ``result`` element.

| The ``@language`` attribute declares a valid code (*en*) from the *Language* codelist.
| Note: This specifies the language of the document being linked to.

.. literalinclude:: ../../../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-document-link example starts-->
	:end-before: <!--result-document-link example ends-->

| In some cases, a ``document-link`` may be in multiple languages.  This is expressed by repeating the ``language`` element.

Changelog
~~~~~~~~~

2.03
^^^^
The optional ``language`` element of a ``document-link`` in a ``actual`` in a ``period`` in a ``indicator`` in a ``result`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L217>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/language.rst>`_

