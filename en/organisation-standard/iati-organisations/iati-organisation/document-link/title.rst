title
=====

``iati-organisations/iati-organisation/document-link/title``

This is the reference page for the XML element ``title``. 

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
| Example usage of ``title`` of a ``document-link`` in an ``iati-organisation``.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--document-link starts-->
	:end-before: <!--document-link ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-common.xsd#L50>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/document-link/title.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   title/narrative

