provider-org
============

``iati-activities/iati-activity/planned-disbursement/provider-org``

This is the reference page for the XML element ``provider-org``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

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



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``provider-org`` of a ``planned-disbursement`` in an ``iati-activity``.

| This example declares the organisation identifier with the ``@ref`` attribute.
| This example also declares the type of organisation which provided the funds, using the @type attribute.

.. code-block:: xml

        <provider-org ref="BB-BBB-123456789-1234AA" type="10" />

| This example declares the unique ``iati-identifier`` of the reported ``iati-activity`` from where the transaction is provided, with the ``@provider-activity-id`` attribute.

.. code-block:: xml

        <provider-org ref="BB-BBB-123456789" type="10" provider-activity-id="BB-BBB-123456789-1234AA" />

Full example, within a ``planned-disbursement``.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--planned-disbursement starts-->
	:end-before: <!--planned-disbursement ends-->

Changelog
~~~~~~~~~

2.03
^^^^
| The definition of the ``@ref`` attribute was `updated <https://discuss.iatistandard.org/t/migration-of-organisationregistrationagency-codelist-to-org-id-guide-included-2-03/851>`__.

2.02
^^^^
| The optional ``provider-org`` element was `added <http://support.iatistandard.org/entries/29665337-Add-provider-org-and-receiver-org-to-planned-disbursement-element>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2094>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/planned-disbursement/provider-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   provider-org/narrative

