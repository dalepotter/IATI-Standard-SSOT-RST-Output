crs-add
=======

``iati-activities/iati-activity/crs-add``

This is the reference page for the XML element ``crs-add``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: crs-add

Definition
~~~~~~~~~~


Additional items specific to CRS++ reporting.


Rules
~~~~~








This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example ``crs-add`` for an ``iati-activity``.

| This element is a parent for other child element.

.. code-block:: xml

     <crs-add attached="1">
     ...
     </crs-add>

| Full example with all child elements:

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->


Changelog
~~~~~~~~~

1.03
^^^^

| New in 1.03
| Added the optional ``crs-add`` element and its child elements


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2190>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   crs-add/other-flags
   crs-add/loan-terms
   crs-add/loan-status
   crs-add/channel-code

