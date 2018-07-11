document-date
=============

``iati-activities/iati-activity/result/indicator/period/actual/document-link/document-date``

This is the reference page for the XML element ``document-date``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: document-date

Definition
~~~~~~~~~~


The date of publication of the document that is being linked to.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/result/indicator/period/actual/document-link/document-date/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  



Example Usage
~~~~~~~~~~~~~~~~~
This ``document-date`` element would normally be the production or published date of the relevant document to identify the specific document version.

Example Usage
~~~~~~~~~~~~~
| Example usage of the ``document-date`` element within a ``document-link`` in a ``actual`` in a ``period`` in a ``indicator`` as part of a ``result`` element.

| This examples declares an ISO date (corresponding to 5th February 2014) using the ``@iso-date`` attribute.

.. literalinclude:: ../../../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-document-link example starts-->
	:end-before: <!--result-document-link example ends-->

| The ``document-date`` element should only be used once for each ``document-link`` element.

Changelog
~~~~~~~~~

The optional ``document-date`` element of a ``document-link`` in a ``actual`` in a ``period`` in a ``indicator`` in a ``result`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L237>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/period/actual/document-link/document-date.rst>`_

