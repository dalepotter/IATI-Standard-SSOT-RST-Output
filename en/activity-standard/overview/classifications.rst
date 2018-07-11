Classifications
===============

Definition
----------
Within the **IATI activity standard** it is expected that *classifications* information is provided for any ``iati-activity``

Namely:

* ``sector`` - the thematic catgory (or set of categories) an ``iati-activity`` operates with

Additionally, the following classifications enable the publication of various codes (often associated with CRS++ reporting)

* ``policy-marker``
* ``collaboration-type``
* ``default-finance-type``
* ``default-flow-type``
* ``default-aid-type``
* ``default-tied-status``


Considerations
--------------
When using the **IATI activity standard** to declare *documents*, the following should be considered:

* An ``iati-activity`` can have singular or multiple ``sector``
* When multiple ``sector`` are described, then a ``@percentage`` should be declared for each.  This should sum to 100% for each ``iati-activity``.
* A ``@vocabulary`` can be declared when describing a ``sector``.  This should be on the *Vocabulary* codelist.
* If no ``@vocabulary`` is declared, then the :doc:`DAC 5 digit codelist </codelists/Sector>` is assumed.
* A ``reporting-org`` can declare their own ``@vocabulary``, via using the *RO* (Reporting Org) *Vocabulary* code.
* Multiple or singular ``policy-marker`` can also be described.  Unlike ``sector``, a percentage is not required.
* The classifications of ``default-finance-type``, ``default-flow-type``, ``default-aid-type`` and ``default-tied-status`` apply to the whole ``iati-activity``.  These can be overridden within a single ``transaction`` via using any of ``finance-type`` , ``flow-type`` , ``aid-type`` and/or ``tied-status``.
* If an ``iati-activity`` is either wholly *tied*, *partially tied* or *untied* it is recommended that the appropriate ``default-tied-status`` code is used.
* If an ``iati-activity`` has more than one *tied status* it is recommended that the reported commitment(s) are split into the relevant tied, untied and/or partially-tied amounts and ``tied-status`` is reported at ``transaction`` level. (NB that tied status should be reported for commitments only.)

2.01+ Considerations
--------------------
In versions 2.01 and above, the following must also be considered:

* A ``sector`` is mandatory.
* Descriptive text / name is no longer supported for any classification elements. 
* A ``sector`` can also be published as child elements of a ``transaction``.  When this is done, it is expected that **all** ``transaction`` include such data, whilst ``sector`` is subsequently **not** included at the ``iati-activity`` level. 


Reference pages
---------------


* :doc:`sector </activity-standard/iati-activities/iati-activity/sector>`

* :doc:`policy-marker </activity-standard/iati-activities/iati-activity/policy-marker>`

* :doc:`default-flow-type </activity-standard/iati-activities/iati-activity/default-flow-type>`

* :doc:`default-finance-type </activity-standard/iati-activities/iati-activity/default-finance-type>`

* :doc:`collaboration-type </activity-standard/iati-activities/iati-activity/collaboration-type>`

* :doc:`default-aid-type </activity-standard/iati-activities/iati-activity/default-aid-type>`

* :doc:`default-tied-status </activity-standard/iati-activities/iati-activity/default-tied-status>`
