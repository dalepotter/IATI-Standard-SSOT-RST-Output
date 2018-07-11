recipient-region
================

``iati-activities/iati-activity/recipient-region``

This is the reference page for the XML element ``recipient-region``. See also the relevant overview page: :doc:`/activity-standard/overview/geography` 

.. index::
  single: recipient-region

Definition
~~~~~~~~~~


A supranational geopolitical region that will benefit from
this activity. For sub-national geographical location, use the
location element.

Multiple countries and regions can be reported, in which case
the percentage attribute MUST be used to specify the share of
total commitments across all reported countries and regions.
Recipient-region must not be used merely to describe the
region of a country reported in recipient-country, but ONLY if
the region is a recipient IN ADDITION to the country.

Region can also be reported at transaction rather than
activity level. If transaction/recipient-country AND/OR
transaction/recipient-region are used THEN ALL transaction
elements MUST contain a recipient-country and/or
recipient-region element AND iati-activity/recipient-region
and iati-activity/recipient-region MUST NOT be used AND each
transaction MUST only contain one recipient-country or
recipient-region.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/recipient-region/.code:

@code
  Either an OECD DAC or UN region code. Codelist is
  determined by vocabulary attribute.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Region codelist </codelists/Region>`, if the relevant vocabulary is used.



  
.. _iati-activities/iati-activity/recipient-region/.vocabulary:

@vocabulary
  An IATI code for the vocabulary from which the region code
  is drawn. If it is not present 1 - 'OECD DAC' is assumed.


  This value must be of type xsd:string.


  This value must be on the :doc:`RegionVocabulary codelist </codelists/RegionVocabulary>`.



  
.. _iati-activities/iati-activity/recipient-region/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined. If the vocabulary is 99 (reporting organisation), the URI where this internal vocabulary is defined. While this is an optional field it is STRONGLY RECOMMENDED that all publishers use it to ensure that the meaning of their codes are fully understood by data users.


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/recipient-region/.percentage:

@percentage
  The percentage of total commitments or total activity budget to this item. Content must be a decimal number between 0 and 100 inclusive, with no percentage sign. Percentages for all reported countries and regions MUST add up to 100.


  This value must be of type xsd:decimal.



  The sum of values matched at ``recipient-region/@percentage`` and ``recipient-country/@percentage`` must be ``100``.



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

Please note, if using your own vocabulary (i.e. code 99), it is recommended that this is used in addition to the DAC OECD region vocabulary (code 1).

| The ``recipient-region`` element can be repeated in any ``iati-activity``.

| When multiple ``recipient-region`` are declared, then the ``@percentage`` values should sum to 100% for the specific ``iati-activity``.

.. code-block:: xml

	<recipient-region code="489" vocabulary="1" percentage="50" />
	<recipient-region code="389" vocabulary="1" percentage="50" />

| When both the ``recipient-region`` and ``recipient-country``, then the ``@percentage`` values should sum to 100% for the specific ``iati-activity``.

.. code-block:: xml

	<recipient-country code="AF" percentage="50" />
	<recipient-region code="489" vocabulary="1" percentage="50" />


Changelog
~~~~~~~~~

2.03
^^^^
Definition of ``@vocabulary-uri`` attribute `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.
Definition of ``@percentage`` attribute `updated <https://discuss.iatistandard.org/t/boundary-values-for-percentages-included-2-03/843>`__.

2.02
^^^^
The ``vocabulary-uri`` attribute was `added <http://support.iatistandard.org/entries/105713163-Add-URI-attribute-to-elements-where-Reporting-organisation-vocabularies-are-used>`__.

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element, but only in particular use-cases.

1.03
^^^^
Where used, the ``@percentage`` attribute is now designated as a decimal value and no longer as a positive Integer


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L367>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/recipient-region.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   recipient-region/narrative

