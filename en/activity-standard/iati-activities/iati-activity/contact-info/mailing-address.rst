mailing-address
===============

``iati-activities/iati-activity/contact-info/mailing-address``

This is the reference page for the XML element ``mailing-address``. See also the relevant overview page: :doc:`/activity-standard/overview/contact-info` 

.. index::
  single: mailing-address

Definition
~~~~~~~~~~


Data type for an element that must contain human-readable text.
The information may be repeated in different languages.


Rules
~~~~~








This element may occur any number of times.








Example Usage
~~~~~~~~~~~~~
Example ``mailing-address`` within ``contact-info`` of an ``iati-activity``

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--contact-info starts-->
	:end-before: <!--contact-info ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is no longer allowed with this element.  It should `now be declared <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#narrative-new-elements>`__  with the new child ``narrative`` element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L767>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/contact-info/mailing-address.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   mailing-address/narrative

