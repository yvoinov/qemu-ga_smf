=============================================================
qemu-ga SMF Installation & Remove        (C) 2025 Yuri Voinov
=============================================================

***  WARNING!  The  default  package  set  to  run  qemu-ga,
installed in /usr/local!

This set of scripts for installation and removal SMF service
for qemu-ga daemon for OpenIndiana Hipster and above.

All  the  necessary  prerequisites needed to run the service
qemu-ga,  according  to  the manual configuration (excluding
the  actual  configuration  of qemu-ga) performed during the
installation  of  service,  removal  service SMF removes all
scripts and performs deregister service qemu-ga and stop.

To activate the qemu-ga SMF follow these steps:
------------------------------------------------------------

1.  Set up the qemu-ga and all necessary libraries, if it is
not already.

2.   Configure   the   qemu-ga  editing  qemu-ga.conf  (when
applicable).

***  WARNING!  The  default  package  set  to  run  qemu-ga,
installed in /usr/local!

4. Run the script qemu-ga_smf_inst.sh, that performs all the
necessary  prerequisites  and  post actionû and will install
qemu-ga SMF service.

5.  Run  the  command  svcadm enable qemu-ga to activate and
start the service qemu-ga.

To  deactivate  and remove qemu-ga SMF service, follow these
steps:
------------------------------------------------------------

1. Start the script qemu-ga_smf_rmv.sh. The script stops all
running  qemu-ga  processes,  de-registers  SMF service, and
completely   removes   SMF  and  rolls  back  the  operation
performed earlier in the activation of the service.

*** Note: Removal of qemu-ga SMF service does not remove the
installed software qemu-ga.

Archive contains:

init.qemu-ga        - Managing method qemu-ga SMF
qemu-ga.xml         - Service manifest qemu-ga SMF
readme_ru.txt         - Ýòîò ôàéë (Russian)
readme_en.txt         - This file (English)
qemu-ga_smf_inst.sh    - SMF Installation script
qemu-ga_smf_rmv.sh     - SMF Removal script
 
=============================================================
qemu-ga SMF Installation & Remove        (C) 2025 Yuri Voinov
=============================================================