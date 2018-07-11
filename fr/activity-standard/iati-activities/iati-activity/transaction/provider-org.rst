provider-org
============

``iati-activities/iati-activity/transaction/provider-org``

This is the reference page for the XML element ``provider-org``. 

.. index::
  single: provider-org

Definition
~~~~~~~~~~


For incoming funds this is the organisation from which
the transaction originated. If omitted on outgoing funds
the reporting-org is assumed.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/provider-org/.ref:

@ref
  Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.


  This value must be of type xsd:string.



  ``transaction/provider-org/@ref`` should match the regex ``[^\/\&\|\?]+``
.. _iati-activities/iati-activity/transaction/provider-org/.provider-activity-id:

@provider-activity-id
  If incoming funds are being provided from the budget
  of another activity that is reported to IATI, it if
  STRONGLY RECOMMENDED that this should record the
  provider's unique IATI activity identifier for that
  activity.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/transaction/provider-org/.type:

@type
  The type of organisation providing the funds.


  This value must be of type xsd:string.


  This value must be on the :doc:`OrganisationType codelist </codelists/OrganisationType>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1015>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/transaction/provider-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   provider-org/narrative

