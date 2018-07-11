default-aid-type
================

``iati-activities/iati-activity/default-aid-type``

This is the reference page for the XML element ``default-aid-type``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: default-aid-type

Definition
~~~~~~~~~~


The type of aid being supplied (project-type intervention,
budget support, debt relief, etc.). This element specifies a
default for all the activity's financial transactions; it can
be overridden at the individual transaction level.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/default-aid-type/.code:

@code
  A code from the specified vocabulary.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`AidType codelist </codelists/AidType>`.



  
.. _iati-activities/iati-activity/default-aid-type/.vocabulary:

@vocabulary
  A code for the vocabulary aid-type classifications. If omitted the AidType (OECD DAC) codelist is assumed. The code must be a valid value in the AidTypeVocabulary codelist.


  This value must be of type xsd:string.


  This value must be on the :doc:`AidTypeVocabulary codelist </codelists/AidTypeVocabulary>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``default-aid-type``  for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*A01*) from the *AidType* codelist.
| The ``@vocabulary`` attribute declares a valid code (*1*) from the *AidTypeVocabulary* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--default-aid-type starts-->
	:end-before: <!--default-aid-type ends-->

Changelog
~~~~~~~~~
2.03
^^^^
The ``default-aid-type`` element can be reported multiple times within a ``iati-activity`` element `added <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__.
The ``@code`` attribute definition was `updated <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__.
The ``@vocabulary`` attribute was `added <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__.

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L474>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/default-aid-type.rst>`_

