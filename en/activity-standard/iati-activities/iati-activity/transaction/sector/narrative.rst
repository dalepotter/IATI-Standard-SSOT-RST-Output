narrative
=========

``iati-activities/iati-activity/transaction/sector/narrative``

This is the reference page for the XML element ``narrative``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: narrative

Definition
~~~~~~~~~~


The free text description of the reporting organisation's own sector definition. This can be repeated in multiple languages


Rules
~~~~~

The text in this element must be of type xsd:string.








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/sector/narrative/.xml:lang:

@xml:lang
  A code specifying the language of text in this element. It is recommended that wherever possible only codes from ISO 639-1 are used. If not present, the default language is assumed.

  This value must be on the :doc:`Language codelist </codelists/Language>`.



  



Example Usage
~~~~~~~~~~~~~
The ``narrative`` child element can be used to declare freetext for the ``sector`` element of a ``transaction``.

| The ``narrative`` element should be used specially when the *99* (Reporting Organisation) or *98* (Reporting Organisation 2) *SectorVocabulary* are declared.

.. code-block:: xml

	<sector vocabulary="99" code="1">
		<narrative>Health Sector</narrative>
	</sector>

| The ``narrative`` element can be repeated for any language additional to the default language set in ``iati-activity``, by using the ``@xml:lang`` attribute.  Example not shown.


Changelog
~~~~~~~~~

2.01
^^^^
The ``sector`` element was added to ``transaction`` in 2.01


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L27>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/sector/narrative.rst>`_

