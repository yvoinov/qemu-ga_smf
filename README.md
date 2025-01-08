# OpenSolaris QEMU guest agent SMF
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://github.com/yvoinov/qemu-ga_smf/blob/master/LICENSE)

By default, QEMU guest agent binaries are supposed to be located in /usr/local (the build from sources assumes this prefix by default).

OpenSolaris not supported virtual-console (yet?), so qemu-ga utilizes ISA serial to communicate with VM.

When deleting the service, the QEMU guest agent daemon stops.

Follow these steps to enable QEMU guest agent SMF:

1. Build and install QEMU guest agent if not already installed.

2. Check and verify qemu-ga config in method script.

3. Run the qemu-ga_smf_inst.sh script, which will perform all installation steps and install the QEMU guest agent SMF service.

3. Run `svcadm enable qemu-guest-agent` command to enable and start the QEMU guest agent service.

To deactivate and remove the QEMU guest agent SMF service, follow these steps:

1. Run the qemu-ga_smf_rmv.sh  script. The script stops all running QEMU guest agent process, unregisters the SMF service, completely removes the QEMU guest agent SMF and rolls back the operations performed earlier when the service was activated.

Note: Removing the QEMU guest agent SMF service does not remove the installed QEMU guest agent software.
