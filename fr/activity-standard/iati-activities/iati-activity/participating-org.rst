participating-org
=================

``iati-activities/iati-activity/participating-org``

This is the reference page for the XML element ``participating-org``. 

.. index::
  single: participating-org

Definition
~~~~~~~~~~


An organisation involved with the activity. May be a donor, fund, agency, etc. Specifying the @ref identifier is strongly recommended. May contain the organisation name as narrative.

If the reporting organisation plays a role in the activity it should be repeated here. One organisation may play more than one role (eg, funding and implementing): in such a case each role should be reported and the name of the organisation repeated.


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/participating-org/.ref:

@ref
  Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.


  This value must be of type xsd:string.



  ``participating-org/@ref`` should match the regex ``[^\/\&\|\?]+``

  Either ``@ref`` or ``narrative`` must be present.
.. _iati-activities/iati-activity/participating-org/.type:

@type
  The type of organisation issuing the report. See IATI codelist for values.


  This value must be of type xsd:string.


  This value must be on the :doc:`OrganisationType codelist </codelists/OrganisationType>`.



  
.. _iati-activities/iati-activity/participating-org/.role:

@role
  An IATI code describing the organisation's role in the activity (donor, agency, etc.).

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`OrganisationRole codelist </codelists/OrganisationRole>`.



  
.. _iati-activities/iati-activity/participating-org/.activity-id:

@activity-id
  A valid activity identifier published by the participating organisation which points to the activity that it has published to IATI that describes its role in this activity.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/participating-org/.crs-channel-code:

@crs-channel-code
  Under CRS++ Reporting Directives this code identifies the implementing agency. Codes ending in '00' are generic and are similar to the OrganisationType code.


  This value must be of type xsd:string.


  This value must be on the :doc:`CRSChannelCode codelist </codelists/CRSChannelCode>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L250>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/participating-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   participating-org/narrative

