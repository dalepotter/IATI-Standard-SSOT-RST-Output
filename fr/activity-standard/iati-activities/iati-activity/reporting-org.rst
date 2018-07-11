reporting-org
=============

``iati-activities/iati-activity/reporting-org``

This is the reference page for the XML element ``reporting-org``. 

.. index::
  single: reporting-org

Definition
~~~~~~~~~~


The organisation issuing the report.
May be a primary source (reporting on its own activity as
donor, implementing agency, etc) or a secondary source
(reporting on the activities of another organisation).

Specifying the @ref attribute is mandatory.
May contain the organisation name as content.

All activities in an activity xml file must contain the same
@ref AND this @ref must be the same as the iati-identifier
recorded in the registry publisher record of the account under
which this file is published.


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/reporting-org/.ref:

@ref
  Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}.

  This attribute is required.



  This value must be of type xsd:string.



  ``reporting-org/@ref`` should match the regex ``[^\/\&\|\?]+``
.. _iati-activities/iati-activity/reporting-org/.type:

@type
  The type of organisation issuing the report. See IATI codelist for values.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`OrganisationType codelist </codelists/OrganisationType>`.



  
.. _iati-activities/iati-activity/reporting-org/.secondary-reporter:

@secondary-reporter
  A flag indicating that the reporting organisation of this activity is acting as a secondary reporter. A secondary reporter is one that reproduces data on the activities of an organisation for which it is not directly responsible. This does not include a publisher officially assigned as a proxy to report on behalf of another.


  This value must be of type xsd:boolean.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L74>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/reporting-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   reporting-org/narrative

