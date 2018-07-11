document-link
=============

``iati-activities/iati-activity/result/indicator/document-link``

This is the reference page for the XML element ``document-link``. 

.. index::
  single: document-link

Definition
~~~~~~~~~~


A link to an online, publicly accessible web page or document expanding on the result.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/document-link/.url:

@url
  The target URL of the external document, e.g. "http://www.example.org/doc.odt".

  This attribute is required.



  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/result/indicator/document-link/.format:

@format
  An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FileFormat codelist </codelists/FileFormat>`.



  





Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1740>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/fr/activity-standard/iati-activities/iati-activity/result/indicator/document-link.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   document-link/title
   document-link/description
   document-link/category
   document-link/language
   document-link/document-date

