default-tied-status
===================

``iati-activities/iati-activity/default-tied-status``

This is the reference page for the XML element ``default-tied-status``. See also the relevant overview page: :doc:`/activity-standard/overview/classifications` 

.. index::
  single: default-tied-status

Definition
~~~~~~~~~~


Whether the aid is untied, tied, or partially tied. This
element specifies a default for all the activity's financial
transactions; it can be overridden at the individual
transaction level.

If an activity is partially tied it is recommended that tied
and untied commitments are reported as separate transactions
and that transaction/tied-status is used to classify them.


Rules
~~~~~








This element must occur no more than once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/default-tied-status/.code:

@code
  An IATI code interpreting the usage of Columns 36-38 of the
  CRS++ reporting format. (Amount tied, Amount partially
  untied, Amount tied)

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`TiedStatus codelist </codelists/TiedStatus>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``default-tied-status``  for an ``iati-activity``.

| The ``@code`` attribute declares a valid code (*3*) from the *TiedStatus* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--default-tied-status starts-->
	:end-before: <!--default-tied-status ends-->
	
Changelog
~~~~~~~~~

2.01
^^^^
Freetext is `no longer allowed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#freetext-amended-elements>`__  within this element.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L787>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/default-tied-status.rst>`_

