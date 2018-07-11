provider-org
============

``iati-activities/iati-activity/planned-disbursement/provider-org``

This is the reference page for the XML element ``provider-org``. 

.. index::
  single: provider-org

Definition
~~~~~~~~~~


The organisation from which the planned disbursement will originate.
If omitted the reporting-org is assumed.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/planned-disbursement/provider-org/.ref:

@ref
  Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/planned-disbursement/provider-org/.provider-activity-id:

@provider-activity-id
  The identifier for the activity in which the planned disbursement will be reported. If omitted the current activity is assumed.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/planned-disbursement/provider-org/.type:

@type
  The type of organisation providing the funds.


  This value must be of type xsd:string.


  This value must be on the :doc:`OrganisationType codelist </codelists/OrganisationType>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2094>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/planned-disbursement/provider-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   provider-org/narrative

