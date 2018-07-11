sector
======

``iati-activities/iati-activity/transaction/sector``

This is the reference page for the XML element ``sector``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: sector

Definition
~~~~~~~~~~


A recognised code, from a recognised vocabulary, classifying the purpose of this transaction.

If this element is used then ALL transaction elements should contain a transaction/sector element and iati-activity/sector should NOT be used.

This element can be used multiple times, but only one sector can be reported per vocabulary.


Rules
~~~~~








This element may occur any number of times.







Either ``transaction/sector`` or ``sector`` must be present.




Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/sector/.vocabulary:

@vocabulary
  An IATI code for the vocabulary (codelist) used for sector classifications. If omitted, OECD DAC 5-digit Purpose Codes are assumed.
  
  It is recommended that OECD DAC 5-digit Purpose Codes are used wherever possible. It is also recommended that if a publisher has its own classification system or systems, then the vocabularies 99 or 98 (Reporting Organisation's own vocabularies) should be used in addition to the DAC codes.
  
  Note that at transaction level, only one sector per vocabulary can be reported.


  This value must be of type xsd:string.


  This value must be on the :doc:`SectorVocabulary codelist </codelists/SectorVocabulary>`.



  
.. _iati-activities/iati-activity/transaction/sector/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 or 98 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/transaction/sector/.code:

@code
  The code for the sector.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Sector codelist </codelists/Sector>`, if the relevant vocabulary is used.



  



Example Usage
~~~~~~~~~~~~~
Example ``sector`` of a ``transaction`` within an ``iati-activity``.

| The ``@vocabulary`` attribute declares a valid code (*2*) from the *SectorVocabulary* codelist.
| An example value *111* from this vocabulary is declared with the ``@code`` attribute.

.. code-block:: xml

	<sector vocabulary="2" code="111" />

| The ``sector`` element can be repeated in any ``transaction``.

| The ``vocabulary`` is used to declare which ``SectorVocabulary`` classification list is in use. If this is omitted, then IATI assumes a *SectorVocabulary* of *1* (OECD DAC CRS Purpose Codes (5 digit)).

| If a vocabulary is not on the *SectorVocabulary* codelist, then the value of *99* or *98* (Reporting Organisation) should be declared.

| If a publisher uses a vocabulary of 98 or 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:

.. code-block:: xml

    <sector vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="A1" />

Full example:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.03
^^^^
The definition of the ``@vocabulary-uri`` was `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.

2.02
^^^^
The ``@vocabulary-uri`` attribute was `added <http://support.iatistandard.org/entries/105713163-Add-URI-attribute-to-elements-where-Reporting-organisation-vocabularies-are-used>`__.

2.01
^^^^
The ``sector`` element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#transaction-new-child-elements>`__ as a child element of ``transaction``.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1124>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/sector.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   sector/narrative

