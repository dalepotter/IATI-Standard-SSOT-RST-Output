name
====

``iati-organisations/iati-organisation/name``

This is the reference page for the XML element ``name``. See also the relevant overview pages: :doc:`/organisation-standard/overview/organisations`,  :doc:`/organisation-standard/overview/iati-organisation` 

.. index::
  single: name

Definition
~~~~~~~~~~


The human-readable name of the organisation.


Rules
~~~~~








This element must occur once and only once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example of ``name`` of an ``iati-organisation``.

.. literalinclude:: ../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--name starts-->
	:end-before: <!--name ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L117>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/name.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   name/narrative

