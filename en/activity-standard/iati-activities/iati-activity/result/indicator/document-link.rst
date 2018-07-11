document-link
=============

``iati-activities/iati-activity/result/indicator/document-link``

This is the reference page for the XML element ``document-link``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

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



  



Example Usage
~~~~~~~~~~~~~

Example ``document-link`` in a ``indicator`` in a ``result`` element.

| This element is a parent for other child elements.

| The ``@format`` attribute declares a valid code (*application/vnd.oasis.opendocument.text*) from the *FileFormat* codelist.
| The ``@url`` attribute provides the document location.

.. code-block:: xml

    <document-link format="application/vnd.oasis.opendocument.text" url="http:www.example.org/docs/result_indicator_en.odt">
    ...
    </document-link>

| Full example with all child elements:

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-indicator starts-->
	:end-before: <!--result-indicator ends-->

| The ``document-link`` element can be repeated in any ``result`` element.

Changelog
~~~~~~~~~

2.03
^^^^
The optional ``document-link`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1740>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/document-link.rst>`_


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

