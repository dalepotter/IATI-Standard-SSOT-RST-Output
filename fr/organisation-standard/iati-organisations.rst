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



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L28>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   iati-organisations/iati-organisation

