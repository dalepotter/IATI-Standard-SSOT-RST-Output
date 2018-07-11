other-identifier
================

``iati-activities/iati-activity/other-identifier``

This is the reference page for the XML element ``other-identifier``. 

.. index::
  single: other-identifier

Definition
~~~~~~~~~~


An other identifier for the activity. This may be a publishers
own identifier that it wishes to record with the activity.
This element is also used to trace changes to activity
identifiers, for example when and organisation has changed
it's organisation identifier.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-activities/iati-activity/other-identifier/.ref:

@ref
  The identifier you wish to report.
  This can be used to report a number of different types
  of identifiers. See the OtherIdentifierType codelist
  for details and options.

  This attribute is required.



  This value must be of type xsd:string.



  
.. _iati-activities/iati-activity/other-identifier/.type:

@type
  The type of identifier being reported, taken from
  the OtherIdentifierType codelist.

  This attribute is required.



  This value must be of type xsd:string.


  This value must be on the :doc:`OtherIdentifierType codelist </codelists/OtherIdentifierType>`.



  



Example Usage
~~~~~~~~~~~~~
Example ``other-identifier`` of an ``iati-activity``.

| An example ``@ref`` of *ABC123-XYZ* is declared.
| The ``@type`` attribute declares a valid code (*A1*) from the *OtherIdentifierType* codelist.

.. literalinclude:: ../../activity-standard-example-annotated.xml
	:language: xml
	:start-after: <!--other-identifier starts-->
	:end-before: <!--other-identifier ends-->

2.01
^^^^
| Freetext support of the ``other-identifier`` was removed.  A new ``other-identifier/@ref`` was `added as a replacement <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#other-identifier-removed-new-attributes>`__.

| A new attribute ``other-identifier/@type`` was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#other-identifier-removed-new-attributes>`__, to be used with new code list *OtherIdentifierType*.

| The ``other-identifier/@owner-ref`` and ``other-identifier/@owner-name`` attributes were `removed <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#other-identifier-removed-new-attributes>`__.

| The ``owner-org`` child element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/##other-identifier-new-child-elements>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-activities-schema.xsd#L508>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/activity-standard/iati-activities/iati-activity/other-identifier.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   other-identifier/owner-org

