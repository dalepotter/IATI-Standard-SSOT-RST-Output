other-flags
===========

``iati-activities/iati-activity/crs-add/other-flags``

This is the reference page for the XML element ``other-flags``. 

.. index::
  single: other-flags

Definition
~~~~~~~~~~


This covers the four CRS++ columns titled:
"Free standing technical cooperation";
"Programme-based approach";
"Investment project";
"Associated financing"


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/crs-add/other-flags/.code:

@code
  An IATI code describing the equivalent CRS++ columns

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`CRSAddOtherFlags codelist </codelists/CRSAddOtherFlags>`.



  
.. _iati-activities/iati-activity/crs-add/other-flags/.significance:

@significance
  A boolean indicating whether the flag applies. If 'false' do not report the flag

  This attribute is required.



  This value must be of type xsd:boolean.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2198>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/crs-add/other-flags.rst>`_

