policy-marker
=============

``iati-activities/iati-activity/policy-marker``

This is the reference page for the XML element ``policy-marker``. 

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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L869>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/policy-marker.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   policy-marker/narrative

