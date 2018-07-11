tag
===

``iati-activities/iati-activity/tag``

This is the reference page for the XML element ``tag``. 

.. index::
  single: tag

Definition
~~~~~~~~~~


Categorisations from established taxonomies that enrich the classification of the activity but that, unlike those reported in the sector element, cannot be associated with percentage splits on finances.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/tag/.code:

@code
  The code for the tag as defined in the specified vocabulary.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/tag/.vocabulary:

@vocabulary
  An IATI code for the vocabulary or taxonomy (see non-embedded codelist) used for tag classifications.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`TagVocabulary codelist </codelists/TagVocabulary>`.



  
.. _iati-activities/iati-activity/tag/.vocabulary-uri:

@vocabulary-uri
  The URI where this vocabulary is defined.


  This value must be of type xsd:anyURI.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1533>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/tag.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   tag/narrative

