humanitarian-scope
==================

``iati-activities/iati-activity/humanitarian-scope``

This is the reference page for the XML element ``humanitarian-scope``. 

.. index::
  single: humanitarian-scope

Definition
~~~~~~~~~~


Classification of emergencies, appeals and other humanitarian
events and actions.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/humanitarian-scope/.type:

@type
  A code for the type of event or action being classified.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`HumanitarianScopeType codelist </codelists/HumanitarianScopeType>`.



  
.. _iati-activities/iati-activity/humanitarian-scope/.vocabulary:

@vocabulary
  A code for a recognised vocabulary of terms classifying the
  event or action.

  This attribute is required.



  This value must be of type xsd:string.


  This value should be on the :doc:`HumanitarianScopeVocabulary codelist </codelists/HumanitarianScopeVocabulary>`.



  
.. _iati-activities/iati-activity/humanitarian-scope/.vocabulary-uri:

@vocabulary-uri
  A u.r.i. for the vocabulary specified which provides access to
  the list of codes and descriptions.


  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/humanitarian-scope/.code:

@code
  A code for the event or action from the vocabulary specified.

  This attribute is required.



  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example ``humanitarian-scope`` of an ``iati-activity``.

| The ``@type`` attribute declares a valid code (*1*) from the *HumanitarianScopeType* codelist.
| The ``@vocabulary`` attribute declares a valid code (*1-2*) from the *HumanitarianScopeVocabulary* codelist.
| The ``@code`` attribute declares a valid code (*EQ-2015-000048-NPL*) from the specified vocabulary.

.. code-block:: xml

	<humanitarian-scope type="1" vocabulary="1-2" code="EQ-2015-000048-NPL">
	...
	</humanitarian-scope>

If a publisher uses a vocabulary of 99 (i.e. 'Reporting Organisation'), then the ``@vocabulary-uri`` attribute should also be used, for example:

.. code-block:: xml

	<humanitarian-scope type="1" vocabulary="99" vocabulary-uri="http://example.com/vocab.html" code="5">
	  <narrative>Nepal Earthquake (April 2015)</narrative>
	</humanitarian-scope>


| The ``humanitarian-scope`` element can be repeated in any ``iati-activity``.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--humanitarian-scope starts-->
	:end-before: <!--humanitarian-scope ends-->

| If a vocabulary is not on the *HumanitarianScopeVocabulary* codelist, then the value of *99* (*Reporting Organisation*) should be declared.

Changelog
~~~~~~~~~

2.03
^^^^
The definition of the ``@vocabulary-uri`` was `updated <https://discuss.iatistandard.org/t/guidance-on-u-r-i-usage-for-publisher-s-own-vocabularies-included-2-03/850>`__.

2.02
^^^^
The ``humanitarian-scope`` element was `added <http://support.iatistandard.org/entries/105778163-Humanitarian-Emergencies-and-Appeals>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L817>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/humanitarian-scope.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   humanitarian-scope/narrative

