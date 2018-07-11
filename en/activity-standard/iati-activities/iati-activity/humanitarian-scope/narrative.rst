narrative
=========

``iati-activities/iati-activity/humanitarian-scope/narrative``

This is the reference page for the XML element ``narrative``. 

.. index::
  single: narrative

Definition
~~~~~~~~~~


The description of the code specified.


Rules
~~~~~

The text in this element must be of type xsd:string.








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/humanitarian-scope/narrative/.xml:lang:

@xml:lang
  A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
The ``narrative`` child element can be used to declare freetext for the ``humanitarian-scope`` element.

| The ``narrative`` element should be used only when the *99* (*Reporting Organisation*) *HumanitarianScopeVocabulary* is declared.

.. code-block:: xml

	<humanitarian-scope type="1" vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="5">
	  <narrative>Nepal Earthquake (April 2015)</narrative>
	</humanitarian-scope>

| The ``narrative`` element can be repeated for any language additional to the default language set in ``iati-activity``, by using the ``@xml:lang`` attribute.  Example not shown.

Changelog
~~~~~~~~~

2.02
^^^^
| The ``humanitarian-scope`` and ``narrative`` elements were introduced in 2.02.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L27>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/humanitarian-scope/narrative.rst>`_

