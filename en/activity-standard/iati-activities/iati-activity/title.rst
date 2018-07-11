title
=====

``iati-activities/iati-activity/title``

This is the reference page for the XML element ``title``. 

.. index::
  single: title

Definition
~~~~~~~~~~


Data type for an element that must contain human-readable text.
The information may be repeated in different languages.


Rules
~~~~~








This element must occur once and only once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example ``title`` for an ``iati-activity``:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--title starts-->
	:end-before: <!--title ends-->

Changelog
~~~~~~~~~
2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.



Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L93>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/title.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   title/narrative

