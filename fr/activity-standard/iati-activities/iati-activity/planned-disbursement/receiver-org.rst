receiver-org
============

``iati-activities/iati-activity/planned-disbursement/receiver-org``

This is the reference page for the XML element ``receiver-org``. 

.. index::
  single: receiver-org

Definition
~~~~~~~~~~


The organisation receiving the money from the planned disbursement.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/planned-disbursement/receiver-org/.ref:

@ref
  Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}. If this is not present then the narrative MUST contain the name of the organisation.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/planned-disbursement/receiver-org/.receiver-activity-id:

@receiver-activity-id
  If outgoing funds are being provided to another activity that is reported to IATI, this may, if possible, record the unique IATI activity identifier for that activity.


  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/planned-disbursement/receiver-org/.type:

@type
  The type of organisation receiving the funds.


  This value must be of type xsd:string.


  This value must be on the :doc:`OrganisationType codelist </codelists/OrganisationType>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2136>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/planned-disbursement/receiver-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   receiver-org/narrative

