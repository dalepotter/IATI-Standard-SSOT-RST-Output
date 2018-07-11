tied-status
===========

``iati-activities/iati-activity/transaction/tied-status``

This is the reference page for the XML element ``tied-status``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: tied-status

Definition
~~~~~~~~~~


Optional element to override the top-level default-tied-status element on a transaction-by-transaction basis if needed.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/tied-status/.code:

@code
  An IATI code interpreting the usage of Columns 36-38 of the CRS++ reporting format. (Amount tied, Amount partially untied, Amount tied)

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`TiedStatus codelist </codelists/TiedStatus>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``tied-status`` of a ``transaction`` in an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*5*) from the *TiedStatus* codelist.

| Note: The ``tied-status`` element can override the ``default-tied-status`` value set in ``iati-activity``:

.. literalinclude:: ../../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--transaction starts-->
	:end-before: <!--transaction ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1281>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/tied-status.rst>`_

