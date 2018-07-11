category
========

``iati-activities/iati-activity/result/indicator/period/actual/document-link/category``

This is the reference page for the XML element ``category``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: category

Definition
~~~~~~~~~~


IATI Document Category Code


Rules
~~~~~








This element must occur at least once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/actual/document-link/category/.code:

@code
  An IATI code defining the category of the document.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`DocumentCategory codelist </codelists/DocumentCategory>`.



  



Example Usage
~~~~~~~~~~~~~
| Example  usage of ``category`` of a ``document-link`` in a ``actual`` in a ``period`` in a ``indicator`` in a ``result`` element.

| This examples declares the ``DocumentCategory`` code *A01*, using the ``@code`` attribute.

.. literalinclude:: ../../../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-document-link example starts-->
	:end-before: <!--result-document-link example ends-->

| The ``category`` element can be repeated in any ``document-link``.

Changelog
~~~~~~~~~

2.03
^^^^
The mandatory ``category`` element of a ``document-link`` in a ``actual`` in a ``period`` in a ``indicator`` in a ``result`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L197>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/category.rst>`_

