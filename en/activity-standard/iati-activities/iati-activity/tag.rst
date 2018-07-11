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



  



Example Usage
~~~~~~~~~~~~~
Example ``tag`` in a ``iati-activity`` element.

| The ``@vocabulary`` attribute declares a valid code (*1*) from the *TagVocabulary* codelist.
| An example value *1* from this vocabulary is declared with the ``@code`` attribute.

.. code-block:: xml

	<tag vocabulary="1" code="1" />

| The ``tag`` element can be repeated in any ``iati-activity``.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--tag starts-->
	:end-before: <!--tag ends-->

| If a vocabulary is not on the *TagVocabulary* codelist, then the value of *99* (Reporting Organisation) should be declared.

| If a publisher uses a vocabulary of 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:

.. code-block:: xml

    <tag vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="T1" />


Changelog
~~~~~~~~~

2.03
^^^^
The ``tag`` element within a ``iati-activity`` element was `added <https://discuss.iatistandard.org/t/non-statistical-secondary-sectors-excluded-2-03/849>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1533>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/tag.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   tag/narrative

