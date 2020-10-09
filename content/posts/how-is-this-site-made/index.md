---
draft: false
resources: []
title: What's up?
pubdate: 2020-10-9

---

Couple of things. 

I got a new server. It's got 4 HDs with uhh...

```
lscpu
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   40 bits physical, 48 bits virtual
CPU(s):                          16
On-line CPU(s) list:             0-15
Thread(s) per core:              2
Core(s) per socket:              4
Socket(s):                       2
NUMA node(s):                    2
Vendor ID:                       GenuineIntel
CPU family:                      6
Model:                           26
Model name:                      Intel(R) Xeon(R) CPU           X5560  @ 2.80GHz
Stepping:                        5
CPU MHz:                         1761.227
CPU max MHz:                     2800.0000
CPU min MHz:                     1600.0000
BogoMIPS:                        5598.27
Virtualization:                  VT-x
L1d cache:                       256 KiB
L1i cache:                       256 KiB
L2 cache:                        2 MiB
L3 cache:                        16 MiB
NUMA node0 CPU(s):               0,2,4,6,8,10,12,14
NUMA node1 CPU(s):               1,3,5,7,9,11,13,15
Vulnerability Itlb multihit:     KVM: Mitigation: Split huge pages
Vulnerability L1tf:              Mitigation; PTE Inversion; VMX conditional cache flushes, SMT vulnerable
Vulnerability Mds:               Vulnerable: Clear CPU buffers attempted, no microcode; SMT vulnerable
Vulnerability Meltdown:          Mitigation; PTI
Vulnerability Spec store bypass: Mitigation; Speculative Store Bypass disabled via prctl and seccomp
Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
Vulnerability Spectre v2:        Mitigation; Full generic retpoline, IBPB conditional, IBRS_FW, STIBP conditional, RSB filling
Vulnerability Srbds:             Not affected
Vulnerability Tsx async abort:   Not affected
Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ht tm pbe syscall nx rdtscp lm constant_tsc arch_pe
                                 rfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf pni dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm dca sse4_1 sse4_2 popcnt lahf_l
                                 m pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid dtherm ida flush_l1d

lsmem
RANGE                                  SIZE  STATE REMOVABLE  BLOCK
0x0000000000000000-0x00000000dfffffff  3.5G online       yes   0-27
0x0000000100000000-0x000000081fffffff 28.5G online       yes 32-259

Memory block size:       128M
Total online memory:      32G
Total offline memory:      0B

lsblk
NAME                                         MAJ:MIN RM   SIZE RO TYPE MOUNTPOINT
loop0                                          7:0    0    55M  1 loop /snap/core18/1880
loop1                                          7:1    0  71.3M  1 loop /snap/lxd/16099
loop2                                          7:2    0  29.9M  1 loop /snap/snapd/8542
loop3                                          7:3    0  55.3M  1 loop /snap/core18/1885
loop4                                          7:4    0  30.3M  1 loop /snap/snapd/9279
loop5                                          7:5    0  70.6M  1 loop /snap/lxd/16922
sda                                            8:0    0 136.7G  0 disk
├─sda1                                         8:1    0     1M  0 part
└─sda2                                         8:2    0 136.7G  0 part /
sdb                                            8:16   0 136.7G  0 disk
└─ceph--597b9aeb--35b9--4cc2--8a7b--a7d1c618d801-osd--data--d2a9958e--c9f3--4957--a29c--ae3f6685ce4d
                                             253:1    0 136.7G  0 lvm
sdc                                            8:32   0 136.7G  0 disk
└─ceph--f36b6efb--f61e--47cf--a20f--0eba4056099a-osd--data--d06fa426--89ce--415d--adfc--56bbe2c78a79
                                             253:2    0 136.7G  0 lvm
sdd                                            8:48   0 136.7G  0 disk
└─ceph--ab7c8948--fd80--4b38--86ab--1db07e9af8b2-osd--data--09c336e3--8c7d--43ed--94e0--424d5ba21f24
                                             253:0    0 136.7G  0 lvm
rbd0                                         252:0    0    10G  0 disk /var/lib/kubelet/pods/8e93a254-f19e-43b8-bdc1-ed92a6c2bdf4/volumes/kubernetes.io~csi/pvc-b03313ab-e883-4d1e-baa4-23e0b2338b24/mount
rbd1                                         252:16   0    40G  0 disk /var/lib/kubelet/pods/d99dcd17-6801-4816-8a92-19ee8917de9c/volumes/kubernetes.io~csi/pvc-8d943f7a-fe11-4e6b-afbc-3224360e3b38/mount
```
That. If you can tell I've done a few things to it off the bat. 

All declerative and remakable. I like it a lot. The practice of k8s and gitops. That's what I'll post here mostly. Feel free to follow along.

Other than that, life is well.