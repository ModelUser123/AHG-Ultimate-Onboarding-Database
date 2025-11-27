# Decision Trees

## Diagnostic Flowcharts and Repair Decision Guides

This guide provides visual decision trees and flowcharts for common diagnostic scenarios.

---

## Table of Contents

1. [No Start Conditions](#no-start-conditions)
2. [Engine Performance Issues](#engine-performance-issues)
3. [Brake Diagnosis](#brake-diagnosis)
4. [Electrical Issues](#electrical-issues)
5. [HVAC Diagnosis](#hvac-diagnosis)
6. [Noise Diagnosis](#noise-diagnosis)
7. [Repair vs. Replace Decisions](#repair-vs-replace-decisions)
8. [Customer Concern Prioritization](#customer-concern-prioritization)

---

## No Start Conditions

### No Crank Decision Tree

```
Vehicle Does Not Crank
│
├── Battery voltage 12.4V+?
│   │
│   ├── NO → Charge/test/replace battery
│   │        └── Retest
│   │
│   └── YES → Check voltage at starter S terminal (key to start)
│             │
│             ├── Has voltage at S terminal?
│             │   │
│             │   ├── NO → Check neutral safety switch
│             │   │        ├── Shift to neutral, try start
│             │   │        │   ├── Starts → Adjust/replace NS switch
│             │   │        │   └── No start → Check ignition switch
│             │   │        │                  └── Check relay/fuse
│             │   │
│             │   └── YES → Check ground to starter
│             │             │
│             │             ├── Bad ground → Repair ground
│             │             │
│             │             └── Good ground → Check starter draw
│             │                               │
│             │                               ├── High draw → Mechanical issue
│             │                               │              or bad starter
│             │                               └── Low/no draw → Replace starter
```

### Cranks But No Start Decision Tree

```
Engine Cranks But Does Not Start
│
├── Check for spark
│   │
│   ├── NO SPARK → Check crank sensor signal
│   │              │
│   │              ├── No signal → Replace crank sensor
│   │              │               └── Check wiring
│   │              │
│   │              └── Has signal → Check cam sensor
│   │                               └── Check coils/ignition module
│   │
│   └── HAS SPARK → Check fuel pressure
│                    │
│                    ├── NO PRESSURE → Check fuel pump relay
│                    │                 └── Check fuel pump fuse
│                    │                 └── Check pump power/ground
│                    │                 └── Replace fuel pump
│                    │
│                    ├── LOW PRESSURE → Check for restriction
│                    │                  └── Check regulator
│                    │                  └── Weak pump
│                    │
│                    └── NORMAL PRESSURE → Check for injector pulse
│                                          │
│                                          ├── NO PULSE → Check PCM signals
│                                          │              └── Check wiring
│                                          │
│                                          └── HAS PULSE → Check compression
│                                                          └── Check timing
```

---

## Engine Performance Issues

### Check Engine Light Diagnosis

```
Check Engine Light On
│
├── Scan for codes
│   │
│   ├── No codes stored
│   │   └── Intermittent issue
│   │       └── Check freeze frame data
│   │       └── Monitor live data
│   │
│   └── Codes present
│       │
│       ├── Single code → Research code
│       │                 └── Check for TSBs
│       │                 └── Perform pinpoint test
│       │                 └── Repair and verify
│       │
│       └── Multiple codes → Look for pattern
│                            │
│                            ├── Related codes → Find root cause
│                            │   (e.g., multiple misfire + lean)
│                            │
│                            └── Unrelated codes → Address by priority
│                                                  └── Safety first
│                                                  └── Drivability second
```

### Engine Misfire Diagnosis

```
Engine Misfire Detected (P0300-P0308)
│
├── Single cylinder misfire (P0301-P0308)
│   │
│   ├── Swap ignition coil with known good cylinder
│   │   │
│   │   ├── Misfire moves → Replace coil
│   │   │
│   │   └── Misfire stays → Swap injector
│   │                        │
│   │                        ├── Misfire moves → Replace injector
│   │                        │
│   │                        └── Misfire stays → Compression test
│   │                                            │
│   │                                            ├── Low compression
│   │                                            │   └── Leak-down test
│   │                                            │   └── Valve or ring issue
│   │                                            │
│   │                                            └── Good compression
│   │                                                └── Check plug condition
│   │                                                └── Check wire (if applicable)
│   │
│   └── Random misfire (P0300)
│       │
│       ├── Check fuel pressure → Low = fuel delivery issue
│       ├── Check vacuum leaks → Smoke test
│       ├── Check fuel trims → High positive = lean condition
│       ├── Check base timing
│       └── Check for multiple component failures
```

### Overheating Diagnosis

```
Engine Overheating
│
├── Check coolant level
│   │
│   ├── LOW → Check for leaks
│   │         │
│   │         ├── External leak visible → Repair leak
│   │         │
│   │         └── No external leak → Check for internal leak
│   │                                 └── Combustion leak test
│   │                                 └── Head gasket check
│   │
│   └── FULL → Check thermostat operation
│              │
│              ├── Not opening → Replace thermostat
│              │
│              └── Opening → Check cooling fan
│                            │
│                            ├── Not running → Check relay, fuse, sensor
│                            │
│                            └── Running → Check radiator flow
│                                          │
│                                          ├── Restricted → Flush or replace
│                                          │
│                                          └── Good flow → Check water pump
│                                                          └── Impeller damage
│                                                          └── Belt slipping
```

---

## Brake Diagnosis

### Brake Noise Diagnosis

```
Customer Reports Brake Noise
│
├── When does noise occur?
│   │
│   ├── Only when braking
│   │   │
│   │   ├── Grinding sound → Check pad thickness
│   │   │                    └── Metal on metal = Replace pads + rotors
│   │   │
│   │   ├── Squealing sound → Check for:
│   │   │                     └── Wear indicators hitting
│   │   │                     └── Glazed pads/rotors
│   │   │                     └── Missing shims
│   │   │                     └── Debris
│   │   │
│   │   └── Thumping/pulsation → Measure rotor runout
│   │                            └── Check thickness variation
│   │                            └── Machine or replace rotors
│   │
│   └── All the time (not related to braking)
│       └── Check wheel bearing
│       └── Check for debris in brakes
│       └── Check backing plate contact
```

### Brake Pull Diagnosis

```
Vehicle Pulls When Braking
│
├── Check caliper slide pins
│   │
│   ├── Seized or sticking → Clean and lubricate
│   │
│   └── OK → Compare brake temperatures after test drive
│            │
│            ├── One side significantly hotter
│            │   └── Check brake hose for restriction
│            │   └── Check caliper piston
│            │
│            └── Temps relatively equal
│                └── Check pad contamination
│                └── Check alignment
│                └── Check suspension components
```

---

## Electrical Issues

### Battery Drain Diagnosis

```
Battery Goes Dead Overnight
│
├── Load test battery
│   │
│   ├── Battery fails → Replace battery
│   │
│   └── Battery good → Test alternator
│                      │
│                      ├── Not charging → Repair/replace alternator
│                      │
│                      └── Charging OK → Parasitic draw test
│                                        │
│                                        ├── Draw under 50mA → Normal
│                                        │   └── Check usage patterns
│                                        │   └── Check battery age
│                                        │
│                                        └── Draw over 50mA → Find source
│                                            └── Pull fuses one at a time
│                                            └── Identify problem circuit
│                                            └── Trace to component
```

### Electrical Accessory Not Working

```
Electrical Component Not Working
│
├── Check fuse
│   │
│   ├── Blown → Replace fuse
│   │           │
│   │           ├── Blows again → Short circuit
│   │           │                 └── Trace wiring
│   │           │
│   │           └── Holds → Original may have been weak
│   │                       └── Monitor
│   │
│   └── Good → Check for power at component
│              │
│              ├── No power → Trace wiring from fuse
│              │              └── Check connectors
│              │              └── Check switches
│              │
│              └── Has power → Check ground
│                              │
│                              ├── No ground → Repair ground
│                              │
│                              └── Good ground → Component failed
```

---

## HVAC Diagnosis

### AC Not Cooling

```
AC Blowing Warm Air
│
├── Check if compressor clutch engaging
│   │
│   ├── NOT ENGAGING
│   │   │
│   │   ├── Check refrigerant level (low pressure switch)
│   │   │   └── Low → Leak test, repair, recharge
│   │   │
│   │   ├── Check clutch fuse/relay
│   │   │   └── Faulty → Replace
│   │   │
│   │   ├── Check clutch coil
│   │   │   └── No power → Trace wiring
│   │   │   └── Has power → Replace clutch/compressor
│   │   │
│   │   └── Check clutch gap
│   │       └── Excessive → Adjust or replace
│   │
│   └── ENGAGING
│       │
│       └── Check system pressures
│           │
│           ├── Both low → Low charge, leak
│           ├── Both high → Overcharge, condenser issue
│           ├── Low side high, high side low → Compressor weak
│           └── Normal pressures → Check blend door operation
```

### Heater Not Working

```
No Heat from Heater
│
├── Check coolant level
│   │
│   ├── Low → Fill and check for leaks
│   │         └── Check for head gasket issue
│   │
│   └── Full → Feel heater hoses
│              │
│              ├── Both hot → Blend door issue
│              │              └── Check actuator
│              │              └── Check door linkage
│              │
│              ├── One hot, one cool → Heater core restricted
│              │                       └── Flush core
│              │                       └── Replace if no improvement
│              │
│              └── Both cool → Thermostat stuck open
│                              └── Replace thermostat
```

---

## Noise Diagnosis

### Engine Noise Identification

```
Engine Noise Complaint
│
├── When does noise occur?
│   │
│   ├── Cold start only → Piston slap or lifter tick
│   │                     └── If goes away when warm → Usually acceptable
│   │                     └── If persistent → Further diagnosis
│   │
│   ├── At idle only → Exhaust leak
│   │                  └── Accessory bearing
│   │                  └── Timing chain slack
│   │
│   ├── Under acceleration → Rod knock
│   │                        └── Piston slap
│   │                        └── Exhaust leak
│   │
│   └── All operating conditions → Locate with stethoscope
│                                  └── Top end = valve train
│                                  └── Bottom end = rod/main bearing
│                                  └── Front = accessories
```

---

## Repair vs. Replace Decisions

### Engine Repair vs. Replace

```
Major Engine Problem Identified
│
├── What is the issue?
│   │
│   ├── Single component failure → Usually repair
│   │
│   └── Multiple issues → Consider replacement
│
├── Vehicle value vs. repair cost
│   │
│   ├── Repair cost > 50% vehicle value → Consider replacement
│   │
│   └── Repair cost < 50% vehicle value → Usually repair
│
├── Vehicle age and mileage
│   │
│   ├── Low mileage, good condition → Repair
│   │
│   └── High mileage, multiple issues → Replace engine or vehicle
│
└── Engine replacement options
    │
    ├── Used engine → $1,000-$3,000 + labor
    ├── Remanufactured → $3,000-$5,000 + labor
    └── New (if available) → Highest cost
```

### Transmission Repair vs. Replace

```
Transmission Problems
│
├── Is it internal or external?
│   │
│   ├── External (sensor, solenoid) → Usually repair
│   │
│   └── Internal (clutch packs, hard parts) → Consider rebuild/replace
│
├── Severity of symptoms
│   │
│   ├── Occasional slip or hard shift → Diagnose further
│   │   └── May be fluid or solenoid
│   │
│   ├── Multiple gears affected → Internal damage likely
│   │   └── Rebuild or replace
│   │
│   └── Complete failure → Replace
│
└── Options
    │
    ├── Rebuild in-house → $2,000-$4,000
    ├── Remanufactured → $2,500-$4,500 + labor
    └── Used → $800-$2,000 + labor
```

---

## Customer Concern Prioritization

### Priority Classification

```
Customer Concern Assessment
│
├── PRIORITY 1 - SAFETY
│   │
│   ├── Brakes near failure
│   ├── Steering/suspension unsafe
│   ├── Lighting failures
│   ├── Tire hazards
│   └── Action: Recommend immediate repair
│
├── PRIORITY 2 - RELIABILITY
│   │
│   ├── Components near failure
│   ├── Warning lights on
│   ├── Overdue maintenance
│   └── Action: Schedule soon
│
├── PRIORITY 3 - PREVENTIVE
│   │
│   ├── Maintenance coming due
│   ├── Minor wear observed
│   └── Action: Plan for future
│
└── PRIORITY 4 - COMFORT/CONVENIENCE
    │
    ├── Non-essential accessories
    ├── Cosmetic issues
    └── Action: Customer discretion
```

---

## Diagnostic Time Guidelines

### Expected Diagnostic Times

| Complexity | Expected Time | Examples |
|------------|---------------|----------|
| Simple | 0.3-0.5 hrs | Check engine light, single code |
| Moderate | 0.5-1.0 hrs | Multiple symptoms, need testing |
| Complex | 1.0-2.0 hrs | Intermittent issues, electrical |
| Difficult | 2.0+ hrs | Multiple systems, no codes |

---

## Related Resources

- [Diagnostics by Symptom](../diagnostics/README.md)
- [OBD-II Code Interpretation](../obd2-codes/README.md)
- [Electrical Troubleshooting](../electrical/README.md)
- [Brake Systems](../brake-systems/README.md)

---

*Last Updated: 2024*
*AHG Auto Repair Knowledge Base*
