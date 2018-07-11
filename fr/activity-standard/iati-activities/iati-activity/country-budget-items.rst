country-budget-items
====================

``iati-activities/iati-activity/country-budget-items``

This is the reference page for the XML element ``country-budget-items``. 

.. index::
  single: country-budget-items

Definition
~~~~~~~~~~


This item encodes the alignment of activities with both the functional and administrative classifications used in the recipient country's Chart of Accounts. This applies to both on- and off-budget activities.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/country-budget-items/.vocabulary:

@vocabulary
  An IATI code for the common functional classification or country system (This allows for common codes, country-specific, or any other classification agreed between countries and donors).

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`BudgetIdentifierVocabulary codelist </codelists/BudgetIdentifierVocabulary>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1569>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/country-budget-items.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   country-budget-items/budget-item

