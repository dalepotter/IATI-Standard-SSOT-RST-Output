title
=====

``iati-activities/iati-activity/result/indicator/document-link/title``

This is the reference page for the XML element ``title``. See also the relevant overview page: :doc:`/activity-standard/overview/result` 

.. index::
  single: title

Definition
~~~~~~~~~~


A short, human-readable title.


Rules
~~~~~








This element must occur once and only once (within each parent element).








Example Usage
~~~~~~~~~~~~~
| Example usage of ``title`` of a ``document-link`` in a ``indicator`` in a ``result`` element.

.. literalinclude:: ../../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-document-link example starts-->
	:end-before: <!--result-document-link example ends-->

Changelog
~~~~~~~~~

2.03
^^^^
The mandatory ``title`` element of a ``document-link`` in a ``indicator`` in a ``result`` element was `added <https://discuss.iatistandard.org/t/add-document-link-to-results-indicator-included-2-03/895>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L50>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/document-link/title.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   title/narrative

