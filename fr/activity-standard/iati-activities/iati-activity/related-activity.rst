related-activity
================

``iati-activities/iati-activity/related-activity``

This is the reference page for the XML element ``related-activity``. 

.. index::
  single: related-activity

Definition
~~~~~~~~~~


Another separately reported IATI activity that is related to this one. The ‘type’ attribute describes the type of relationship: (eg. parent, child, multifunded). It is strongly recommended that linkage between activities in a hierarchical group should always be managed by use of this element with @type of 1 (parent) or 2 (child).


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/related-activity/.ref:

@ref
  A valid activity identifier (as defined in iati-activity/iati-identifier).

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/related-activity/.type:

@type
  An IATI code for the type of relationship

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`RelatedActivityType codelist </codelists/RelatedActivityType>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1624>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/related-activity.rst>`_

