iati-organisations
==================

``iati-organisations``

This is the reference page for the XML element ``iati-organisations``. 

.. index::
  single: iati-organisations

Definition
~~~~~~~~~~


Top-level list of one or more IATI organisation records.


Rules
~~~~~












Attributes
~~~~~~~~~~


.. _iati-organisations/.version:

@version
  A number indicating the IATI specification version in use.
  This is mandatory and must be a valid version.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`Version codelist </codelists/Version>`.



  
.. _iati-organisations/.generated-datetime:

@generated-datetime
  A date/time stamp for when this file was generated. This
  is not necessarily the last-updated date for the
  individual activity records in it. Use of this attribute
  is highly recommended, to allow recipients to know when a
  file has been updated.


  This value must be of type xsd:dateTime.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``iati-organisations``.

| This element is a parent for other all other elements of the **IATI Organisation Standard**.

| This example provides a dateTime of *2014-09-10T07:15:37Z*  for the ``@generated-datetime`` attribute.  
| A dateTime in UTC time is indicated by adding a *Z* behind the time
| This example dateTime format conforms to the *xsd:dateTime* standard.

| The ``@version`` attribute declares a valid code (*2.01*) from the *Version* codelist.

.. literalinclude:: organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--iati-organisations starts-->
	:end-before: <!--iati-organisation starts-->

The ``iati-organisation`` element acts as a container for other sub-elements.  It is closed as follows:

.. literalinclude:: organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--iati-organisation ends-->	
	:end-before: <!--iati-organisations ends-->


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L28>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   iati-organisations/iati-organisation

