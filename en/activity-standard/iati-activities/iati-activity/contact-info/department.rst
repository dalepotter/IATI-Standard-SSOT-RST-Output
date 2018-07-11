department
==========

``iati-activities/iati-activity/contact-info/department``

This is the reference page for the XML element ``department``. See also the relevant overview page: :doc:`/activity-standard/overview/contact-info` 

.. index::
  single: department

Definition
~~~~~~~~~~


Data type for an element that must contain human-readable text.
The information may be repeated in different languages.


Rules
~~~~~








This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example ``department`` within ``contact-info`` of an ``iati-activity``.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--contact-info starts-->
	:end-before: <!--contact-info ends-->

Changelog
~~~~~~~~~

2.01
^^^^
The ``contact-info/department`` child element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#contact-info-department-new-element>`__


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L701>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/contact-info/department.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   department/narrative

