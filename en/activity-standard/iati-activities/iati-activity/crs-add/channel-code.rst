channel-code
============

``iati-activities/iati-activity/crs-add/channel-code``

This is the reference page for the XML element ``channel-code``. See also the relevant overview page: :doc:`/activity-standard/overview/crs-fss` 

.. index::
  single: channel-code

Definition
~~~~~~~~~~


The CRS channel code for this activity. This should only be used for reporting to CRS. The code list contains both organisation types and names of organisations. For non-CRS purposes these should be reported using the participating-org element.


Rules
~~~~~


The text in this element must be of type xsd:string.






This element must occur no more than once (within each parent element).








Example Usage
~~~~~~~~~~~~~
Example usage of ``channel-code`` of ``crs-add`` for an ``iati-activity``.

| The contents of the element contain a valid code (*21039*) from the *CRSChannelCode* codelist.

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--crs-add starts-->
	:end-before: <!--crs-add ends-->


Changelog
~~~~~~~~~
2.02
^^^^
The optional ``channel-code`` element was `added <http://support.iatistandard.org/entries/83678719-DAC-Channel-of-Delivery>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L2392>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/crs-add/channel-code.rst>`_

