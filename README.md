# MPTCP Receiver Side Out-of-Order Packet Handling

This repository contains a patch and packetdrill test cases for the out-of-order packet queue handling of the [Multipath TCP kernel](https://www.multipath-tcp.org/) implementation developed for the [programmable Multiapth TCP scheduler ProgMP](https://progmp.net).

Without this patch, the MPTCP kernel only pushes in-order packets with regard to the subflow sequence number to the meta socket.

A more efficient patch/implementation might track for each subflows out-of-order queue if the queue is in the data sequence number order to avoid iterations on the queues.

The current patch is for [MPTCP version 0.90](https://github.com/multipath-tcp/mptcp/tree/mptcp_v0.90).