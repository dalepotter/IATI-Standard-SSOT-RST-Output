default-flow-type
=================

``iati-activities/iati-activity/default-flow-type``

This is the reference page for the XML element ``default-flow-type``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: default-flow-type

Definition
~~~~~~~~~~


Whether the activity is funded by Official Development
Assistance (ODA), Other Official Flows (OOF), etc


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/default-flow-type/.code:

@code
  A code from the OECD DAC CRS "Type of flow" codelist

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`FlowType codelist </codelists/FlowType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``default-flow-type``  for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*10*) from the *FlowType* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--default-flow-type starts-->
	:end-before: <!--default-flow-type ends-->

Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L452>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/default-flow-type.rst>`_

