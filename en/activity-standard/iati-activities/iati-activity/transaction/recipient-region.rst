recipient-region
================

``iati-activities/iati-activity/transaction/recipient-region``

This is the reference page for the XML element ``recipient-region``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: recipient-region

Definition
~~~~~~~~~~


A supranational geopolitical region that will benefit from this transaction. If a specific country is not known, then this element MUST be used.

If transaction/recipient-country AND/OR transaction/recipient-region are used THEN ALL transaction elements MUST contain a recipient-country or recipient-region element AND (iati-activity/recipient-country AND iati-activity/recipient-region MUST NOT be used)


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/recipient-region/.code:

@code
  Either an OECD DAC or UN region code. Codelist i determined by vocabulary attribute.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Region codelist </codelists/Region>`, if the relevant vocabulary is used.



  
.. _iati-activities/iati-activity/transaction/recipient-region/.vocabulary:

@vocabulary
  An IATI code for the vocabulary from which the region code is drawn. If it is not present 1 - 'OECD DAC' is assumed.


  This value must be of type xsd:string.


  This value must be on the :doc:`RegionVocabulary codelist </codelists/RegionVocabulary>`.



  
.. _iati-activities/iati-activity/transaction/recipient-region/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  



Example Usage
~~~~~~~~~~~~~
Example ``recipient-region`` of an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*489*) from the *Region* codelist.
| The optional ``@vocabulary`` attribute declares a valid code (*1*) from the *RegionVocabulary* codelist.

.. code-block:: xml

	<recipient-region code="489" vocabulary="1" />

If a publisher uses a vocabulary of 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:

.. code-block:: xml

	<recipient-region code="A1" vocabulary="99" vocabulary-uri="http://example.com/vocab.html" />

Full example:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.03
^^^^
Definition of ``@vocabulary-uri`` attribute `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.

2.02
^^^^
The ``vocabulary-uri`` attribute was `added <http://support.iatistandard.org/entries/105713163-Add-URI-attribute-to-elements-where-Reporting-organisation-vocabularies-are-used>`__.

2.01
^^^^
The ``sector`` element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#transaction-new-child-elements>`__ as a child element of ``transaction``.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1197>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/recipient-region.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-region/narrative

