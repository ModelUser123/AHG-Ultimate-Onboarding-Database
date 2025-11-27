# OBD-II Code Interpretation Guide

## Understanding OBD-II Diagnostic Trouble Codes

OBD-II (On-Board Diagnostics II) is the standardized system for vehicle self-diagnostics. This guide covers code structure, common codes, and interpretation strategies.

---

## Table of Contents

1. [Code Structure](#code-structure)
2. [Powertrain Codes (P-Codes)](#powertrain-codes-p-codes)
3. [Body Codes (B-Codes)](#body-codes-b-codes)
4. [Chassis Codes (C-Codes)](#chassis-codes-c-codes)
5. [Network Codes (U-Codes)](#network-codes-u-codes)
6. [Code Interpretation Strategy](#code-interpretation-strategy)
7. [Freeze Frame Data](#freeze-frame-data)
8. [Common Codes Quick Reference](#common-codes-quick-reference)

---

## Code Structure

### Code Format: PXXXX

```
P 0 1 2 3
│ │ │ │ │
│ │ │ │ └── Specific fault identification (0-9)
│ │ │ └──── Specific fault identification (0-9)
│ │ └────── Subsystem (0-9)
│ └──────── 0 = Generic (SAE), 1 = Manufacturer specific
└────────── P = Powertrain, B = Body, C = Chassis, U = Network
```

### Code Type Indicators

| First Character | System |
|-----------------|--------|
| P | Powertrain (engine, transmission) |
| B | Body (airbags, lighting, HVAC) |
| C | Chassis (ABS, traction control) |
| U | Network (communication between modules) |

| Second Character | Type |
|------------------|------|
| 0 | Generic (SAE standard) |
| 1 | Manufacturer specific |
| 2 | Generic or manufacturer specific |
| 3 | Generic or manufacturer specific |

---

## Powertrain Codes (P-Codes)

### P0xxx - Generic Powertrain Codes

#### P01xx - Fuel and Air Metering

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0100 | MAF Circuit Malfunction | Faulty MAF sensor, wiring, dirty sensor |
| P0101 | MAF Circuit Range/Performance | Vacuum leak, dirty MAF, intake leak |
| P0102 | MAF Circuit Low | MAF sensor, wiring, air leak before MAF |
| P0103 | MAF Circuit High | MAF sensor, wiring short |
| P0106 | MAP Circuit Range/Performance | MAP sensor, vacuum leak, wiring |
| P0107 | MAP Circuit Low | MAP sensor, wiring, vacuum line |
| P0108 | MAP Circuit High | MAP sensor, wiring short |
| P0110 | IAT Circuit Malfunction | IAT sensor, wiring |
| P0111 | IAT Circuit Range/Performance | IAT sensor location, wiring |
| P0112 | IAT Circuit Low | Shorted sensor, wiring issue |
| P0113 | IAT Circuit High | Open circuit, bad sensor |
| P0116 | ECT Circuit Range/Performance | Thermostat stuck, ECT sensor |
| P0117 | ECT Circuit Low | Shorted sensor, wiring |
| P0118 | ECT Circuit High | Open circuit, bad sensor |
| P0120 | TPS Circuit Malfunction | TPS sensor, wiring |
| P0121 | TPS Circuit Range/Performance | TPS sensor, throttle body carbon |
| P0122 | TPS Circuit Low | TPS sensor, wiring short to ground |
| P0123 | TPS Circuit High | TPS sensor, wiring short to voltage |
| P0125 | Insufficient Coolant Temp | Thermostat stuck open, ECT sensor |
| P0128 | Coolant Temp Below Thermostat Regulating Temp | Thermostat stuck open |
| P0130 | O2 Sensor Circuit (Bank 1 Sensor 1) | O2 sensor, wiring, exhaust leak |
| P0131 | O2 Sensor Low Voltage (B1S1) | O2 sensor, lean condition |
| P0132 | O2 Sensor High Voltage (B1S1) | O2 sensor, rich condition |
| P0133 | O2 Sensor Slow Response (B1S1) | Lazy O2 sensor, exhaust leak |
| P0134 | O2 Sensor No Activity (B1S1) | O2 sensor, heater circuit, wiring |
| P0135 | O2 Sensor Heater Circuit (B1S1) | Heater element, fuse, wiring |
| P0136-P0141 | O2 Sensor (Bank 1 Sensor 2) | Same causes as upstream sensor |
| P0150-P0161 | O2 Sensor (Bank 2) | Same causes as Bank 1 |
| P0170 | Fuel Trim (Bank 1) | Vacuum leak, MAF, fuel pressure |
| P0171 | System Too Lean (Bank 1) | Vacuum leak, weak fuel pump, MAF |
| P0172 | System Too Rich (Bank 1) | Leaking injector, fuel pressure, EVAP |
| P0173 | Fuel Trim (Bank 2) | Vacuum leak, MAF, fuel pressure |
| P0174 | System Too Lean (Bank 2) | Vacuum leak, intake leak Bank 2 |
| P0175 | System Too Rich (Bank 2) | Leaking injector, fuel pressure |

**Fuel Trim Interpretation**:
- STFT and LTFT should be within ±10%
- Positive numbers = adding fuel (lean condition detected)
- Negative numbers = removing fuel (rich condition detected)
- LTFT > +25% = significant lean issue
- Both banks lean = system issue (MAF, fuel pressure)
- One bank lean = that side has vacuum leak

---

#### P02xx - Fuel and Air Metering (Injector Circuit)

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0200 | Injector Circuit Malfunction | PCM, wiring, injector |
| P0201 | Injector Circuit Cyl 1 | Injector, wiring, PCM driver |
| P0202 | Injector Circuit Cyl 2 | Injector, wiring, PCM driver |
| P0203 | Injector Circuit Cyl 3 | Injector, wiring, PCM driver |
| P0204 | Injector Circuit Cyl 4 | Injector, wiring, PCM driver |
| P0205 | Injector Circuit Cyl 5 | Injector, wiring, PCM driver |
| P0206 | Injector Circuit Cyl 6 | Injector, wiring, PCM driver |
| P0207 | Injector Circuit Cyl 7 | Injector, wiring, PCM driver |
| P0208 | Injector Circuit Cyl 8 | Injector, wiring, PCM driver |
| P0218 | Transmission Over Temperature | Low fluid, cooling issue |
| P0219 | Engine Overspeed | Missed shift, PCM issue |
| P0220 | Throttle Position Sensor B | TPS sensor, wiring |
| P0230 | Fuel Pump Primary Circuit | Fuel pump relay, wiring, pump |
| P0261 | Cyl 1 Injector Circuit Low | Shorted injector, wiring |
| P0262 | Cyl 1 Injector Circuit High | Open injector, wiring |

---

#### P03xx - Ignition System or Misfire

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0300 | Random/Multiple Cylinder Misfire | Vacuum leak, fuel, spark, compression |
| P0301 | Cylinder 1 Misfire | Spark plug, coil, injector, compression |
| P0302 | Cylinder 2 Misfire | Spark plug, coil, injector, compression |
| P0303 | Cylinder 3 Misfire | Spark plug, coil, injector, compression |
| P0304 | Cylinder 4 Misfire | Spark plug, coil, injector, compression |
| P0305 | Cylinder 5 Misfire | Spark plug, coil, injector, compression |
| P0306 | Cylinder 6 Misfire | Spark plug, coil, injector, compression |
| P0307 | Cylinder 7 Misfire | Spark plug, coil, injector, compression |
| P0308 | Cylinder 8 Misfire | Spark plug, coil, injector, compression |
| P0316 | Engine Misfire at Startup | Fuel pressure, spark, injector |
| P0320 | Ignition/Distributor Signal | CKP sensor, wiring, timing |
| P0325 | Knock Sensor 1 Circuit | Knock sensor, wiring |
| P0327 | Knock Sensor 1 Low Input | Knock sensor, wiring |
| P0328 | Knock Sensor 1 High Input | Knock sensor, wiring, engine knock |
| P0330 | Knock Sensor 2 Circuit | Knock sensor, wiring |
| P0335 | Crankshaft Position Sensor A | CKP sensor, wiring, reluctor |
| P0336 | Crankshaft Position Sensor A Range/Performance | CKP sensor, reluctor damage |
| P0340 | Camshaft Position Sensor A | CMP sensor, wiring, timing |
| P0341 | Camshaft Position Sensor A Range/Performance | CMP sensor, timing chain |
| P0345 | Camshaft Position Sensor A Bank 2 | CMP sensor Bank 2 |
| P0351-P0358 | Ignition Coil Primary/Secondary | Coil, wiring, PCM driver |

**Misfire Diagnostic Strategy**:
1. Single cylinder misfire → Start with swap test (coil, injector)
2. Multiple specific cylinders → Look for pattern (same bank, same coil pack)
3. Random misfire (P0300) → System issue (vacuum, fuel pressure, base timing)

---

#### P04xx - Auxiliary Emission Controls

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0400 | EGR Flow Malfunction | EGR valve stuck, passages clogged |
| P0401 | EGR Insufficient Flow | Carbon buildup, EGR valve, DPFE sensor |
| P0402 | EGR Excessive Flow | EGR valve stuck open, vacuum leak |
| P0411 | Secondary Air Injection Incorrect Flow | Air pump, check valve, hoses |
| P0420 | Catalyst Efficiency Below Threshold (Bank 1) | Catalytic converter, O2 sensor |
| P0421 | Warm Up Catalyst Efficiency Below Threshold | Catalytic converter |
| P0430 | Catalyst Efficiency Below Threshold (Bank 2) | Catalytic converter |
| P0440 | EVAP System Malfunction | Gas cap, hoses, purge valve |
| P0441 | EVAP Incorrect Purge Flow | Purge valve, vacuum lines |
| P0442 | EVAP Small Leak | Gas cap, hoses, canister |
| P0443 | EVAP Purge Control Valve Circuit | Purge valve, wiring |
| P0446 | EVAP Vent System | Vent valve, wiring, canister |
| P0449 | EVAP Vent Valve/Solenoid | Vent valve, wiring |
| P0451 | EVAP Pressure Sensor Range/Performance | Tank pressure sensor |
| P0452 | EVAP Pressure Sensor Low | Tank pressure sensor |
| P0453 | EVAP Pressure Sensor High | Tank pressure sensor |
| P0455 | EVAP Large Leak | Gas cap, hose disconnected, leak |
| P0456 | EVAP Very Small Leak | Minor leak, gas cap seal |

**P0420/P0430 Interpretation**:
- Indicates downstream O2 sensor is seeing too much switching
- Healthy cat: downstream O2 should be nearly flat line
- First verify front O2 sensor is functioning correctly
- Check for exhaust leaks before cat
- May need to monitor O2 sensor waveforms

---

#### P05xx - Vehicle Speed and Idle Control

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0500 | Vehicle Speed Sensor | VSS, wiring, output shaft sensor |
| P0501 | Vehicle Speed Sensor Range/Performance | VSS, wiring |
| P0505 | Idle Air Control System | IAC valve, carbon buildup |
| P0506 | Idle Control System RPM Lower Than Expected | Vacuum leak, IAC, throttle body |
| P0507 | Idle Control System RPM Higher Than Expected | IAC, vacuum leak, throttle body |
| P0520 | Engine Oil Pressure Sensor | Oil pressure sensor, wiring |
| P0562 | System Voltage Low | Battery, alternator, connections |
| P0563 | System Voltage High | Alternator overcharging |

---

#### P06xx - Computer and Output Circuit

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0600 | Serial Communication Link | PCM internal, wiring |
| P0601 | Internal Control Module Memory Check Sum | PCM failure |
| P0602 | Control Module Programming | PCM needs reprogrammed |
| P0603 | Internal Control Module KAM | Battery disconnected, PCM |
| P0606 | PCM Processor | PCM internal failure |
| P0607 | Control Module Performance | PCM failure |

---

#### P07xx - Transmission

| Code | Description | Common Causes |
|------|-------------|---------------|
| P0700 | Transmission Control System | Check for additional trans codes |
| P0705 | Trans Range Sensor Circuit | PRNDL switch, wiring |
| P0706 | Trans Range Sensor Performance | PRNDL switch, adjustment |
| P0715 | Input/Turbine Speed Sensor | Input speed sensor, wiring |
| P0720 | Output Speed Sensor | Output speed sensor, wiring |
| P0730 | Incorrect Gear Ratio | Internal trans issue, low fluid |
| P0731 | Gear 1 Incorrect Ratio | Internal trans issue |
| P0732 | Gear 2 Incorrect Ratio | Internal trans issue |
| P0733 | Gear 3 Incorrect Ratio | Internal trans issue |
| P0734 | Gear 4 Incorrect Ratio | Internal trans issue |
| P0740 | Torque Converter Clutch Circuit | TCC solenoid, wiring |
| P0741 | Torque Converter Clutch Performance | TCC solenoid, converter |
| P0750 | Shift Solenoid A | Shift solenoid, wiring |
| P0751 | Shift Solenoid A Performance | Shift solenoid, internal trans |
| P0755 | Shift Solenoid B | Shift solenoid, wiring |
| P0756 | Shift Solenoid B Performance | Shift solenoid, internal trans |
| P0760 | Shift Solenoid C | Shift solenoid, wiring |
| P0765 | Shift Solenoid D | Shift solenoid, wiring |
| P0770 | Shift Solenoid E | Shift solenoid, wiring |

---

## Body Codes (B-Codes)

### Common B-Codes

| Code | Description | Common Causes |
|------|-------------|---------------|
| B0001 | Driver Frontal Stage 1 Deployment | Airbag module, wiring, sensor |
| B0002 | Driver Frontal Stage 2 Deployment | Airbag module |
| B0051 | Passenger Frontal Stage 1 Deployment | Airbag module |
| B1000 | ECU Malfunction | Airbag module internal |
| B1200 | Climate Control Head | HVAC control module |
| B1318 | Battery Voltage Low | Battery, alternator |
| B1342 | ECU Damaged | Module replacement needed |
| B1480 | Brake Pedal Input Circuit | Brake switch, wiring |
| B2958 | Security System | Transponder, PATS antenna |

---

## Chassis Codes (C-Codes)

### Common C-Codes

| Code | Description | Common Causes |
|------|-------------|---------------|
| C0035 | Left Front Wheel Speed Sensor | Wheel speed sensor, wiring, tone ring |
| C0040 | Right Front Wheel Speed Sensor | Wheel speed sensor |
| C0041 | Right Front Wheel Speed Sensor Range | Wheel speed sensor, hub |
| C0045 | Left Rear Wheel Speed Sensor | Wheel speed sensor |
| C0050 | Right Rear Wheel Speed Sensor | Wheel speed sensor |
| C0265 | EBCM Relay | ABS relay, wiring |
| C0550 | ECU Malfunction | ABS module |
| C0710 | Steering Position Sensor | Clock spring, sensor, wiring |
| C1095 | ABS Hydraulic Pump Motor | ABS pump, wiring |
| C1145 | Wheel Speed Sensor RF Input Circuit | RF wheel speed sensor |
| C1155 | Wheel Speed Sensor LF Input Circuit | LF wheel speed sensor |
| C1175 | Wheel Speed Sensor LR Input Circuit | LR wheel speed sensor |
| C1185 | Wheel Speed Sensor RR Input Circuit | RR wheel speed sensor |

---

## Network Codes (U-Codes)

### Common U-Codes

| Code | Description | Common Causes |
|------|-------------|---------------|
| U0001 | High Speed CAN Communication | CAN bus wiring, modules |
| U0100 | Lost Communication with ECM/PCM | PCM, CAN bus wiring |
| U0101 | Lost Communication with TCM | TCM, CAN bus wiring |
| U0121 | Lost Communication with ABS | ABS module, wiring |
| U0140 | Lost Communication with BCM | BCM, wiring |
| U0155 | Lost Communication with IPC | Instrument cluster, wiring |
| U0168 | Lost Communication with VCIM | Vehicle communication module |
| U0401 | Invalid Data from ECM | PCM data error |
| U1000 | Class 2 Communication Malfunction | Network communication error |
| U1096 | Lost Communication with Shifter Module | Shifter module, wiring |

**U-Code Diagnostic Tips**:
- Often caused by single module failure
- Can also be CAN bus wiring issue
- Check for TSBs - may require software update
- Module not powering up will cause "lost communication"

---

## Code Interpretation Strategy

### Step 1: Retrieve All Codes

- Pull codes from ALL modules, not just PCM
- Note pending codes and history codes
- Check for multiple codes - they may be related

### Step 2: Prioritize Codes

**Priority Order**:
1. Codes that disable systems (transmission, ABS)
2. Codes causing driveability symptoms
3. Emissions-related codes
4. Communication codes (may be root cause)
5. Informational codes

### Step 3: Research Codes

- Check manufacturer TSBs
- Look for pattern failures
- Note if code is generic (P0xxx) or manufacturer specific (P1xxx)

### Step 4: Analyze Freeze Frame Data

- Provides snapshot when code set
- Look at:
  - Engine RPM
  - Vehicle speed
  - Engine load
  - Coolant temperature
  - Fuel trims
  - Run time

### Step 5: Perform Pinpoint Tests

- Follow manufacturer diagnostic procedure
- Don't replace parts based on code alone
- Verify repair by clearing codes and road testing

---

## Freeze Frame Data

### Key Parameters to Review

| Parameter | What It Tells You |
|-----------|------------------|
| Engine RPM | Engine speed when code set (idle, cruise, accel) |
| Vehicle Speed | Stopped, city driving, highway |
| Engine Load | Light load, heavy load, WOT |
| Coolant Temp | Cold start issue vs. hot issue |
| STFT/LTFT | Fuel delivery problem direction |
| MAP/MAF | Load calculation accuracy |
| Spark Advance | Knock or timing issue |
| Runtime | How long engine was running |

### Interpreting Freeze Frame

**Example 1: P0171 Lean Code**
```
RPM: 750 (idle)
Speed: 0 MPH
Load: 22%
ECT: 195°F
STFT: +18%
LTFT: +22%
```
**Interpretation**: Lean at idle when warm = vacuum leak likely

**Example 2: P0300 Random Misfire**
```
RPM: 2500
Speed: 55 MPH
Load: 65%
ECT: 210°F
STFT: -5%
LTFT: +8%
```
**Interpretation**: Misfire under load when warm = ignition or compression issue

---

## Common Codes Quick Reference

### Top 25 Most Common Codes

| Rank | Code | Description | Quick Check |
|------|------|-------------|-------------|
| 1 | P0420 | Catalyst Efficiency | Check O2 sensors first |
| 2 | P0171 | System Too Lean | Smoke test for vacuum leaks |
| 3 | P0300 | Random Misfire | Check plugs, coils, compression |
| 4 | P0440 | EVAP System | Start with gas cap |
| 5 | P0442 | EVAP Small Leak | Smoke test EVAP system |
| 6 | P0135 | O2 Heater B1S1 | Check fuse and heater circuit |
| 7 | P0455 | EVAP Large Leak | Check gas cap and hoses |
| 8 | P0401 | EGR Insufficient Flow | Clean EGR passages |
| 9 | P0128 | Coolant Temp Below Thermostat | Replace thermostat |
| 10 | P0301-P0308 | Specific Misfire | Swap test coil/injector |
| 11 | P0172 | System Too Rich | Check fuel pressure, EVAP purge |
| 12 | P0505 | Idle Air Control | Clean IAC and throttle body |
| 13 | P0174 | System Too Lean B2 | Check intake manifold gasket |
| 14 | P0340 | Camshaft Position Sensor | Check sensor and timing |
| 15 | P0335 | Crankshaft Position Sensor | Check sensor and reluctor |
| 16 | P0141 | O2 Heater B1S2 | Check fuse and heater circuit |
| 17 | P0446 | EVAP Vent System | Check vent valve |
| 18 | P0430 | Catalyst Efficiency B2 | Check O2 sensors first |
| 19 | P0507 | Idle RPM High | Check for vacuum leak |
| 20 | P0113 | IAT Circuit High | Check sensor and wiring |
| 21 | P0133 | O2 Slow Response | Replace O2 sensor |
| 22 | P0500 | Vehicle Speed Sensor | Check VSS and wiring |
| 23 | P0325 | Knock Sensor Circuit | Check sensor and wiring |
| 24 | P0700 | Transmission Control | Check for additional trans codes |
| 25 | P0741 | TCC Performance | Check TCC solenoid |

---

## Manufacturer Specific Codes

### Note on P1xxx Codes

P1xxx codes are manufacturer specific. Always reference:
- Factory service manual
- Manufacturer TSBs
- Aftermarket scan tool code definitions specific to make

### Common Resources for Manufacturer Codes

- ALLDATA
- Mitchell On-Demand
- Factory service information subscriptions
- Manufacturer technical hotlines

---

## Related Resources

- [Diagnostics by Symptom](../diagnostics/README.md)
- [Decision Trees](../decision-trees/README.md)
- [Electrical Troubleshooting](../electrical/README.md)
- [Engine Repair](../engine-repair/README.md)
- [Transmission](../transmission/README.md)

---

*Last Updated: 2024*
*AHG Auto Repair Knowledge Base*
