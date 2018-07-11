total-expenditure
=================

``iati-organisations/iati-organisation/total-expenditure``

This is the reference page for the XML element ``total-expenditure``. 

.. index::
  single: total-expenditure

Definition
~~~~~~~~~~


The total-expenditure element allows for the reporting of the
organisation’s international development expenditure. The
recommendation is that, where and when possible, the organisation’s
total expenditure for each of the past three years is reported.
The expense line allows publishers to record further breakdown.


Rules
~~~~~








This element may occur any number of times.








Example Usage
~~~~~~~~~~~~~
| Example of ``total-expenditure`` for an ``iati-organisation``.

| This element is a parent for other child elements.

.. code-block:: xml

	<total-expenditure>
	...
	</total-expenditure>

| Full example with all child elements.

.. literalinclude:: ../../organisation-standard-example-annotated.xml
	:language: xml
	:start-after: <!--total-expenditure starts-->
	:end-before: <!--total-expenditure ends-->

| The ``total-expenditure`` element can be repeated in any ``iati-organisation``.

Changelog
~~~~~~~~~
2.02
^^^^
The optional ``total-expenditure`` element was `added <http://support.iatistandard.org/entries/83404469-Add-Total-Expenditure-Element-To-Organisation-File>`__.


Developer tools
~~~~~~~~~~~~~~~

Find the source of this documentation on github:

* `Schema <https://github.com/IATI/IATI-Schemas/blob/version-2.03/iati-organisations-schema.xsd#L652>`_
* `Extra Documentation <https://github.com/IATI/IATI-Extra-Documentation/blob/version-2.03/en/organisation-standard/iati-organisations/iati-organisation/total-expenditure.rst>`_


Subelements
~~~~~~~~~~~

.. toctree::
   :titlesonly:
   :maxdepth: 1

   total-expenditure/period-start
   total-expenditure/period-end
   total-expenditure/value
   total-expenditure/expense-line

