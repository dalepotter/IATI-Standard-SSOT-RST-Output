



//result/indicator/period
-------------------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//recipient-org-budget
----------------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//recipient-region-budget
-------------------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//planned-disbursement
----------------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//iati-activity
---------------


* ``activity-date[@type='1' or @type='2']`` must be present.

* Either ``sector`` or ``transaction/sector`` must be present.

* Either ``transaction/sector`` or ``sector`` must be present.

* ``reporting-org/@ref`` should match the regex ``[^\/\&\|\?]+``

* ``iati-identifier`` should match the regex ``[^\/\&\|\?]+``

* ``participating-org/@ref`` should match the regex ``[^\/\&\|\?]+``

* ``transaction/provider-org/@ref`` should match the regex ``[^\/\&\|\?]+``

* ``transaction/receiver-org/@ref`` should match the regex ``[^\/\&\|\?]+``

* ``activity-date[@type='1']/@iso-date`` must be before or the same as ``activity-date[@type='3']/@iso-date``

* ``activity-date[@type='2']/@iso-date`` must be before or the same as ``activity-date[@type='4']/@iso-date``

* ``activity-date[@type='2']/@iso-date`` must not be in the future.

* ``activity-date[@type='4']/@iso-date`` must not be in the future.

* The sum of values matched at ``recipient-country/@percentage`` and ``recipient-region/@percentage`` must be ``100``.

* The sum of values matched at ``recipient-region/@percentage`` and ``recipient-country/@percentage`` must be ``100``.




//iati-organisation
-------------------


* ``reporting-org/@ref`` should match the regex ``[^\/\&\|\?]+``

* ``organisation-identifier`` should match the regex ``[^\/\&\|\?]+``




//budget
--------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//result/indicator[@measure='1' or @measure='2' or @measure='3' or @measure='4']/period/actual
----------------------------------------------------------------------------------------------


* ``@value`` must be present.




//participating-org
-------------------


* Either ``@ref`` or ``narrative`` must be present.

* Either ``narrative`` or ``@ref`` must be present.




//result/indicator[@measure='1' or @measure='2' or @measure='3' or @measure='4']/period/target
----------------------------------------------------------------------------------------------


* ``@value`` must be present.




//result/indicator[@measure='1' or @measure='2' or @measure='3' or @measure='4']/baseline
-----------------------------------------------------------------------------------------


* ``@value`` must be present.




//total-budget
--------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//result/indicator
------------------


* There must be no more than one element or attribute matched at ``reference[1]`` or ``../reference[1]``.

* There must be no more than one element or attribute matched at ``../reference[1]`` or ``reference[1]``.




//transaction
-------------


* ``transaction-date/@iso-date`` must not be in the future.

* ``value/@value-date`` must not be in the future.




//recipient-country-budget
--------------------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``




//total-expenditure
-------------------


* ``period-start/@iso-date`` must be before or the same as ``period-end/@iso-date``


