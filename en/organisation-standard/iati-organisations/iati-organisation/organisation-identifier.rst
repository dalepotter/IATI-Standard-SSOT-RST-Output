organisation-identifier
=======================

``iati-organisations/iati-organisation/organisation-identifier``

This is the reference page for the XML element ``organisation-identifier``. 

.. index::
  single: organisation-identifier

Definition
~~~~~~~~~~


Machine-readable identification string for the organisation issuing the report. Must be in the format {RegistrationAgency}-{RegistrationNumber} where {RegistrationAgency} is a valid code in the Organisation Registration Agency code list and {RegistrationNumber} is a valid identifier issued by the {RegistrationAgency}.


Rules
~~~~~








This element must occur once and only once (within each parent element).







``organisation-identifier`` should match the regex ``[^\/\&\|\?]+``





Example Usage
~~~~~~~~~~~~~
Example ``organisation-identifier`` of an ``iati-organisation``.

.. literalinclude:: ../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--organisation-identifier starts-->
	:end-before: <!--organisation-identifier ends-->

Changelog
~~~~~~~~~

2.03
^^^^
| The definition of the ``organisation-identifier`` element was `updated <https://discuss.iatistandard.org/t/migration-of-organisationregistrationagency-codelist-to-org-id-guide-included-2-03/851>`__.

2.01
^^^^
The ``iati-identifier`` element was `renamed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#iati-identifier-renamed-element>`__  as ``organisation-identifier``


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L70>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/organisation-identifier.rst>`_

