receiver-org
============

``iati-activities/iati-activity/planned-disbursement/receiver-org``

This is the reference page for the XML element ``receiver-org``. See also the relevant overview page: :doc:`/activity-standard/overview/budgets` 

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



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``receiver-org`` of a ``planned-disbursement`` in an ``iati-activity``.

| This example declares the organisation identifier with the ``@ref`` attribute.
| This example also declares the type of organisation which received the funds, using the @type attribute.

.. code-block:: xml

        <receiver-org ref="AA-AAA-123456789" type="23">Agency A</receiver-org>

| This example declares the unique ``iati-identifier`` of the reported ``iati-activity`` to where the transaction is received, with the ``@receiver-activity-id`` attribute.

.. code-block:: xml

        <receiver-org ref="AA-AAA-123456789" type="23" receiver-activity-id="AA-AAA-123456789-1234" />

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
| The optional ``receiver-org`` element was `added <http://support.iatistandard.org/entries/29665337-Add-provider-org-and-receiver-org-to-planned-disbursement-element>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2136>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/planned-disbursement/receiver-org.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   receiver-org/narrative

