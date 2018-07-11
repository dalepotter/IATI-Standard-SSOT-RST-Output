narrative
=========

``iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative``

This is the reference page for the XML element ``narrative``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: narrative

Definition
~~~~~~~~~~


The free text name or description of the item being described. This can
be repeated in multiple languages.


Rules
~~~~~

The text in this element must be of type xsd:string.








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative/.xml:lang:

@xml:lang
  A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
The ``narrative`` child element can be used to declare freetext for the ``title`` element.

.. literalinclude:: ../../../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-document-link example starts-->
	:end-before: <!--result-document-link example ends-->

| The ``narrative`` element can be repeated for any language additional to the default language set in ``iati-organisation``, by using the ``@xml:lang`` attribute.

| Note: This relates to the language of the text in the XML.

Changelog
~~~~~~~~~

2.03
^^^^
| This mandatory ``narrative`` element of a ``title`` in a ``document-link`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L27>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/baseline/document-link/title/narrative.rst>`_

