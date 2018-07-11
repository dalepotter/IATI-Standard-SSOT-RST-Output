description
===========

``iati-activities/iati-activity/result/document-link/description``

This is the reference page for the XML element ``description``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: description

Definition
~~~~~~~~~~


A description of the document contents, or guidance on where to access the relevant information in the document.


Rules
~~~~~








This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~

Example usage of ``description``  of a ``document-link`` in a ``result`` element.

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-document-link example starts-->
	:end-before: <!--result-document-link example ends-->

Changelog
~~~~~~~~~

2.03
^^^^
The optional ``description`` element of a ``document-link`` in a ``result`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L190>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/document-link/description.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   description/narrative

