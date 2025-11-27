# Diagnostics by Symptom

## Quick Symptom Index

This guide provides diagnostic pathways based on customer-reported symptoms. Each section includes probable causes, diagnostic steps, and repair recommendations.

---

## Table of Contents

1. [Engine/Drivetrain Symptoms](#enginedrivetrain-symptoms)
2. [Brake Symptoms](#brake-symptoms)
3. [Steering/Handling Symptoms](#steeringhandling-symptoms)
4. [Electrical Symptoms](#electrical-symptoms)
5. [HVAC Symptoms](#hvac-symptoms)
6. [Noise Symptoms](#noise-symptoms)
7. [Fluid Leak Symptoms](#fluid-leak-symptoms)

---

## Engine/Drivetrain Symptoms

### Car Won't Start - No Crank

**Customer Description**: "The car does nothing when I turn the key"

**Probable Causes** (in order of likelihood):
1. Dead battery
2. Corroded or loose battery connections
3. Faulty starter motor
4. Faulty starter relay/solenoid
5. Ignition switch failure
6. Neutral safety switch malfunction
7. Anti-theft system engaged

**Diagnostic Steps**:
1. Check battery voltage (should be 12.4V+ at rest, 9.6V+ while cranking)
2. Inspect battery terminals for corrosion
3. Test starter draw (normal: 150-200 amps for 4-cylinder, 200-250 for V8)
4. Check for voltage at starter "S" terminal while cranking
5. Verify neutral safety switch operation (shift to neutral and try)
6. Check all grounds

**Repair Timeline**: 30 min - 2 hours depending on cause

---

### Car Won't Start - Cranks But Won't Fire

**Customer Description**: "It turns over but won't start"

**Probable Causes**:
1. No fuel (empty tank or fuel pump failure)
2. No spark (ignition system failure)
3. Timing issue (jumped timing chain/belt)
4. Compression loss
5. Crank/cam sensor failure
6. Immobilizer/security system issue

**Diagnostic Steps**:
1. Check for fuel pressure at rail (spec varies by vehicle, typically 40-60 PSI)
2. Check for spark at plugs
3. Verify crank and cam sensor signals with scan tool
4. Check for injector pulse
5. Compression test if other systems OK

**Decision Tree**:
```
Cranks but no start
├── Has fuel pressure?
│   ├── NO → Check fuel pump relay, fuse, pump
│   └── YES → Check for spark
│       ├── NO → Check ignition coils, CKP sensor, timing
│       └── YES → Check for injector pulse
│           ├── NO → Check PCM power/ground, CKP/CMP sensors
│           └── YES → Compression test, timing check
```

---

### Engine Runs Rough/Misfires

**Customer Description**: "The engine shakes" or "It feels like it's missing"

**Probable Causes**:
1. Worn spark plugs
2. Faulty ignition coil(s)
3. Vacuum leak
4. Fuel injector issue
5. Compression loss (head gasket, valves)
6. Mass air flow sensor contaminated
7. EGR valve stuck open

**Diagnostic Steps**:
1. Scan for misfire codes - identify which cylinder(s)
2. Swap coils/injectors to confirm component failure
3. Check spark plug condition
4. Smoke test for vacuum leaks
5. Check fuel trim data (STFT/LTFT should be ±10%)
6. Compression/leak-down test if needed

**Repair Timeline**: 1-4 hours depending on cause

---

### Engine Overheating

**Customer Description**: "The temperature gauge goes into the red"

**Probable Causes**:
1. Low coolant level (leak or consumption)
2. Thermostat stuck closed
3. Radiator clogged or restricted
4. Cooling fan not operating
5. Water pump failure
6. Head gasket failure
7. Radiator cap not holding pressure

**Diagnostic Steps**:
1. Visual inspection for leaks
2. Pressure test cooling system (15-16 PSI typical)
3. Check thermostat operation
4. Verify fan operation (check relay, temp switch)
5. Flow test radiator
6. Combustion leak test (block test)
7. Check for milky oil or coolant in exhaust

**CRITICAL**: Do not remove radiator cap when hot. Wait for engine to cool.

---

### Check Engine Light On

**Customer Description**: "The check engine light came on"

**Diagnostic Steps**:
1. Retrieve DTCs with scan tool
2. Check freeze frame data
3. Research TSBs for that code/vehicle
4. Perform pinpoint tests per diagnostic chart
5. Clear codes and road test to verify repair

**Common Code Categories**:
- P0xxx: Powertrain codes
- P0100-0199: Fuel and air metering
- P0200-0299: Fuel and air metering (injector circuit)
- P0300-0399: Ignition system or misfire
- P0400-0499: Emission controls
- P0500-0599: Vehicle speed and idle control

See [OBD-II Code Interpretation](../obd2-codes/README.md) for complete code reference.

---

## Brake Symptoms

### Brake Pedal Feels Soft/Spongy

**Customer Description**: "The brake pedal goes down too far"

**Probable Causes**:
1. Air in brake lines
2. Brake fluid leak
3. Worn brake pads/shoes
4. Faulty master cylinder
5. Brake hose internal deterioration
6. ABS module malfunction

**Diagnostic Steps**:
1. Check brake fluid level
2. Visual inspection of all brake components
3. Check for external leaks at calipers, lines, master cylinder
4. Bleed brakes and evaluate pedal
5. If still soft after bleed, inspect master cylinder
6. Check for internal hose collapse (may need to disconnect caliper)

---

### Brake Pedal Pulsation

**Customer Description**: "The brake pedal vibrates when I stop"

**Probable Causes**:
1. Warped brake rotors
2. Rotor thickness variation
3. Loose wheel bearing
4. Worn suspension components

**Diagnostic Steps**:
1. Measure rotor runout (max 0.002" - 0.003" typically)
2. Measure rotor thickness variation (max 0.0005" typically)
3. Check wheel bearing play
4. Inspect suspension components

**Note**: Pulsation felt in steering wheel = front brakes
Pulsation felt in brake pedal only = rear brakes

---

### Brakes Pull to One Side

**Customer Description**: "The car pulls when I brake"

**Probable Causes**:
1. Seized caliper or slide pins
2. Contaminated brake pads (oil/grease)
3. Collapsed brake hose
4. Uneven pad wear
5. Worn suspension allowing alignment change under braking

**Diagnostic Steps**:
1. Road test to confirm symptom
2. Inspect caliper slide pins for free movement
3. Check brake hose condition
4. Inspect pad condition and wear pattern
5. Compare rotor temperatures after test drive

---

### Grinding Noise When Braking

**Customer Description**: "I hear a grinding sound when I brake"

**Probable Causes**:
1. Worn brake pads (metal on metal)
2. Debris caught in brakes
3. Rust on rotors after sitting
4. Damaged brake hardware

**Diagnostic Steps**:
1. Immediate inspection required
2. Check pad thickness (minimum 2-3mm typically)
3. Inspect rotor surface for scoring
4. Look for broken hardware or debris

**IMPORTANT**: Advise customer to drive carefully. Worn pads can cause rotor damage and caliper piston damage, significantly increasing repair cost.

---

## Steering/Handling Symptoms

### Vehicle Pulls to One Side

**Customer Description**: "The car drifts to the right/left"

**Probable Causes**:
1. Tire pressure difference
2. Alignment out of spec
3. Brake dragging
4. Worn tire (conicity)
5. Worn steering/suspension components

**Diagnostic Steps**:
1. Check and equalize tire pressures
2. Check alignment specs
3. Road test for brake drag (feel wheel temps after driving)
4. Swap front tires side to side - if pull changes direction, tire conicity
5. Inspect steering and suspension components

---

### Steering Wheel Vibration

**Customer Description**: "The steering wheel shakes at highway speed"

**Probable Causes**:
1. Wheel balance
2. Bent wheel
3. Tire defect (flat spot, bulge, separation)
4. Worn tie rod ends
5. Worn ball joints
6. Warped brake rotors (if during braking)

**Diagnostic Steps**:
1. Road test to identify speed range of vibration
2. Visual tire inspection
3. Balance wheels
4. Check for bent wheels
5. Inspect steering/suspension components
6. If during braking only, see brake section

**Speed Correlation**:
- 40-50 mph: Usually front wheel balance
- 55-70 mph: Usually rear wheel balance or driveline
- All speeds: Tire defect or bent wheel

---

### Clunk/Noise When Turning

**Customer Description**: "I hear a clunk when turning"

**Probable Causes**:
1. Worn CV joint/axle (clicking when turning)
2. Worn ball joints
3. Worn tie rod ends
4. Loose/worn strut mount
5. Worn sway bar links/bushings
6. Worn steering shaft U-joint

**Diagnostic Steps**:
1. Test drive - note if noise is during acceleration, coasting, or braking
2. CV joint clicking = typically under acceleration
3. Bounce test for strut mounts
4. Check ball joints and tie rods with vehicle on ground (loaded)
5. Check sway bar links (push/pull by hand)

---

## Electrical Symptoms

### Battery Keeps Dying

**Customer Description**: "I have to jump start every morning"

**Probable Causes**:
1. Parasitic draw (something staying on)
2. Failing battery
3. Faulty alternator
4. Corroded connections
5. Aftermarket accessory wired incorrectly

**Diagnostic Steps**:
1. Load test battery
2. Check alternator output (13.5-14.5V at idle)
3. Parasitic draw test:
   - All modules asleep (may take 30+ minutes)
   - Normal draw: 20-50mA
   - Pull fuses to isolate circuit

**Parasitic Draw Procedure**:
1. Connect ammeter in series with battery
2. Wait for modules to go to sleep
3. If draw >50mA, remove fuses one at a time
4. When draw drops, you've found the problem circuit
5. Trace circuit to find cause

---

### Lights Flickering/Dimming

**Customer Description**: "My lights flicker or dim"

**Probable Causes**:
1. Loose/corroded battery connections
2. Failing alternator
3. Loose ground connection
4. Failing headlight switch
5. Voltage drop in circuit

**Diagnostic Steps**:
1. Clean and tighten battery connections
2. Check all ground connections
3. Test alternator output under load
4. Voltage drop test on charging circuit
5. Check for ripple voltage (failing diode in alternator)

---

### No Power/Accessories Don't Work

**Customer Description**: "Nothing works in my car"

**Probable Causes**:
1. Blown fusible link
2. Main fuse blown
3. Battery connection issue
4. Ignition switch failure

**Diagnostic Steps**:
1. Check battery connections
2. Check fusible links at battery
3. Check main fuses in underhood fuse box
4. Test for voltage at fuse box
5. Check ignition switch power delivery

---

## HVAC Symptoms

### AC Not Cooling

**Customer Description**: "The AC blows warm air"

**Probable Causes**:
1. Low refrigerant (leak)
2. Compressor not engaging
3. Condenser fan not working
4. Clogged condenser
5. Expansion valve/orifice tube clogged
6. Compressor failure
7. Blend door stuck

**Diagnostic Steps**:
1. Check if compressor is engaging
2. Check refrigerant pressures (low and high side)
3. Check for blend door operation (feel temp at vents while adjusting)
4. If compressor not engaging, check:
   - Refrigerant level (low pressure switch)
   - Clutch gap
   - Power and ground to clutch
   - Pressure switch operation

**Pressure Guide** (R-134a at 80°F ambient):
- Low side: 25-35 PSI
- High side: 175-225 PSI

---

### Heater Not Working

**Customer Description**: "No heat from vents"

**Probable Causes**:
1. Low coolant level
2. Thermostat stuck open
3. Clogged heater core
4. Blend door not operating
5. Heater control valve stuck (if equipped)

**Diagnostic Steps**:
1. Check coolant level (fill if low)
2. Check both heater hoses - both should be hot
   - One hot, one cool = clogged core or control valve
3. Check thermostat operation (gauge should reach normal)
4. Check blend door operation

---

### Blower Motor Not Working

**Customer Description**: "No air comes from vents"

**Probable Causes**:
1. Blown blower fuse
2. Faulty blower motor resistor
3. Faulty blower motor
4. Faulty blower relay
5. Faulty blower switch
6. Wiring issue

**Diagnostic Steps**:
1. Check fuse
2. Check for power and ground at blower motor
3. Apply direct power to blower motor to test
4. If works on high only, resistor is faulty
5. Check for power at resistor input

---

## Noise Symptoms

### Squealing on Startup

**Customer Description**: "I hear a squeal when I first start the car"

**Probable Causes**:
1. Serpentine belt worn/glazed
2. Belt tensioner weak
3. Pulley misalignment
4. Idler pulley bearing failing

**Diagnostic Steps**:
1. Spray water on belt - if squeal stops temporarily, belt is cause
2. Inspect belt for cracks, glazing
3. Check tensioner tension and movement
4. Check pulley alignment
5. Spin pulleys by hand (engine off) - listen/feel for bearing roughness

---

### Knocking/Ticking from Engine

**Customer Description**: "Engine makes a knocking or ticking sound"

**Probable Causes**:
1. Low oil level
2. Wrong oil viscosity
3. Worn hydraulic lifters
4. Exhaust leak
5. Rod/main bearing wear
6. Piston slap
7. Worn timing chain

**Diagnostic Steps**:
1. Check oil level and condition
2. Listen with stethoscope to isolate location
3. Check for exhaust leaks (manifold bolts, flex pipe)
4. Lifter tick - often worse on cold start, improves when warm
5. Rod knock - increases with RPM, worse under load
6. Piston slap - worse when cold, improves when warm

**CRITICAL**: If oil pressure warning light is on with noise, do not run engine. Check oil level immediately.

---

### Grinding When Shifting (Manual)

**Customer Description**: "It grinds when I shift gears"

**Probable Causes**:
1. Clutch not fully releasing
2. Worn synchronizers
3. Low transmission fluid
4. Worn clutch master/slave cylinder

**Diagnostic Steps**:
1. Check clutch pedal free play
2. Check fluid level in clutch master (if hydraulic)
3. Check for full clutch release at pedal
4. If grinds on all gears, likely clutch release issue
5. If grinds on specific gear, likely synchronizer

---

## Fluid Leak Symptoms

### Fluid Identification Guide

| Color | Consistency | Sweet Smell? | Likely Fluid |
|-------|-------------|--------------|--------------|
| Green, Orange, Pink | Watery | Yes | Coolant |
| Red, Pink | Thin/oily | No | Transmission fluid |
| Red | Thin/oily | No | Power steering |
| Dark brown/black | Thick/oily | No | Engine oil |
| Light brown | Oily | No | New engine oil or brake fluid |
| Clear | Watery | No | Water (AC drain) |
| Amber | Oily | No | Brake fluid |

### Finding the Leak Source

**Procedure**:
1. Clean affected area
2. Add UV dye to suspected system
3. Run vehicle
4. Inspect with UV light
5. Trace dye trail to highest point

**Common Leak Locations**:
- **Oil**: Valve cover gaskets, oil pan gasket, rear main seal, oil filter, drain plug
- **Coolant**: Hoses, water pump, radiator, heater core, intake manifold gasket
- **Trans fluid**: Pan gasket, cooler lines, axle seals, input shaft seal
- **Power steering**: Pump, rack seals, hoses, reservoir

---

## Diagnostic Equipment Checklist

### Essential Equipment
- [ ] OBD-II scan tool with live data
- [ ] Digital multimeter
- [ ] Brake pressure gauge
- [ ] Fuel pressure gauge
- [ ] Compression tester
- [ ] Cooling system pressure tester
- [ ] AC manifold gauges
- [ ] Stethoscope
- [ ] UV light and dye kit
- [ ] Smoke machine

### Advanced Equipment
- [ ] Oscilloscope
- [ ] Lab scope
- [ ] Fuel injector tester
- [ ] Battery/charging system analyzer
- [ ] Leak-down tester
- [ ] Borescope

---

## Related Resources

- [OBD-II Code Interpretation](../obd2-codes/README.md)
- [Decision Trees](../decision-trees/README.md)
- [Brake Systems](../brake-systems/README.md)
- [Engine Repair](../engine-repair/README.md)
- [Electrical Troubleshooting](../electrical/README.md)

---

*Last Updated: 2024*
*AHG Auto Repair Knowledge Base*
