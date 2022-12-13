# DPDK-Project
DNS server based on DPDK 

## Phase-1:
 - Setup with memif interface between 2 DPDK process
 - Setup with memif pktgen and testpmd
 - setup with memif pktgen and possible applciation (dns resolver)
 - send and recieve packet from dns-resolver (no processing) for 10Gbps line rate

## phase-2:
 - use SW packet parsing for UDP port 53
 - identify if DNS is request|response
 - count the request-response
 - Setup the enviroment with physical niC
 - use UDP RSS to send to multiple queue
 - process DNS request|response per queue
 - aggregate and dispaly stats

## phase-3:
 - process DNS request from HW NIC using RSS and PTYPE
 - create response on seperate buffer
 - create response on orginal request

## phase-4:
 - improve dns lookup with hash and crc
 - improve dns lookup with LPM
 - use hyperscan to do string regex matching

## phase 5:
 - consolidate the learning and findings into whitepaper.
