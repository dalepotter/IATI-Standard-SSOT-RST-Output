budget-line
===========

``iati-organisations/iati-organisation/recipient-country-budget/budget-line``

This is the reference page for the XML element ``budget-line``. See also the relevant overview page: :doc:`/organisation-standard/overview/budgets` 

.. index::
  single: budget-line

Definition
~~~~~~~~~~


A breakdown of the recipient country's budget into
sub-totals.  The breakdown is determined by the
reporting organisation and described in the narrative.
The period covered is the same as that covered by the
parent recipient-country-budget element. The sum of
budget-line values does not have to equal the value
given in the parent element.


Rules
~~~~~








This element may occur any number of times.







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/recipient-country-budget/budget-line/.ref:

@ref
  An internal reference for this budget line taken
  from the reporting organisation's own system.
  Optional.


  This value must be of type xsd:string.



  



Example Usage
~~~~~~~~~~~~~
Example ``budget-line`` for ``recipient-country-budget`` of an ``iati-organisation``.

| An example ``@ref`` attribute is included.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--recipient-country-budget starts-->
	:end-before: <!--recipient-country-budget ends-->

| The ``budget-line`` element can be repeated in any ``recipient-country-budget``.


Changelog
~~~~~~~~~

2.01
^^^^
| The ``budget-line`` element was `added <http://iatistandard.org/upgrades/integer-upgrade-to-2-01/2-01-changes/#budget-line-new-element>`__ as a child element of ``recipient-country-budget``.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L598>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/recipient-country-budget/budget-line.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   budget-line/value
   budget-line/narrative

