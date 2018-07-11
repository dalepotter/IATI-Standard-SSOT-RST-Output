aid-type
========

``iati-activities/iati-activity/transaction/aid-type``

This is the reference page for the XML element ``aid-type``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: aid-type

Definition
~~~~~~~~~~


A code from the specified vocabulary.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/aid-type/.code:

@code
  A code from the specified vocabulary.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`AidType codelist </codelists/AidType>`.



  
.. _iati-activities/iati-activity/transaction/aid-type/.vocabulary:

@vocabulary
  A code for the vocabulary aid-type classifications. If omitted the AidType (OECD DAC) codelist is assumed. The code must be a valid value in the AidTypeVocabulary codelist.


  This value must be of type xsd:string.


  This value must be on the :doc:`AidTypeVocabulary codelist </codelists/AidTypeVocabulary>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``aid-type`` of a ``transaction`` in an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*A02*) from the *AidType* codelist.
| The ``@vocabulary`` attribute declares a valid code (*1*) from the *AidTypeVocabulary* codelist.

| Note: The ``aid-type`` element can override the ``default-aid-type`` value set in ``iati-activity``:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.03
^^^^
The ``aid-type`` element can be reported multiple times within a ``transaction`` element `added <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__.
The ``@code`` attribute definition was `updated <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__.
The ``@vocabulary`` attribute was `added <https://discuss.iatistandard.org/t/add-vocabularies-to-aid-type-included-2-03/847>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1274>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/aid-type.rst>`_

