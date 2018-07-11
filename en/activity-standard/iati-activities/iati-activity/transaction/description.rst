description
===========

``iati-activities/iati-activity/transaction/description``

This is the reference page for the XML element ``description``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: description

Definition
~~~~~~~~~~


Data type for an element that must contain human-readable text.
The information may be repeated in different languages.


Rules
~~~~~








This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example usage of ``description`` of a ``transaction`` in an ``iati-activity``.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1008>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/description.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   description/narrative

