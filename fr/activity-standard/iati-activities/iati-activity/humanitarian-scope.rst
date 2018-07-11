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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L817>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/humanitarian-scope.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   humanitarian-scope/narrative

