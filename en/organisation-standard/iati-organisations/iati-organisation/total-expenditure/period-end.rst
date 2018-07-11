period-end
==========

``iati-organisations/iati-organisation/total-expenditure/period-end``

This is the reference page for the XML element ``period-end``. 

.. index::
  single: period-end

Definition
~~~~~~~~~~


The end of the period (which must not be greater than one year)


Rules
~~~~~








This element must occur once and only once (within each parent element).







Attributes
~~~~~~~~~~


.. _iati-organisations/iati-organisation/total-expenditure/period-end/.iso-date:

@iso-date
  

  This attribute is required.



  This value must be of type xsd:date.



  ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``



Example Usage
~~~~~~~~~~~~~
Example ``period-end`` of ``total-expenditure`` for an ``iati-organisation``.

| An example date is declared in the ``@iso-date`` attribute.
| This example date format conform to the *xsd:date* standard - for most cases *YYYY-MM-DD* is sufficient.

.. literalinclude:: ../../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--total-expenditure starts-->
	:end-before: <!--total-expenditure ends-->

Changelog
~~~~~~~~~
2.02
^^^^
The optional ``total-expenditure`` element was `added <http://support.iatistandard.org/entries/83404469-Add-Total-Expenditure-Element-To-Organisation-File>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L678>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/total-expenditure/period-end.rst>`_

