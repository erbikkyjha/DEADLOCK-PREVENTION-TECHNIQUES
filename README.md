# DEADLOCK-PREVENTION-TECHNIQUES

ONE-SHOT ALGORITHM [21]
In one shot algorithm one protocol requires each process to request and be allocated all its
resources before it begins execution. Given a request from process P for resources R1, R2,
..., Run, the resource manager follows these rules
if process P has ever acquired any resources before, then refuse the request
else if any resource R1, ... Rn does not exist then
refuse the request
else
{if any resource R1, ... Rn is not free, then wait until all resources R1, ... Rn are free end if
grant process P exclusive access to resources R1, ... Rn} end
EXAMPLE: -
Suppose that a person needs both a knife and fork to eat.
Person P1 needs knife and fork and person P2 needs knife and fork.
Person P1 requests knife and fork, person P2 also requests knife and fork.
Only one of P1 or P2 will be granted the resources.
Suppose it is P1. P2 is forced to wait.
Person P1 uses the knife and fork until finished.
Person P1 releases the knife and fork.
Since the resources that P2 was waiting for are free, P2 is granted both the knife and fork.
Person P2 uses the knife and fork until finished. Person P2 releases the knife and fork.
MULTISHOT ALGORITHM [21]
In multishot or repeated one shot algorithm, an alternative protocol allows a process to
request resources only when the process has none. A process may request some resources
and use them. Before it can request any additional resources, however, it must release all the
resources that it is currently allocated.
Given a request from process P for resources R1, R2, ..., Rn, the resource manager
follows a similar rule to that for one-shot
if process P currently has any resources,
then refuse the request
else if any resource R1, ... Rn, does not
exist, then refuse the request else
{ if any resource R1, ... Rn is not free,
then wait until all resources R1, ... Rn are free end if
grant process P exclusive access to resources R1, ...
Rn }
end if
If a process P wants to request resources while holding resources, they follow these steps:
P frees all resources being held P requests all resources previously held plus the new
resources it wants to acquire.
HIERARCHICAL ALGORITHM [21]
Assume the resources have unique priorities (i.e., all priorities are different). Given a
request from process P for resource R, the resource manager follows these rules:
if process P currently has any resources with equal or higher priority than
resources R, then
refuse the request
else if resource R1 does not exist, then
refuse the request else
{
if the resource R is not free, then wait until resource R is free
end if
grant process P exclusive access to resources R
} end if
EXAMPLE:
Suppose that a person needs both a knife and fork to eat. Knife is given priority 2 and fork
priority 1, assuming that zero is the highest priority. Person P1 needs knife and fork and
person P2 needs knife and fork. Person P1 requests knife first because it is lower priority and
then fork. Person P2 also requests knife and then fork. Only one of P1 or P2 will be granted
the knife. Suppose it is P1. Person P2 will wait for the knife to be free. Then only P1 will
request the fork. The request will be granted. Person P1 will use the knife and fork until
finished. Person P1 will release the knife and fork. Since person P2 is waiting for the knife,
the request can now be granted. Then Person P2 will immediately request the fork and this
request will also be granted. Person P2 will use the knife and fork until finished. Person P2
will release the knife and fork.
