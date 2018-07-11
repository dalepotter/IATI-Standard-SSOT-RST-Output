iati-activities
===============

``iati-activities``

This is the reference page for the XML element ``iati-activities``. 

.. index::
  single: iati-activities

Definition
~~~~~~~~~~


Top-level list of one or more IATI activity records.


Rules
~~~~~












Attributes
~~~~~~~~~~


.. _iati-activities/.version:

@version
  A number indicating the IATI specification version in use.
  This is mandatory and must be a valid version.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Version codelist </codelists/Version>`.



  
.. _iati-activities/.generated-datetime:

@generated-datetime
  A date/time stamp for when this file was generated. This
  is not necessarily the last-updated date for the
  individual activity records in it. Use of this attribute
  is highly recommended, to allow recipients to know when a
  file has been updated.


  This value must be of type xsd:dateTime.



  
.. _iati-activities/.linked-data-default:

@linked-data-default
  If a publisher chooses to publish linked data about their
  IATI activities then allowing them to declare where this
  data is published would support discovery of it, and any
  additional information they may choose to publish as
  Linked Data alongside it.
  
  This attribute is a URI path upon which an activity
  identifier can be appended to get a differentiable URI
  for any activity contained within a file.
  
  Where a publisher declares using one of these properties
  that authoritative linked data is accessible for an
  activity then consuming applications that are generating
  Linked Data from an IATI XML file should assert an
  owl:sameAs relationship to the relevant URI.


  This value must be of type xsd:anyURI.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``iati-activities``. 

| This element is a parent for other all other elements of the **IATI Activity Standard**.

| This example provides a dateTime of *2014-09-10T07:15:37Z*  for the ``@generated-datetime`` attribute.  
| A dateTime in UTC time is indicated by adding a *Z* behind the time
| This example date time format conforms to the *xsd:dateTime* standard.

| The ``@version`` attribute declares a valid code (*2.x*) from the *Version* codelist.
| The optional ``@linked-data-default`` attribute is also included.

.. literalinclude:: activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--iati-activities starts-->
	:end-before: <!--iati-activity starts-->

The ``iati-activities`` element acts as a container for other sub-elements.  It is closed as follows:

.. literalinclude:: activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--iati-activity ends-->	
	:end-before: <!--iati-activities ends-->
	
Changelog
~~~~~~~~~

1.02
^^^^
Introduced the ``@linked-data-default`` attribute on ``iati-activities`` element



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L28>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   iati-activities/iati-activity

