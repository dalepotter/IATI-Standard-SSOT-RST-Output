other-flags
===========

``iati-activities/iati-activity/crs-add/other-flags``

This is the reference page for the XML element ``other-flags``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

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



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``other-flags`` of ``crs-add`` for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*1*) from the *CRSAddOtherFlags* codelist.

| A ``@significance`` boolean of *1* indicates that this flag is reported.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->


Changelog
~~~~~~~~~
2.01
^^^^
The element ``aid-type-flag`` has been `renamed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#other-flags-renamed-element>`__.

The associated codelist *AidTypeFlag* has been renamed as *CRSAddOtherFlags*

1.03
^^^^

| New in 1.03
| Added the optional ``crs-add`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2198>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/other-flags.rst>`_

