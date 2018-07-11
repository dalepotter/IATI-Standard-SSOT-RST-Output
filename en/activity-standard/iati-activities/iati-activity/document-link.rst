document-link
=============

``iati-activities/iati-activity/document-link``

This is the reference page for the XML element ``document-link``. See also the relevant overview page: :doc:`/activity-standard/overview/linked-documents` 

.. index::
  single: document-link

Definition
~~~~~~~~~~


A link to an online, publicly accessible web page or document.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/document-link/.url:

@url
  The target URL of the external document, e.g. "http://www.example.org/doc.odt".

  This attribute is required.



  This value must be of type xsd:anyURI.



  
.. _iati-activities/iati-activity/document-link/.format:

@format
  An IANA code for the MIME type of the document being referenced, e.g. "application/pdf".

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FileFormat codelist </codelists/FileFormat>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``document-link`` in an ``iati-activity``.

| This element is a parent for other child elements.

| The ``@format`` attribute declares a valid code (*application/vnd.oasis.opendocument.text*) from the *FileFormat* codelist.

.. code-block:: xml

    <document-link format="application/vnd.oasis.opendocument.text" url="http:www.example.org/docs/report_en.odt">
    ...
    </document-link>

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--document-link starts-->
	:end-before: <!--document-link ends-->

| The ``document-link`` element can be repeated in any ``iati-activity``.

Changelog
~~~~~~~~~
2.03
^^^^
The child element ``description`` was `added <https://discuss.iatistandard.org/t/document-link-description-included-2-03/841>`__.

1.02
^^^^
Removed ``@language`` attribute from, and introduced an new ``language`` child element to, the ``document-link`` element.




Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L150>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/document-link.rst>`_


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

