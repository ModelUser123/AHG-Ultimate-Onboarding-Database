# AC/Heating Systems

## Complete HVAC Service and Repair Guide

This guide covers air conditioning, heating, and ventilation system diagnosis and repair.

---

## Table of Contents

1. [HVAC System Overview](#hvac-system-overview)
2. [Air Conditioning System](#air-conditioning-system)
3. [Heating System](#heating-system)
4. [Ventilation System](#ventilation-system)
5. [Diagnostics](#diagnostics)
6. [Common Repairs](#common-repairs)
7. [Refrigerant Handling](#refrigerant-handling)

---

## HVAC System Overview

### System Components

**Air Conditioning**:
- Compressor
- Condenser
- Evaporator
- Expansion device (orifice tube or TXV)
- Receiver-drier or accumulator
- Refrigerant lines
- AC clutch and pressure switches
- Refrigerant (R-134a or R-1234yf)

**Heating**:
- Heater core
- Heater hoses
- Heater control valve (some vehicles)
- Coolant (shared with engine)

**Ventilation**:
- Blower motor
- Blower resistor/module
- Blend door actuators
- Mode door actuators
- Ductwork
- Cabin air filter

---

## Air Conditioning System

### AC Operation Basics

**The Refrigeration Cycle**:

1. **Compressor**: Compresses low-pressure gas to high-pressure gas
2. **Condenser**: High-pressure gas releases heat, becomes high-pressure liquid
3. **Expansion Device**: High-pressure liquid becomes low-pressure liquid
4. **Evaporator**: Low-pressure liquid absorbs heat, becomes low-pressure gas
5. Cycle repeats

### AC System Pressures

**R-134a Typical Pressures** (at 80°F ambient):
| Location | Pressure |
|----------|----------|
| Low side (at rest) | 70-90 PSI |
| High side (at rest) | 70-90 PSI |
| Low side (running) | 25-40 PSI |
| High side (running) | 175-225 PSI |

**Pressure Relationships**:
| Condition | Low Side | High Side | Indication |
|-----------|----------|-----------|------------|
| Normal | 25-40 | 175-225 | System OK |
| Both low | Low | Low | Low charge/leak |
| Both high | High | High | Overcharge or poor cooling at condenser |
| Low side high, high side low | High | Low | Compressor weak or expansion device open |
| Low side very low | Very low | Normal/low | Restriction |

### AC Component Service

**Compressor**:
- Check for noise and proper engagement
- Inspect clutch air gap (typically 0.015-0.025")
- Check for oil leaks at shaft seal
- Verify proper oil charge when replacing

**Condenser**:
- Inspect for debris and damage
- Check for leaks at connections
- Ensure adequate airflow

**Evaporator**:
- Usually not visible
- Check for leaks (dye or electronic detector)
- Inspect drain for blockage

**Expansion Device**:
- Orifice tube: Check for debris, inspect screen
- TXV: Check for proper superheat

### AC Performance Testing

**Procedure**:
1. Connect manifold gauges
2. Start engine, set AC to max cold, high blower
3. Allow system to stabilize (5 minutes)
4. Record pressures
5. Measure vent temperature

**Vent Temperature Goals**:
| Ambient Temp | Vent Temp Target |
|--------------|------------------|
| 70°F | 35-45°F |
| 80°F | 40-50°F |
| 90°F | 45-55°F |
| 100°F | 50-60°F |

---

## Heating System

### Heater Operation

- Engine coolant flows through heater core
- Blower forces air through heater core
- Blend door controls how much air passes through core
- Heat is absorbed from coolant into cabin

### Heater System Diagnosis

**No Heat Symptoms**:

| Symptom | Likely Cause |
|---------|--------------|
| No heat, both hoses cool | Low coolant, thermostat stuck open |
| No heat, one hose hot | Heater core clogged, control valve stuck |
| No heat, both hoses hot | Blend door stuck, airflow issue |
| Heat intermittent | Air in system, low coolant |
| Sweet smell, foggy windows | Heater core leak |

### Heater Core Service

**Flush Procedure** (for restricted core):
1. Disconnect heater hoses
2. Flush with water or chemical flush
3. Flush until clear
4. Reconnect hoses

**Replacement** (location varies significantly by vehicle):
- Often requires dashboard removal
- Labor intensive (4-10 hours typical)
- Replace hoses and thermostat while accessible

---

## Ventilation System

### Blower Motor System

**Components**:
- Blower motor
- Blower resistor or module
- Blower relay
- Blower switch

**Blower Motor Diagnosis**:

| Symptom | Likely Cause |
|---------|--------------|
| No operation at any speed | Blown fuse, motor, relay |
| Works on high only | Resistor or module |
| Works on some speeds | Resistor, switch |
| Weak airflow all speeds | Motor wearing, debris |
| Noise from blower | Motor bearings, debris |

**Resistor Testing**:
1. Locate resistor (usually near blower motor)
2. Measure resistance between terminals
3. Compare to specification
4. Look for burned/melted appearance

### Blend Door Actuators

**Function**: Control temperature mix (hot/cold)

**Symptoms of Failure**:
- Clicking noise from dash
- Temp stuck hot or cold
- Temperature inconsistent

**Diagnosis**:
1. Operate temp control
2. Listen for actuator movement
3. Use scan tool to command actuator
4. Check for binding or broken door

### Mode Door Actuators

**Function**: Control air direction (defrost, floor, panel)

**Symptoms of Failure**:
- Air only from one location
- Clicking when changing modes

### Cabin Air Filter

**Function**: Filters air entering cabin

**Service Interval**: 15,000-30,000 miles or annually

**Replacement**:
1. Locate filter (glove box, under dash, or under hood)
2. Remove filter access panel
3. Note filter orientation
4. Install new filter
5. Reinstall access panel

---

## Diagnostics

### AC System Diagnostic Flowchart

```
AC Not Cooling
├── Compressor Running?
│   ├── NO → Check pressure switch, fuse, relay, clutch
│   │   └── Low charge → Leak test, repair, recharge
│   └── YES → Check pressures
│       ├── Normal pressures, poor cooling
│       │   └── Check blend door, airflow, evaporator
│       ├── Low side high, high side low
│       │   └── Compressor weak or internal issue
│       ├── Both sides low
│       │   └── Low charge, leak in system
│       ├── Both sides high
│       │   └── Overcharge, condenser cooling issue
│       └── Low side vacuum/very low
│           └── Restriction in system
```

### Leak Detection Methods

1. **Electronic Leak Detector**
   - Most sensitive method
   - Can find small leaks

2. **UV Dye**
   - Add dye to system
   - Inspect with UV light
   - Shows leak location

3. **Soap Solution**
   - Spray on connections
   - Bubbles indicate leak
   - Good for larger leaks

4. **Nitrogen Pressure Test**
   - Pressurize with nitrogen
   - Submerge components or use soap

### HVAC Scan Tool Data

**Key Parameters**:
| Parameter | Use |
|-----------|-----|
| AC pressure switch | Verify switch operation |
| AC clutch command | Verify PCM is commanding clutch |
| Blend door position | Verify actuator position |
| Mode door position | Verify mode selection |
| Blower speed command | Verify control module operation |
| Inside/outside temp | Temperature sensor input |

---

## Common Repairs

### AC Recharge Procedure

**Tools Required**:
- Manifold gauges
- Vacuum pump
- Refrigerant
- Scale
- Leak detector

**Procedure**:
1. Connect manifold gauges
2. Check existing pressures
3. Recover remaining refrigerant
4. Evacuate system (15-30 minutes minimum)
5. Hold vacuum - if gauge rises, leak present
6. Charge system by weight to specification
7. Run system and verify pressures
8. Check vent temperatures
9. Leak check connections

**Refrigerant Charge** (typical):
- Most vehicles: 1.5-2.5 lbs R-134a
- Always use vehicle-specific specification

### Compressor Replacement

**Procedure**:
1. Recover refrigerant
2. Disconnect electrical connector
3. Remove refrigerant lines
4. Remove mounting bolts
5. Remove compressor
6. Drain and measure oil from old compressor
7. Add correct amount of new oil to new compressor
8. Install new compressor
9. Replace receiver-drier or accumulator
10. Replace orifice tube if equipped
11. Evacuate and recharge system
12. Add proper amount of PAG oil

**Oil Notes**:
- Use oil specified for compressor
- PAG 46, PAG 100, or PAG 150 (varies)
- R-1234yf uses specific oil

### Condenser Replacement

**Procedure**:
1. Recover refrigerant
2. Remove bumper cover/grille as needed
3. Disconnect refrigerant lines
4. Remove condenser mounting
5. Install new condenser
6. Replace receiver-drier (often integrated)
7. Add proper oil amount
8. Evacuate and recharge

### Evaporator Replacement

**Procedure** (varies significantly by vehicle):
1. Recover refrigerant
2. Remove dashboard (often required)
3. Remove HVAC housing
4. Separate housing
5. Remove evaporator
6. Install new evaporator
7. Replace expansion device
8. Reassemble
9. Evacuate and recharge

---

## Refrigerant Handling

### EPA Section 608/609 Requirements

**Requirements**:
- Technicians must be certified
- Refrigerant must be recovered, not vented
- Records must be kept
- Proper equipment required

### R-134a vs R-1234yf

| Property | R-134a | R-1234yf |
|----------|--------|----------|
| GWP | 1430 | 4 |
| Service ports | Standard | Unique |
| Oil type | PAG | Specific PAG |
| Machine | Standard | Dedicated |
| Cost | Lower | Higher |
| Flammability | Low | Mildly flammable |

### Safety Precautions

1. **Eye Protection**: Always wear safety glasses
2. **Skin Protection**: Refrigerant causes frostbite
3. **Ventilation**: Work in well-ventilated area
4. **Flammability**: R-1234yf is mildly flammable
5. **Pressure**: Systems are under high pressure
6. **Recovery**: Never vent refrigerant

---

## HVAC System Quick Reference

### Common AC Issues by Symptom

| Symptom | First Check | Second Check |
|---------|-------------|--------------|
| No cold air | Compressor engaging | Refrigerant level |
| Weak cooling | Cabin filter | Evaporator/condenser |
| Intermittent cooling | Compressor clutch | Pressure switches |
| AC smell | Evaporator mold | Cabin filter |
| Noise when AC on | Compressor | Idler/tensioner |

### Refrigerant Capacity by Make (Examples)

| Make | Model | Capacity |
|------|-------|----------|
| Ford | F-150 | 28-36 oz |
| Toyota | Camry | 16-22 oz |
| Honda | Accord | 18-22 oz |
| Chevrolet | Silverado | 28-36 oz |

*Always verify with vehicle-specific specification*

---

## Related Resources

- [Diagnostics by Symptom](../diagnostics/README.md)
- [Electrical Troubleshooting](../electrical/README.md)
- [Fluid Specifications](../fluid-specs/README.md)
- [Customer Communication](../customer-communication/README.md)

---

*Last Updated: 2024*
*AHG Auto Repair Knowledge Base*
