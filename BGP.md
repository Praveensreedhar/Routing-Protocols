# BGP 
BGP is used to exchange route between different Autonomous systems. BGP exchanges network rechability informantion (NLRI) to other ASs for exchanging route informations.

##  Autonomous System Numbers

Organisations require Autonomous System Numbers(AS) to communicate to internet. AS is a four  byte providing  65,535 AS numbers for assigning.  64,512–65,535 Private autonomous systems and rest can use publicaly.

##  BGP Path Attributes

BGP uses path attribute associated with each network path. BGP path attributes are classified as follows.

### 1. Well-known mandatory
### 2. Well-known discretionary
### 3. Optional transitive
### 4. Optional nontransitive

### Well-known mandatory

Well-known mandatory attribute must be reconginised by all bgp routers.
This attribute is present in all BGP update and passed to all other BGP routers.
#### a) Origin
#### b) AS-Path
#### c) Next-hpoe

### Well-known discretionary

Well-known discretionary must be recognized by all BGP routers and passed on to other BGP routers but need not be present in an update

#### a) Local-Preferece 
#### b) Attomic-aggregate

### Optional transitive

This type of attribute is optoinal, means either understood by the router or not.
Transitive means that if it exists the router will always include it in the updates it sends out.
If the router doesn't understand the attribute it will also mark it as partial when sending it.

#### a) Aggregator
#### b) Community

### Optional non-transitive

This type of attribute is optoinal, means either understood by the router or not.
non-transitive means once received it will never pass it on to other Ebgp neighbors (non-transitive between AS, just did a test on GNS3 with MED and it gets propagated within the AS).

#### a) MED
#### b) Orginator ID
#### c) Cluster list

