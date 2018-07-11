flow-type
=========

``iati-activities/iati-activity/transaction/flow-type``

This is the reference page for the XML element ``flow-type``. See also the relevant overview page: :doc:`/activity-standard/overview/transactions` 

.. index::
  single: flow-type

Definition
~~~~~~~~~~


Optional element to override the top-level default-flow-type element.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/transaction/flow-type/.code:

@code
  A code from the OECD DAC CRS "Type of flow" codelist

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FlowType codelist </codelists/FlowType>`.



  



Example Usage
~~~~~~~~~~~~~
Example usage of ``flow-type`` of a ``transaction`` in an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*20*) from the *FlowType* codelist.

| Note: The ``flow-type`` element can override the ``default-flow-type`` value set in ``iati-activity``:

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

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L1234>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/transaction/flow-type.rst>`_

