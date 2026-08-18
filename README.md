# Patent Invention Specification

## System and Method for Authorising Geographically Remote Electric Vehicle Charging Using Energy Associated with a Domestic Energy System

### 1. Technical Field

The present invention relates generally to electric vehicle charging, distributed energy systems, domestic energy storage, smart electricity networks, energy management systems, authentication systems and public charging infrastructure.

More particularly, the invention relates to a system and method by which a user associated with a domestic energy system can authenticate that system to a geographically remote electric vehicle charging station and authorise delivery of electrical energy to an electric vehicle at the remote charging station, wherein the quantity or cost of energy delivered at the remote charging station is associated with, allocated against, compensated by, or otherwise controlled in relation to energy available from or associated with the user's domestic energy system.

The invention may be implemented using domestic batteries, solar photovoltaic systems, smart meters, domestic energy-management systems, energy suppliers, aggregators, electricity networks, energy accounts or combinations thereof.

---

## 2. Background

Electric vehicles are increasingly charged using public charging infrastructure.

A conventional public charging station generally obtains electrical energy from the electricity network at the location of the charging station. The vehicle user is then charged for the electrical energy delivered to the vehicle and, in some cases, for associated infrastructure or parking services.

Many households, however, have domestic energy resources including:

- rechargeable domestic batteries;
- solar photovoltaic generation;
- domestic energy-management systems;
- smart meters;
- time-of-use electricity tariffs;
- dynamic electricity tariffs;
- electricity import or export arrangements;
- vehicle-to-home systems;
- vehicle-to-grid systems; and
- other distributed energy resources.

A user may therefore have access to electrical energy or an energy-related financial entitlement at their home while being geographically separated from their electric vehicle.

This creates a particular problem for users who do not have convenient private parking or who cannot install a domestic EV charging point adjacent to their vehicle.

For example, a user may have a domestic battery containing 8 kWh of usable energy but may park an electric vehicle several streets away from their home. The user may wish to utilise energy associated with the domestic battery for charging the vehicle.

Physically transmitting electricity from the domestic battery to the geographically remote vehicle would generally require a dedicated electrical connection and is therefore impractical in many circumstances.

There is therefore a need for a system capable of separating the **physical location of electrical energy delivery** from the **location and identity of the user's authorised domestic energy resource**.

---

## 3. Problem Addressed by the Invention

The invention addresses the problem of allowing an authorised user to utilise energy associated with a domestic energy resource for charging an electric vehicle at a geographically remote charging station without requiring a dedicated physical electrical connection between the domestic energy resource and the remote charging station.

A further problem is preventing unauthorised users from accessing the domestic energy resource or consuming an energy allocation associated with that resource.

A further problem is determining how much energy may safely or economically be allocated for remote charging while preserving a minimum domestic energy reserve.

A further problem is reconciling the electrical energy physically delivered at the remote charging station with the user's domestic energy account, energy resource or energy entitlement.

---

## 4. Summary of the Invention

According to a first aspect of the invention, there is provided an energy management system comprising:

1. a domestic energy resource associated with a user;
2. a remote electric vehicle charging station geographically separated from the domestic energy resource;
3. an authentication system configured to authenticate the user;
4. a domestic energy interface configured to obtain information relating to energy available from or associated with the domestic energy resource;
5. a remote charging interface configured to communicate with the remote electric vehicle charging station;
6. an authorisation engine configured to generate a remote charging authorisation based at least partly on the authenticated identity of the user and the energy information obtained from the domestic energy resource; and
7. an energy accounting or allocation system configured to associate electrical energy delivered by the remote electric vehicle charging station with the domestic energy resource or an energy account associated with the user.

The physical electrical energy supplied to the vehicle may be obtained from the electricity network at the remote charging station.

The domestic energy resource may therefore be physically separate from the remote charging station while the system maintains an electronic association between the domestic energy resource and the energy supplied to the vehicle.

---

## 5. Core Concept

The invention can be understood as creating an **energy bridge without necessarily creating a physical electrical bridge**.

```text
             USER'S HOME

       +-----------------------+
       | Solar PV              |
       |     |                 |
       |     v                 |
       | Home Battery          |
       |     |                 |
       | Smart Meter           |
       |     |                 |
       | Energy Management     |
       +----------+------------+
                  |
                  | authenticated
                  | energy information
                  v
          +-----------------+
          | ENERGY CONTROL  |
          | PLATFORM        |
          +--------+--------+
                   |
                   | temporary
                   | authorisation
                   v
          +-----------------+
          | REMOTE STREET   |
          | CHARGING POST   |
          +--------+--------+
                   |
                   | electricity
                   v
                  EV
```

The electricity physically delivered to the vehicle can therefore originate from the local electricity network while the system records, allocates, compensates or otherwise associates that energy with the user's authorised domestic energy resource.

---

## 6. Definitions

### Domestic energy resource

An energy storage system, energy generation system, smart meter, electricity account, domestic energy management system, electricity supply arrangement, energy credit or combination thereof associated with a user or premises.

### Remote charging station

An electric vehicle charging station located geographically separately from the domestic energy resource.

### Energy allocation

An electronically maintained quantity, value, credit, entitlement, accounting quantity or other representation associated with energy available from, supplied by, exported by, stored by or otherwise associated with a domestic energy resource.

### Energy authorisation

An electronically generated permission allowing a specified charging station to deliver a specified amount or value of electrical energy to a specified vehicle or user.

### Domestic reserve

An amount of energy that the system is configured to retain at the domestic energy resource and which is not available for remote allocation.

---

## 7. Detailed Description

### 7.1 Domestic Energy Resource

In one embodiment, the domestic energy resource comprises a rechargeable battery located at a user's home.

The battery may comprise:

- a lithium-ion battery;
- a sodium-ion battery;
- a flow battery;
- another rechargeable energy-storage device; or
- a combination of energy storage devices.

The domestic energy resource may communicate with an energy-management controller.

The controller may provide information including:

- battery state of charge;
- available capacity;
- maximum permitted discharge;
- minimum reserve;
- instantaneous household demand;
- expected household demand;
- battery temperature;
- battery health;
- battery charging state;
- electricity tariff;
- predicted solar generation;
- predicted household consumption; and
- permitted remote-energy allocation.

---

## 8. Domestic Energy Reserve

In one embodiment, the system prevents the entire domestic battery from being allocated to remote charging.

For example:

```text
Battery capacity:             13.5 kWh
Current state of charge:      82%
Energy stored:                11.07 kWh
Required domestic reserve:     5.00 kWh
Operating reserve:             1.00 kWh
Available remote allocation:  5.07 kWh
```

The remote charging system may therefore receive an authorisation for no more than 5.07 kWh.

The domestic reserve may be dynamically calculated.

For example:

**Remote Allocation = Available Energy - Domestic Reserve - Safety Margin**

The domestic reserve may be increased automatically when predicted household consumption increases.

---

## 9. Dynamic Allocation

The available remote allocation may be calculated using information obtained from multiple sources.

```text
Battery state
      +
Household demand forecast
      +
Solar generation forecast
      +
Electricity tariff
      +
Battery health
      +
User-defined reserve
      +
Network restrictions
      =
Remote energy allocation
```

This permits the system to prevent remote charging from adversely affecting domestic electricity requirements.

---

## 10. User Authentication

A user may authenticate at the remote charging station using one or more of:

- mobile application;
- QR code;
- NFC;
- RFID;
- biometric authentication;
- vehicle identity;
- digital certificate;
- account credentials;
- cryptographic token;
- payment credential;
- device-to-device authentication; or
- a combination thereof.

The remote charging station need not receive the user's domestic energy supplier password.

Instead, the user may authenticate with an intermediary authorisation service or energy supplier.

The authorisation service may issue a temporary cryptographic token.

---

## 11. Supplier Authentication

In one embodiment, the user selects an energy supplier or energy service provider at the charging station.

The charging station may display:

```text
SELECT ENERGY PROVIDER

[ Supplier A ]

[ Supplier B ]

[ Supplier C ]

[ Other ]
```

The user may authenticate using their supplier's authentication system.

The supplier may then provide an authorisation to the energy-management platform without revealing the user's password to the charging station.

---

## 12. Energy Capability Request

Following authentication, the remote charging station may transmit an energy capability request.

For example:

```text
USER ID
VEHICLE ID
CHARGER ID
REQUESTED ENERGY = 7 kWh
MAXIMUM POWER = 7.2 kW
REQUEST EXPIRY = 30 minutes
```

The energy management platform may query the domestic energy resource.

The domestic energy resource may respond:

```text
AVAILABLE ENERGY = 5.4 kWh
MAXIMUM PERMITTED ALLOCATION = 4.8 kWh
MAXIMUM REMOTE POWER = 5 kW
```

The authorisation engine then generates a charging authorisation limited to those values.

---

## 13. Temporary Charging Authorisation

An authorisation may contain:

- Authorisation ID
- User identifier
- Charging station identifier
- Vehicle identifier
- Maximum energy
- Maximum power
- Start time
- Expiry time
- Energy source identifier
- Domestic reserve requirement
- Digital signature

The authorisation may be cryptographically signed.

The remote charging station verifies the signature before permitting charging.

---

## 14. Geographical Restrictions

The system may apply geographical restrictions.

For example, an energy allocation may be:

- valid at a particular charging station;
- valid within a defined geographical region;
- valid within a defined distance from a user's registered premises;
- valid only in a specified country;
- valid only within an authorised charging network; or
- unrestricted geographically.

A user could therefore be permitted to use their domestic energy allocation at charging stations throughout a participating charging network.

---

## 15. Physical Electricity Flow

In a preferred embodiment, the invention does not require electricity to physically travel from the domestic battery to the remote charging station.

Instead:

```text
HOME

Domestic Battery
      |
      v
Energy Management System
      |
      v
Energy Allocation
      |
      v
Authorisation Platform
      |
      v
Remote Charger


STREET

Electricity Grid
      |
      v
Remote Charger
      |
      v
Electric Vehicle
```

The remote charging station therefore receives electricity locally from the electricity network.

The system maintains an electronic relationship between that energy delivery and the user's domestic energy resource.

---

## 16. Alternative Physical Energy Transfer

In another embodiment, the domestic energy resource may physically supply electricity to the remote charging station.

For example, the domestic energy resource may be connected through:

- a private electrical network;
- a microgrid;
- an energy-storage network;
- a controllable distribution network; or
- another electrical transmission arrangement.

The invention therefore encompasses both:

1. electronically accounted energy transfer without physical remote electricity transmission; and
2. physically transmitted electrical energy.

---

## 17. Energy Accounting

When charging begins, the charging station records delivered energy.

For example:

```text
Charging started:       18:12:04
Energy authorised:      5.0 kWh
Energy delivered:       4.7 kWh
Charging stopped:       19:01:17
```

The charging station sends the measured value to the energy-management platform.

The platform then records:

```text
Remote charging allocation
--------------------------
Authorised:       5.0 kWh
Consumed:         4.7 kWh
Unused:           0.3 kWh
```

Unused energy may be returned to the user's available allocation.

---

## 18. Metering

The charging station may contain an electrical meter capable of measuring:

- voltage;
- current;
- power;
- cumulative energy;
- charging duration; and
- charging direction.

The meter may provide digitally signed measurement records.

This allows the system to distinguish between:

- Energy requested
- Energy authorised
- Energy physically delivered
- Energy actually consumed by vehicle
- Energy credited/debited

---

## 19. Energy Reconciliation

At the end of a charging session, the system may perform reconciliation.

For example:

```text
Domestic allocation       5.00 kWh
Remote energy delivered   4.70 kWh
Unused allocation         0.30 kWh
```

The 0.30 kWh may be returned to the available energy allocation.

Alternatively, the system may calculate a monetary or energy-value adjustment.

---

## 20. Tariff Integration

The system may obtain tariff information from the user's energy supplier.

The user may therefore specify:

> "Use my home energy when its effective cost is below the public charging tariff."

The system may compare:

```text
Domestic energy value
        vs
Remote charging price
```

and determine whether remote charging should be authorised.

---

## 21. Battery Degradation

In another embodiment, the system considers the estimated degradation cost associated with battery discharge.

For example:

```text
Battery energy value
+
Battery degradation cost
+
Network cost
+
Charging infrastructure cost
=
Effective remote energy cost
```

The system may therefore prevent an allocation if remote use would exceed a user-defined effective cost.

---

## 22. Multiple Domestic Energy Resources

A user may have multiple domestic energy resources.

For example:

```text
Home Battery
Solar Installation
Second Home Battery
Community Battery
Energy Account
```

The energy-management platform may select one or more resources.

The user may specify:

```text
Priority:

1. Solar-generated stored energy
2. Home battery
3. Energy credit
4. Grid energy
```

---

## 23. Multiple Vehicles

A user may have multiple authorised vehicles.

The system may associate individual charging permissions with:

- vehicle identity;
- registration;
- vehicle digital certificate;
- charging connector;
- mobile device; or
- user account.

A charging authorisation may therefore be restricted to a particular vehicle.

---

## 24. Parking Integration

In one embodiment, the charging post also functions as a parking-management terminal.

The system may combine:

- parking authorisation;
- charging authorisation;
- energy allocation;
- vehicle identification;
- payment;
- charging duration; and
- parking duration.

For example:

```text
PARKING

2 hours

CHARGING

Maximum 5 kWh

ENERGY SOURCE

My Home Energy
```

The charging station may therefore operate as a combined parking meter and energy terminal.

---

## 25. Energy Source Selection

The user may select:

### Mode A — Public electricity

The user purchases electricity normally.

### Mode B — Domestic energy allocation

The user uses an energy allocation associated with their domestic energy system.

### Mode C — Mixed

Part of the charging session is associated with domestic energy and the remainder is purchased normally.

For example:

```text
Requested:       10 kWh
Home allocation:  6 kWh
Public energy:    4 kWh
```

---

## 26. Dynamic Switching

The charging station may dynamically change between energy modes.

For example:

```text
18:00
Home allocation available
-> use domestic allocation

18:45
Domestic allocation exhausted
-> switch to public charging

19:00
User stops charging
```

The switching may occur without physical reconnection of the vehicle.

---

## 27. Security

The system may employ:

- public/private key cryptography;
- digital signatures;
- encrypted communications;
- short-lived authorisation tokens;
- device certificates;
- mutual authentication;
- secure hardware;
- tamper detection;
- replay protection;
- transaction identifiers; and
- audit logs.

The charging station may not receive unrestricted access to the user's domestic energy system.

Instead, it receives only a narrowly scoped authorisation.

---

## 28. Privacy

The system may use pseudonymous identifiers.

The remote charging station need not receive:

- the user's home address;
- complete domestic energy history;
- complete supplier account;
- battery history; or
- household consumption profile.

For example, the station may receive only:

```text
Authorised energy: 4.2 kWh
Maximum power:     7.2 kW
Expires:           20:30
```

---

## 29. Fault Handling

If communication with the domestic energy resource is interrupted, the charging station may:

1. stop charging immediately;
2. continue only until the existing authorisation expires;
3. continue until the authorised energy quantity is exhausted; or
4. switch to conventional paid charging.

The selected behaviour may be configurable.

---

## 30. Emergency Stop

The charging station may include a physical emergency stop.

Activation may immediately disable power delivery while preserving the transaction record.

---

## 31. Example Charging Sequence

A representative sequence is:

1. User parks an EV adjacent to a charging post.
2. User connects the EV to the charging post.
3. The charging post identifies the vehicle.
4. The user selects "Use Home Energy".
5. The user authenticates with their energy provider.
6. The energy provider confirms the user's identity and domestic energy resource.
7. The energy management platform obtains current energy availability.
8. The system calculates the permitted remote energy allocation.
9. A temporary charging authorisation is generated.
10. The charging station verifies the authorisation.
11. The charging station delivers electricity to the EV.
12. The charging station measures delivered energy.
13. The measured energy is reported to the energy management platform.
14. The energy allocation is reconciled.
15. The unused allocation, if any, is restored.
16. The transaction is closed.

---

## 32. Example

A user has:

```text
Domestic battery capacity       13.5 kWh
Battery state of charge          78%
Energy stored                    10.53 kWh
Domestic reserve                  5.00 kWh
Available remote allocation       5.53 kWh
```

The user requests:

```text
4.0 kWh
```

The system authorises:

```text
Maximum energy = 4.0 kWh
Maximum power = 7.2 kW
```

The vehicle receives:

```text
3.72 kWh
```

The remaining:

```text
0.28 kWh
```

is returned to the user's allocation.

---

## 33. Alternative Embodiment — Energy Credits

The invention is not restricted to directly measuring energy stored in a domestic battery.

The domestic energy system may instead generate an energy credit.

For example:

```text
Solar generation
       |
Domestic battery
       |
Energy exported
       |
Energy credit
       |
Remote EV charging
```

The energy credit may be represented in:

- kWh;
- monetary value;
- carbon-adjusted energy;
- tariff-adjusted energy; or
- another machine-readable unit.

---

## 34. Alternative Embodiment — Community Energy

Multiple users may participate.

```text
House A -+
House B -+--> Energy Platform --> Street Chargers
House C -+
```

Each user maintains a separate energy allocation.

The system prevents one user from consuming another user's allocation unless an explicit sharing rule exists.

---

## 35. Energy Sharing

A user may deliberately permit their energy allocation to be shared.

For example:

> "Allow my unused solar energy to be used for charging another authorised vehicle."

The system may then maintain separate ownership and usage records.

---

## 36. Geographic Energy Network

A plurality of charging posts may form a distributed network.

```text
              ENERGY PLATFORM
                    |
       +------------+------------+
       |            |            |
   Charger A    Charger B    Charger C
       |            |            |
      EV           EV           EV
```

A user's energy allocation may be used at any participating charging station subject to the user's permissions and network rules.

---

## 37. Mobile Application

A mobile application may provide:

- domestic energy availability;
- remote charging allocation;
- charging station map;
- charging history;
- energy history;
- authorisation status;
- battery reserve;
- tariff information;
- charging cost;
- energy remaining;
- vehicle selection; and
- remote charging controls.

---

## 38. Street Charging Post

The physical charging post may comprise:

1. housing;
2. charging connector;
3. electrical switching apparatus;
4. electrical meter;
5. communications module;
6. processor;
7. secure authentication module;
8. user interface;
9. payment interface;
10. emergency stop;
11. vehicle detection system;
12. parking-management interface; and
13. optional display.

The post may be installed at:

- roadside parking spaces;
- residential streets;
- council car parks;
- workplace car parks;
- supermarket car parks;
- railway stations;
- public parking areas; or
- other geographically accessible locations.

---

## 39. Street Post User Interface

A representative interface may display:

```text
+-----------------------------+
|       EV ENERGY POST        |
|                             |
|  Vehicle connected          |
|                             |
|  CHOOSE ENERGY SOURCE       |
|                             |
|  [ MY HOME ENERGY ]         |
|                             |
|  [ PUBLIC CHARGING ]        |
|                             |
|  [ MIXED ]                  |
|                             |
|  Available: 5.2 kWh         |
|                             |
|       [ START ]             |
+-----------------------------+
```

The physical form factor may resemble a parking meter.

---

## 40. System Architecture

A preferred system comprises:

```text
+--------------------------------------------+
|              ENERGY PLATFORM               |
|                                            |
| Authentication                             |
| Authorisation                              |
| Energy allocation                          |
| Transaction management                     |
| Meter reconciliation                       |
| Security                                   |
|                                            |
+---------------+----------------------------+
                |
       +--------+---------+
       |                  |
       v                  v
+---------------+   +-----------------+
| DOMESTIC      |   | REMOTE CHARGING |
| ENERGY SYSTEM |   | STATION         |
|               |   |                 |
| Battery       |   | Processor       |
| Solar         |   | Meter           |
| Smart meter   |   | Charger         |
| EMS           |   | Authentication  |
+---------------+   +--------+--------+
                              |
                              v
                             EV
```

---

## 41. Technical Advantages

The system may provide one or more of the following technical advantages:

1. geographically separates energy-resource ownership from charging location;
2. allows remote EV charging without a dedicated electrical connection from the domestic premises;
3. provides controlled access to domestic energy resources;
4. prevents unauthorised depletion of domestic energy storage;
5. allows energy allocations to be limited dynamically;
6. permits energy delivery to be reconciled with a domestic energy resource;
7. supports multiple energy suppliers;
8. supports multiple charging stations;
9. supports dynamic tariffs;
10. supports domestic energy reserves;
11. permits cryptographically controlled charging authorisations;
12. reduces the requirement for users without private driveways to install private EV charging infrastructure;
13. allows charging infrastructure to be integrated with parking infrastructure; and
14. provides an auditable relationship between a remote charging transaction and a domestic energy resource.

---

## 42. Further Embodiments

The invention may additionally incorporate:

- vehicle-to-grid operation;
- vehicle-to-home operation;
- vehicle-to-vehicle energy allocation;
- community batteries;
- energy cooperatives;
- renewable energy certificates;
- carbon accounting;
- dynamic grid constraints;
- demand-response signals;
- smart-meter data;
- electricity network capacity;
- battery degradation models;
- machine-learning energy forecasts;
- blockchain or distributed ledgers;
- conventional centralised databases;
- offline charging authorisations;
- roaming between charging networks;
- contactless authentication;
- fleet charging;
- employer-provided energy allocations; and
- commercial energy accounts.

The use of a distributed ledger is optional and is not required for implementation of the invention.

---

## 43. Alternative Accounting Model

The system may maintain a virtual energy balance.

For example:

```text
Domestic energy account

Starting balance       20.0 kWh
Remote charging         -4.5 kWh
Balance                 15.5 kWh
```

The underlying physical electricity may nevertheless have been delivered from the local electricity network.

The energy balance therefore represents an accounting or allocation relationship rather than necessarily a physical electron-tracking mechanism.

---

## 44. Alternative Settlement Model

Instead of transferring an exact number of kWh, the system may settle the transaction financially.

For example:

```text
Remote charging:             5 kWh
Domestic energy value:       £0.10/kWh
Remote charging cost:        £0.30/kWh

Energy component:             £0.50
Network component:             £0.75
Infrastructure component:      £0.50
```

The system may settle the difference between the domestic energy value and remote charging cost.

---

## 45. Computer-Implemented Method

According to another aspect of the invention, a computer-implemented method comprises:

1. receiving an authentication request from a remote EV charging station;
2. authenticating a user associated with a domestic energy resource;
3. obtaining energy availability information from the domestic energy resource;
4. determining an energy allocation based on the energy availability information;
5. generating a charging authorisation identifying the remote charging station and the energy allocation;
6. transmitting the charging authorisation to the remote charging station;
7. receiving a measurement of electrical energy delivered by the remote charging station;
8. reconciling the measured energy with the energy allocation; and
9. updating an energy account associated with the domestic energy resource.

---

## 46. Computer System

According to another aspect, the invention provides a computer system comprising one or more processors and memory containing instructions which, when executed, cause the system to:

- authenticate a user;
- identify a domestic energy resource;
- obtain energy availability information;
- calculate a permitted remote energy allocation;
- generate an authenticated remote charging authorisation;
- transmit the authorisation to a geographically remote charging station;
- receive charging-meter information; and
- reconcile the charging-meter information with the energy allocation.

---

## 47. Charging Station

According to another aspect, the invention provides a charging station comprising:

- an electric vehicle charging circuit;
- an electrical energy meter;
- a communication interface;
- an authentication interface;
- a processor; and
- a secure authorisation verification module,

wherein the processor is configured to obtain a remote charging authorisation associated with a domestic energy resource geographically separated from the charging station and to control electrical energy delivery to an electric vehicle according to parameters contained in the remote charging authorisation.

---

## 48. Authorisation Token

The remote charging authorisation may be represented by a digitally signed token containing at least:

```text
User identifier
Domestic energy resource identifier
Charging station identifier
Vehicle identifier
Energy quantity
Power limit
Validity period
Transaction identifier
Digital signature
```

The charging station may verify the token locally.

This permits the charging station to continue operation during temporary loss of communication with the central platform.

---

## 49. Offline Mode

In an offline embodiment, the energy platform may issue a pre-authorised energy token.

For example:

```text
ENERGY TOKEN

Maximum energy:       5 kWh
Maximum power:        7.2 kW
Valid until:          22:00
Charging network:     Network A
Vehicle:              Vehicle X
```

The charging station verifies the token locally and records the transaction for subsequent reconciliation.

---

## 50. Fleet Embodiment

A company may maintain an energy account associated with multiple vehicles.

```text
Company Energy Account
        |
        +-- Vehicle 1
        +-- Vehicle 2
        +-- Vehicle 3
        +-- Vehicle 4
```

The system can allocate energy to authorised vehicles at geographically remote charging stations.

---

## 51. Preferred Implementation

A preferred implementation comprises:

1. a domestic rechargeable battery;
2. a domestic energy-management controller;
3. a smart electricity meter;
4. a cloud-based energy-management platform;
5. a user authentication service;
6. a plurality of geographically distributed street charging posts;
7. each charging post having an electrical meter;
8. each charging post having a secure communication module;
9. an EV charging connector;
10. an authorisation engine;
11. an energy allocation engine; and
12. an energy reconciliation engine.

The system calculates an available remote energy allocation from the domestic energy resource, issues a temporary remote charging authorisation, controls charging at a geographically remote charging post and reconciles the measured energy delivered by the charging post against the user's energy allocation.

---

## 52. Scope of the Invention

The invention is not limited to the specific embodiments described.

The domestic energy resource may be physically located at a house, apartment, commercial building, workplace, community facility or other premises.

The remote charging station may be located anywhere geographically separated from the domestic energy resource.

The energy relationship may be represented using electrical energy, monetary value, energy credits, energy certificates, energy allocations or combinations thereof.

The communication between components may be wired or wireless.

The central energy-management platform may be implemented using one or more physical or virtual computing systems.

The foregoing embodiments are therefore illustrative rather than limiting.

---

# 53. Claims

## Claim 1 — System

**1. A system for controlling electric vehicle charging using energy associated with a geographically remote domestic energy resource, the system comprising:**

a domestic energy resource associated with a user;

a remote electric vehicle charging station geographically separated from the domestic energy resource;

an authentication system configured to authenticate the user;

a domestic energy interface configured to obtain energy availability information associated with the domestic energy resource;

an authorisation engine configured, following authentication of the user, to determine a permitted energy allocation based at least partly on the energy availability information and to generate a remote charging authorisation associated with the user and the remote electric vehicle charging station; and

a charging control system configured to permit electrical energy to be delivered from an electrical supply available at the remote electric vehicle charging station to an electric vehicle according to the remote charging authorisation.

## Claim 2

**2. The system of claim 1, wherein the domestic energy resource comprises a rechargeable battery.**

## Claim 3

**3. The system of claim 1 or claim 2, wherein the energy availability information comprises a state of charge of the domestic energy resource.**

## Claim 4

**4. The system of any preceding claim, wherein the authorisation engine determines the permitted energy allocation by subtracting a predetermined domestic energy reserve from energy available at the domestic energy resource.**

## Claim 5

**5. The system of any preceding claim, wherein the domestic energy reserve is dynamically determined according to predicted domestic electricity consumption.**

## Claim 6

**6. The system of any preceding claim, wherein the remote charging authorisation comprises a maximum electrical energy quantity and a maximum electrical power level.**

## Claim 7

**7. The system of any preceding claim, wherein the remote charging authorisation comprises a validity period and an identifier of the remote electric vehicle charging station.**

## Claim 8

**8. The system of any preceding claim, wherein the remote charging authorisation comprises a cryptographically signed authorisation token and the remote electric vehicle charging station comprises a verification module configured to verify the cryptographic signature before permitting charging.**

## Claim 9

**9. The system of any preceding claim, further comprising an electrical energy meter at the remote electric vehicle charging station configured to measure electrical energy delivered to the electric vehicle.**

## Claim 10

**10. The system of claim 9, further comprising an energy reconciliation system configured to compare the measured electrical energy delivered to the electric vehicle with the permitted energy allocation.**

## Claim 11

**11. The system of any preceding claim, wherein electrical energy delivered to the electric vehicle is obtained from an electrical network local to the remote electric vehicle charging station and is electronically associated with the domestic energy resource without requiring a dedicated electrical connection between the domestic energy resource and the remote electric vehicle charging station.**

## Claim 12

**12. The system of any preceding claim, wherein the remote electric vehicle charging station comprises a parking-management interface configured to associate a parking transaction with the remote charging authorisation.**

## Claim 13

**13. The system of any preceding claim, wherein the user can select between a public charging mode, a domestic energy allocation mode and a mixed charging mode.**

## Claim 14

**14. The system of any preceding claim, wherein the permitted energy allocation is determined using at least one of domestic battery state of charge, household electricity demand, predicted electricity demand, solar generation, electricity tariff, battery health, battery reserve and electrical network constraints.**

## Claim 15

**15. The system of any preceding claim, wherein the domestic energy resource comprises one or more of a domestic battery, photovoltaic generation system, smart meter, domestic energy-management system and energy account.**

## Claim 16

**16. A computer-implemented method for controlling geographically remote electric vehicle charging, the method comprising:**

authenticating a user associated with a domestic energy resource;

obtaining energy availability information associated with the domestic energy resource;

determining a permitted energy allocation;

generating a remote charging authorisation associated with the authenticated user and a geographically remote electric vehicle charging station;

transmitting the remote charging authorisation to the geographically remote electric vehicle charging station;

controlling delivery of electrical energy to an electric vehicle according to the remote charging authorisation;

receiving a measurement of electrical energy delivered to the electric vehicle; and

reconciling the measured electrical energy with the permitted energy allocation.

## Claim 17

**17. The method of claim 16, wherein determining the permitted energy allocation comprises maintaining a minimum domestic energy reserve at the domestic energy resource.**

## Claim 18

**18. The method of claim 16 or claim 17, wherein the electrical energy delivered to the electric vehicle is supplied by an electrical network local to the geographically remote electric vehicle charging station.**

## Claim 19

**19. A geographically remote electric vehicle charging station configured to receive a charging authorisation associated with a domestic energy resource geographically separated from the charging station, verify the charging authorisation, measure electrical energy delivered to an electric vehicle and transmit a charging transaction record to an energy-management platform.**

## Claim 20

**20. A computer-readable storage medium containing instructions which, when executed by one or more processors, cause the processors to authenticate a user associated with a domestic energy resource, determine a permitted remote energy allocation, generate a remote charging authorisation, transmit the remote charging authorisation to a geographically remote electric vehicle charging station and reconcile measured energy delivered by the charging station with the remote energy allocation.**

---

# 54. Abstract

A system and method are provided for controlling electric vehicle charging using energy associated with a domestic energy resource geographically separated from an electric vehicle charging station. A user associated with a domestic energy resource is authenticated by an energy-management platform. Energy availability information is obtained from the domestic energy resource and used to determine a permitted remote energy allocation. A temporary charging authorisation is generated for a geographically remote electric vehicle charging station. The charging station verifies the authorisation and delivers electrical energy to an electric vehicle, which may be supplied from an electrical network local to the charging station. Electrical energy delivered to the vehicle is measured and reconciled with the remote energy allocation. The domestic energy resource may comprise a rechargeable battery, photovoltaic system, smart meter or energy account. A domestic energy reserve may be maintained when determining the permitted allocation. The system thereby permits energy associated with a domestic energy resource to be used for electric vehicle charging at a geographically remote location without requiring a dedicated electrical connection between the domestic energy resource and the charging station.

**Suggested figure for the abstract: Figure 1.**

---

# 55. Proposed Patent Drawings

### Figure 1 — Overall system architecture

Show:

```text
Domestic Battery
       |
Smart Meter / EMS
       |
       v
Energy Platform
       |
       v
Remote Charging Post
       |
       v
Electric Vehicle
```

### Figure 2 — Street charging post

Show the physical post including:

- display;
- authentication reader;
- EV connector;
- meter;
- processor;
- communications module;
- emergency stop;
- parking interface.

### Figure 3 — Authentication sequence

```text
User
 |
 v
Charging Post
 |
 v
Authentication Service
 |
 v
Energy Supplier
 |
 v
Energy Platform
 |
 v
Charging Authorisation
 |
 v
Charging Post
```

### Figure 4 — Energy allocation calculation

```text
Battery State
     +
Household Demand
     +
Reserve
     +
Tariff
     +
Network Constraints
     |
     v
Permitted Energy Allocation
```

### Figure 5 — Charging transaction

```text
Request
  |
  v
Authentication
  |
  v
Energy Availability
  |
  v
Authorisation
  |
  v
Charging
  |
  v
Metering
  |
  v
Reconciliation
```

### Figure 6 — Physical versus accounting energy flow

This is particularly important.

Show two separate paths:

```text
PHYSICAL ELECTRICITY

Grid -----------------> Street Charger ---------> EV


ENERGY AUTHORISATION / ACCOUNTING

Home Battery ---------> Energy Platform --------> Street Charger
```

This drawing helps communicate the central technical concept.

### Figure 7 — Multiple charging locations

Show one domestic energy resource authorising multiple geographically distributed charging stations.

### Figure 8 — Mixed charging

Show a charging session in which a domestic allocation is consumed first and public electricity is subsequently used.

### Figure 9 — Domestic reserve protection

Show battery state of charge, reserve and permitted remote allocation.

### Figure 10 — Cryptographic charging token

Show generation, transmission and verification of a signed authorisation token.

---

# 56. Preferred Terminology for the Invention

For future development, the following terminology is recommended.

**Primary concept:**

> Geographically Remote Domestic Energy Authorisation

**System:**

> Remote Domestic Energy Charging System

**Energy token:**

> Remote Energy Charging Authorisation

**Virtual energy representation:**

> Energy Allocation

**Street hardware:**

> Remote Energy Charging Post

**Central platform:**

> Energy Authorisation and Reconciliation Platform

These terms are deliberately broader than a particular energy supplier or battery manufacturer.

---

# 57. Potentially Important Core Distinction

The invention should preferably not be limited to the proposition:

> "Use a home battery to charge an EV somewhere else."

The stronger technical concept is:

> **An authenticated energy-management system that associates a geographically remote EV charging transaction with an authorised domestic energy resource, determines a permitted energy allocation from that resource, issues a scoped charging authorisation to the remote charging station, and reconciles measured energy delivered at the remote station against the allocation.**

This distinction is important because the physical electricity can originate from the local network while the system maintains a controlled technical and accounting relationship with the user's domestic energy resource.

---

# 58. Filing Strategy

Before filing, the following should be treated as particularly important inventive features to investigate:

1. geographically separated domestic energy resource and EV charging point;
2. authenticated association between the two;
3. dynamic calculation of available remote energy;
4. preservation of a domestic energy reserve;
5. temporary charging authorisation;
6. cryptographic authorisation;
7. remote charging station verification;
8. measurement and reconciliation;
9. physical electricity being supplied locally while the energy allocation is associated with the remote domestic resource;
10. integration with parking infrastructure;
11. multi-supplier interoperability;
12. energy allocation usable at multiple geographically distributed charging points.

A patent attorney should then determine which combination provides the strongest independent claim.

---

# 59. Important Filing Note

This specification should be regarded as a **working invention disclosure / patent drafting document**, not as a final solicitor- or patent-attorney-reviewed application.

UK patent practice requires the description to disclose the invention sufficiently for it to be performed, and the claims should define the scope of protection sought.

Before public disclosure or commercial demonstration, the inventor should consider:

1. conducting a professional prior-art search;
2. identifying the actual inventive contribution;
3. checking ownership/inventorship;
4. preparing patent drawings;
5. having the claims reviewed by a UK patent attorney; and
6. filing an application before making a non-confidential public disclosure.

---

## Key Inventive Concept for Further Development

The strongest feature to investigate is the deliberate separation of **physical electricity flow** from the **authorised domestic energy allocation**.

The central concept is:

> **An authenticated energy-management system that associates a geographically remote EV charging transaction with an authorised domestic energy resource, determines a permitted energy allocation from that resource, issues a scoped charging authorisation to the remote charging station, and reconciles measured energy delivered at the remote station against the allocation.**

This should be the primary focus of subsequent prior-art research and claim development.
