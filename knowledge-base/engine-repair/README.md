# Engine Repair

## Complete Engine Service and Repair Guide

This guide covers engine diagnostics, maintenance, and repair procedures for gasoline engines.

---

## Table of Contents

1. [Engine Fundamentals](#engine-fundamentals)
2. [Engine Diagnostics](#engine-diagnostics)
3. [Ignition System Service](#ignition-system-service)
4. [Fuel System Service](#fuel-system-service)
5. [Cooling System Service](#cooling-system-service)
6. [Lubrication System](#lubrication-system)
7. [Timing Belt/Chain Service](#timing-beltchain-service)
8. [Valve Train Service](#valve-train-service)
9. [Engine Mechanical Repairs](#engine-mechanical-repairs)
10. [Common Engine Repairs](#common-engine-repairs)

---

## Engine Fundamentals

### Engine Types

**Configuration**:
- Inline (I4, I6)
- V-Type (V6, V8)
- Flat/Boxer (H4, H6)

**Valve Train**:
- OHV (Overhead Valve) - pushrods
- SOHC (Single Overhead Cam)
- DOHC (Dual Overhead Cam)

**Fuel Delivery**:
- Port Fuel Injection (PFI)
- Direct Injection (GDI)
- Throttle Body Injection (TBI) - older vehicles

### Four-Stroke Cycle

1. **Intake**: Piston moves down, intake valve open, air/fuel enters
2. **Compression**: Piston moves up, valves closed, mixture compressed
3. **Power**: Spark ignites mixture, piston pushed down
4. **Exhaust**: Piston moves up, exhaust valve open, gases expelled

### Engine Specifications

**Key Measurements**:
- Bore: Cylinder diameter
- Stroke: Piston travel distance
- Displacement: Total swept volume
- Compression ratio: Cylinder volume comparison (compressed vs. uncompressed)

**Typical Specifications**:
| Measurement | Typical Range |
|-------------|---------------|
| Compression pressure | 125-175 PSI |
| Compression variation | Max 10% between cylinders |
| Oil pressure (idle) | 10-20 PSI minimum |
| Oil pressure (2000 RPM) | 25-65 PSI |
| Coolant temp (thermostat) | 180-195°F |

---

## Engine Diagnostics

### Compression Test

**Purpose**: Verify cylinder sealing

**Procedure**:
1. Engine at operating temperature
2. Disable ignition and fuel
3. Remove all spark plugs
4. Install compression gauge in cylinder 1
5. Crank engine (WOT) for 4-6 compression strokes
6. Record reading
7. Repeat for all cylinders

**Interpreting Results**:
| Condition | Indication |
|-----------|------------|
| All cylinders within 10% | Normal |
| One cylinder 20%+ low | Ring/valve issue that cylinder |
| Two adjacent cylinders low | Head gasket between them |
| All cylinders low | Timing issue or worn engine |

**Wet Test**:
- Add tablespoon of oil to low cylinder
- Retest
- If compression improves: Ring problem
- If compression same: Valve problem

### Leak-Down Test

**Purpose**: Identify WHERE cylinder is leaking

**Procedure**:
1. Remove all spark plugs
2. Bring cylinder 1 to TDC compression stroke
3. Connect leak-down tester
4. Apply air pressure
5. Listen for escaping air
6. Repeat for all cylinders

**Leak Locations**:
| Location of Air | Indicates |
|-----------------|-----------|
| Intake | Intake valve not sealing |
| Exhaust | Exhaust valve not sealing |
| Oil fill cap | Rings not sealing |
| Radiator | Head gasket to coolant |
| Adjacent cylinder | Head gasket between cylinders |

**Acceptable Leak-Down**: 5-10% (up to 20% on high-mileage engine)

### Cylinder Power Balance Test

**Purpose**: Identify weak cylinder

**Procedure**:
1. With engine running, disable one cylinder at a time
2. Note RPM drop for each cylinder
3. All should drop approximately same amount

**Interpretation**:
- Equal RPM drop = All cylinders contributing equally
- Minimal RPM drop = That cylinder is weak

### Oil Pressure Test

**Procedure**:
1. Connect mechanical gauge to oil pressure port
2. Start engine
3. Record pressure at idle
4. Record pressure at 2000-2500 RPM

**Specifications** (typical):
- Idle: 10-20 PSI minimum
- 2000 RPM: 25-65 PSI

**Low Pressure Causes**:
- Low oil level
- Wrong viscosity oil
- Worn oil pump
- Worn bearings
- Clogged pickup screen

---

## Ignition System Service

### Spark Plug Service

**Inspection Points**:
| Condition | Indicates |
|-----------|-----------|
| Normal (light brown/gray) | Correct A/F ratio |
| Black/sooty (carbon) | Rich mixture or weak spark |
| White/blistered | Lean mixture or overheating |
| Oil fouled | Worn rings or valve seals |
| Deposits | Coolant leak (head gasket) |
| Worn electrode | Normal wear, replace |

**Gap Specifications**:
- Typically 0.028" - 0.060"
- ALWAYS verify with manufacturer spec
- Do NOT gap iridium/platinum plugs - pre-gapped

**Installation**:
1. Apply anti-seize to threads (optional, check manufacturer)
2. Hand start plug
3. Torque to spec (typically 12-18 ft-lbs for aluminum heads)

### Ignition Coil Service

**Testing Coil-on-Plug (COP)**:
1. Swap suspect coil with known good cylinder
2. If misfire moves, coil is faulty
3. If misfire stays, problem is elsewhere

**Coil Resistance Test** (if no swap test possible):
| Measurement | Typical Spec |
|-------------|--------------|
| Primary resistance | 0.5-2.0 ohms |
| Secondary resistance | 5,000-15,000 ohms |

### Distributor Ignition (Older Vehicles)

**Components**:
- Distributor cap
- Rotor
- Ignition module
- Pickup coil
- Ignition coil

**Service Points**:
- Inspect cap for carbon tracks, cracks
- Check rotor for wear
- Verify pickup coil air gap
- Check timing with timing light

---

## Fuel System Service

### Fuel Pressure Testing

**Procedure**:
1. Connect fuel pressure gauge to test port
2. Key on, engine off - note pressure
3. Start engine - note pressure
4. Snap throttle - pressure should increase

**Typical Pressures** (PFI systems):
| Condition | Pressure |
|-----------|----------|
| Key on, engine off | 50-60 PSI |
| Idle | 40-50 PSI |
| Full throttle | 50-60 PSI |
| Residual (after 10 min) | 35+ PSI |

**Pressure Drop Indicates**:
- Leaking injector
- Faulty fuel pressure regulator
- Check valve issue in pump

### Fuel Injector Service

**Testing**:
1. Listen with stethoscope for clicking
2. Check resistance (typically 12-16 ohms)
3. Check spray pattern (if accessible)
4. Measure injector pulse with noid light

**Cleaning**:
- Fuel injector cleaning service recommended every 30,000-50,000 miles
- Use quality fuel system cleaner
- Professional cleaning for heavily clogged injectors

### Throttle Body Service

**Cleaning Procedure**:
1. Remove intake tube
2. Spray throttle body cleaner on plate and bore
3. Wipe with clean rag (DO NOT use scraper)
4. Clean IAC passage if accessible
5. Reinstall intake tube
6. May need throttle position relearn procedure

### MAF Sensor Service

**Cleaning**:
1. Locate MAF sensor
2. Remove carefully
3. Spray MAF sensor cleaner on elements
4. Allow to dry completely
5. Reinstall

**CAUTION**: Never touch MAF elements with fingers or tools

---

## Cooling System Service

### Cooling System Components

- Radiator
- Water pump
- Thermostat
- Hoses (upper, lower, heater)
- Coolant reservoir
- Cooling fans (mechanical or electric)
- Temperature sensor/sending unit

### Cooling System Pressure Test

**Procedure**:
1. Attach pressure tester to radiator
2. Pump to system spec (typically 15-16 PSI)
3. Observe gauge for 15 minutes
4. Pressure drop indicates leak
5. Inspect system for external leaks

### Thermostat Replacement

**Symptoms of Faulty Thermostat**:
- Engine overheating (stuck closed)
- Engine runs cold/heater not working (stuck open)
- Erratic temperature gauge

**Replacement Procedure**:
1. Drain coolant below thermostat level
2. Remove thermostat housing
3. Note thermostat orientation
4. Clean mating surfaces
5. Install new thermostat (spring toward engine)
6. Install new gasket/O-ring
7. Refill and bleed cooling system

### Water Pump Replacement

**Failure Indicators**:
- Coolant leak at weep hole
- Noise (bearing failure)
- Wobble in pump shaft
- Overheating

**General Procedure**:
1. Drain cooling system
2. Remove drive belt
3. Remove pump mounting bolts
4. Remove pump
5. Clean mounting surface
6. Install new pump with new gasket
7. Reinstall belt
8. Refill and bleed system

### Coolant Flush

**Procedure**:
1. Drain coolant from radiator and block
2. Fill with flush solution and water
3. Run engine to operating temperature
4. Drain and flush with clean water
5. Fill with proper coolant mixture (typically 50/50)
6. Bleed air from system

**Bleeding Air**:
- Some vehicles have bleeder valves
- Run engine with heater on high
- Add coolant as level drops
- Watch for bubbles stopping

---

## Lubrication System

### Oil Change Service

**Procedure**:
1. Warm engine slightly
2. Lift and support vehicle
3. Position drain pan
4. Remove drain plug
5. Allow to drain completely
6. Remove oil filter
7. Apply thin film of oil to new filter gasket
8. Install new filter (hand tight + 3/4 turn)
9. Install drain plug with new washer
10. Torque to spec (typically 25-35 ft-lbs)
11. Fill with specified oil quantity
12. Check level, start engine, recheck

### Oil Consumption Diagnosis

**Normal Consumption**: Up to 1 quart per 1,000-3,000 miles (varies by engine)

**Excessive Consumption Causes**:
- Worn valve seals (smoke on startup/decel)
- Worn piston rings (smoke under acceleration)
- PCV system issue
- External leak
- Turbo seal leak (turbocharged engines)

### Oil Analysis

**What Oil Analysis Reveals**:
- Wear metals (iron, copper, aluminum)
- Coolant contamination
- Fuel dilution
- Dirt ingression
- Oil breakdown

---

## Timing Belt/Chain Service

### Timing Belt

**Service Interval**: Typically 60,000-100,000 miles

**Interference vs. Non-Interference**:
- **Interference**: Valve damage if belt breaks
- **Non-Interference**: Engine stops but no valve damage

**Always replace with timing belt**:
- Water pump (usually accessible)
- Tensioner
- Idler pulleys
- Front crankshaft seal
- Cam seals (if accessible)

**General Procedure**:
1. Remove necessary components for access
2. Set engine to TDC cylinder 1
3. Mark all timing marks
4. Remove belt
5. Replace components
6. Install new belt
7. Verify timing marks
8. Rotate engine by hand 2 revolutions
9. Recheck marks
10. Reassemble

### Timing Chain

**Symptoms of Worn Chain**:
- Rattling noise on cold start
- Check engine light (cam/crank correlation code)
- Poor performance
- Hard starting

**Inspection**:
- Check chain stretch with chain deflection measurement
- Inspect guides and tensioners
- Check sprockets for wear

---

## Valve Train Service

### Valve Adjustment

**Types**:
1. **Mechanical (adjustable)**: Adjust with feeler gauge
2. **Hydraulic**: Self-adjusting
3. **Shim-over-bucket**: Adjust by replacing shims
4. **Shim-under-bucket**: Adjust by replacing shims (requires cam removal)

**Mechanical Adjustment Procedure**:
1. Engine cold (unless spec requires hot)
2. Rotate engine to TDC for cylinder being adjusted
3. Insert feeler gauge between cam/rocker and valve stem
4. Adjust to specified clearance
5. Typical specs: Intake 0.006-0.012", Exhaust 0.010-0.016"

### Valve Cover Gasket Replacement

**Common Oil Leak Location**

**Procedure**:
1. Remove accessories covering valve cover
2. Remove valve cover bolts
3. Carefully remove valve cover
4. Clean mating surfaces
5. Install new gasket (may need RTV at corners)
6. Install cover and torque to spec (typically 85-105 in-lbs)

---

## Engine Mechanical Repairs

### Head Gasket Replacement

**Symptoms of Head Gasket Failure**:
- External coolant leak
- Milky oil (coolant in oil)
- White smoke from exhaust (coolant in combustion)
- Bubbles in coolant reservoir
- Overheating
- Compression loss between cylinders

**Block Test (Combustion Leak Test)**:
1. Start with cold engine
2. Remove some coolant from reservoir
3. Install block tester
4. Start engine
5. If fluid changes color: Combustion gases in coolant

**Repair Procedure Overview**:
1. Drain fluids
2. Remove intake and exhaust manifolds
3. Remove valve cover
4. Remove timing cover/belt/chain
5. Remove head bolts in correct sequence
6. Remove head
7. Inspect head for warping (max 0.002" typically)
8. Clean deck surfaces
9. Install new head gasket (note proper orientation)
10. Install head with new bolts
11. Torque in proper sequence and steps
12. Reassemble

**Head Bolt Torque** (typical multi-step example):
1. Hand start all bolts
2. Torque all bolts to 25 ft-lbs
3. Torque all bolts to 50 ft-lbs
4. Torque all bolts to 75 ft-lbs
5. Additional angle tightening if spec requires (e.g., +90°)

### Intake Manifold Gasket

**Symptoms**:
- Vacuum leak (rough idle, lean codes)
- Coolant leak (some designs)
- Oil leak (some designs)

**Procedure**:
1. Drain coolant (if applicable)
2. Remove throttle body and fuel rail
3. Remove intake manifold bolts
4. Remove manifold
5. Clean surfaces
6. Install new gaskets
7. Torque to spec in proper sequence

### Oil Pan Gasket

**Procedure**:
1. Drain oil
2. Support engine if necessary
3. Remove oil pan bolts
4. Lower pan (may need to remove crossmember)
5. Clean surfaces
6. Apply RTV to corners/joints if required
7. Install new gasket
8. Torque bolts in sequence (typically 8-12 ft-lbs)

---

## Common Engine Repairs

### Spark Plug Replacement Intervals

| Plug Type | Interval |
|-----------|----------|
| Copper | 20,000-30,000 miles |
| Platinum | 60,000-100,000 miles |
| Iridium | 100,000+ miles |

### Drive Belt Replacement

**Inspection**:
- Cracks in belt ribs
- Missing chunks
- Glazed appearance
- Fraying
- Squealing noise

**Replacement**:
1. Note belt routing (take photo)
2. Release tensioner
3. Remove belt
4. Install new belt following routing diagram
5. Verify belt is seated properly in all pulleys

### PCV Valve Service

**Symptoms of Failed PCV**:
- Oil leaks (increased crankcase pressure)
- Oil consumption
- Rough idle (if stuck open)
- Sludge buildup (if stuck closed)

**Testing**:
1. Remove PCV valve
2. Shake - should rattle
3. Check for vacuum with engine running
4. Replace if stuck or restricted

---

## Engine Repair Decision Guide

### When to Repair vs. Replace Engine

**Consider Repair When**:
- Single component failure
- Engine has low mileage
- Vehicle has high value
- Known reliable engine

**Consider Replacement When**:
- Multiple issues
- High mileage with wear
- Catastrophic failure
- Repair cost approaches engine value

### Engine Replacement Options

| Option | Pros | Cons |
|--------|------|------|
| New | Warranty, reliability | Highest cost |
| Remanufactured | Warranty, quality | High cost |
| Used (junkyard) | Low cost | Unknown condition |
| Rebuilt in-house | Control quality | Labor intensive |

---

## Engine Diagnostic Tools

### Required Tools
- Compression tester
- Leak-down tester
- Fuel pressure gauge
- Vacuum gauge
- Timing light
- Stethoscope
- OBD-II scanner with live data

### Advanced Tools
- Lab scope
- Borescope
- Infrared thermometer
- Smoke machine
- Oil pressure gauge

---

## Related Resources

- [Diagnostics by Symptom](../diagnostics/README.md)
- [OBD-II Code Interpretation](../obd2-codes/README.md)
- [Fluid Specifications](../fluid-specs/README.md)
- [Torque Specifications](../torque-specs/README.md)
- [Maintenance Intervals](../maintenance-intervals/README.md)

---

*Last Updated: 2024*
*AHG Auto Repair Knowledge Base*
