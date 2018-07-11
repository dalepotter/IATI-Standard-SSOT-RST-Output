condition
=========

``iati-activities/iati-activity/conditions/condition``

This is the reference page for the XML element ``condition``. 

.. index::
  single: condition

Definition
~~~~~~~~~~


The text of a specific condition attached to the activity. Organisation-wide terms and conditions that apply to all activities should not be reported here, but in either iati-organisation/document-link or iati-activity-document-link


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/conditions/condition/.type:

@type
  An IATI code defining the type of condition.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`ConditionType codelist </codelists/ConditionType>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1955>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/conditions/condition.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   condition/narrative

