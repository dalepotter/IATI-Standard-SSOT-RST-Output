document-link
=============

``iati-organisations/iati-organisation/document-link``

This is the reference page for the XML element ``document-link``. 

.. index::
  single: document-link

Definition
~~~~~~~~~~


The recipient country that is the focus of the document.
May be repeated for multiple countries.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/document-link/.url:

@url
  The target URL of the external document, e.g. "http://www.example.org/doc.odt".

  This attribute is required.



  This value must be of type xsd:anyURI.



  
.. _iati-organisations/iati-organisation/document-link/.format:

@format
  An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FileFormat codelist </codelists/FileFormat>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L84>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/organisation-standard/iati-organisations/iati-organisation/document-link.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   document-link/recipient-country
   document-link/narrative
   document-link/title
   document-link/description
   document-link/category
   document-link/language
   document-link/document-date

