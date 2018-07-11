title
=====

``iati-activities/iati-activity/result/indicator/title``

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
Example usage of ``title`` in context of an ``indicator`` in a ``result`` element.

.. literalinclude:: ../../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--result-indicator starts-->
	:end-before: <!--result-indicator ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should now be declared with the new child ``narrative`` element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L50>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/result/indicator/title.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   title/narrative

