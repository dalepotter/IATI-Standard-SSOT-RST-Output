policy-marker
=============

``iati-activities/iati-activity/policy-marker``

This is the reference page for the XML element ``policy-marker``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: policy-marker

Definition
~~~~~~~~~~


A policy or theme addressed by the activity. This element was
designed for the reporting of OECD DAC CRS policy markers
(columns 20-23 and 28-31 of the CRS++ reporting format) but
the vocabulary attribute allows it use by other (including
local) systems. This element can be repeated for each policy
marker.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/policy-marker/.vocabulary:

@vocabulary
  An IATI code for the vocabulary to be used to define
  policy markers. If omitted then the OECD DAC vocabulary is
  assumed.


  This value must be of type xsd:string.


  This value must be on the :doc:`PolicyMarkerVocabulary codelist </codelists/PolicyMarkerVocabulary>`.



  
.. _iati-activities/iati-activity/policy-marker/.vocabulary-uri:

@vocabulary-uri
  If the vocabulary is 99 (reporting organisation), the URI
  where this internal vocabulary is defined.


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/policy-marker/.code:

@code
  A policy marker code from the codelist specified in the
  vocabulary.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`PolicyMarker codelist </codelists/PolicyMarker>`, if the relevant vocabulary is used.



  
.. _iati-activities/iati-activity/policy-marker/.significance:

@significance
  An OECD DAC CRS code indicating the significance of the policy marker
  for this activity. This attribute MUST be used for all OECD DAC CRS
  vocabularies.


  This value must be of type xsd:string.


  This value must be on the :doc:`PolicySignificance codelist </codelists/PolicySignificance>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``policy-marker`` of an ``iati-activity``.

| The ``@vocabulary`` attribute declares a valid code (*1*) from the *PolicyMarkerVocabulary* codelist.
| The ``@code`` attribute declares a valid code (*1*) from the *PolicyMarker* codelist.
| The ``@significance`` attribute declares a valid code (*3*) from the *PolicySignificance* codelist.

.. code-block:: xml

	<policy-marker vocabulary="1" code="2" significance="3" />

If a publisher uses a vocabulary of 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:

.. code-block:: xml

	<policy-marker vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="A1" significance="3" />

| The ``policy-marker`` element can be repeated in any ``iati-activity``.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--policy-marker starts-->
	:end-before: <!--policy-marker ends-->

| If a vocabulary is not on the *PolicyMarkerVocabulary* codelist, then the value of *99* (*Reporting Organisation*) should be declared.

Changelog
~~~~~~~~~

2.03
^^^^
The definition of the ``@vocabulary-uri`` was `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.

2.02
^^^^
The ``vocabulary-uri`` attribute was `added <http://support.iatistandard.org/entries/105713163-Add-URI-attribute-to-elements-where-Reporting-organisation-vocabularies-are-used>`__.

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element, but only in particular use-cases.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L869>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/policy-marker.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   policy-marker/narrative

