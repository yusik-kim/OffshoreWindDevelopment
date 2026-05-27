[Offshore Wind Development Structure](./README.md)


# Design process of Wind Turbine Generator (WTG)

---
 
# Summary 

All WTG activities in the [Offshore Wind Development Structure](./OffshoreWindDevelopment_note.md) are project-specific WTG Engineering. This includes: 

- Site-specific load calculations (wind class, turbulence, typhoon)
- Seismic verification (in APAC specifically)
- Tower height optimization
- Control tuning for grid code
- Transport adaptation
- Interface geometry confirmation
- Foundation load envelope issuance

The design described below is "OEM Platform Design" which is not part of WBS in Offshore Wind Development Structure. This design: 
- Take about 2 years 
- Is completed before Y1 in Offshore Wind Development Structure 
- Has type certificate


----


# 1. Market analysis & target definition

 Define target LCOE (levelized cost of energy), rated power, rotor diameter, and hub height according to the target wind class.

----

# 2.	Turbine concept & architecture selection

1.	Drivetrain: direct-drive vs medium-speed vs high-speed gearbox.
2. 	Generator: PM synchronous, electrically excited synchronous, DFIG etc.
3. 	Converter: full-scale vs partial-scale; DC-link sizing; filter topology.
4. 	Pitch & yaw: number of actuators, redundancy philosophy, emergency pitch.
5.	Braking: aerodynamic + mechanical brake, parking strategy, fail-safe behaviour.
6. 	Tower/support: steel tubular, hybrid, concrete; offshore jacket/monopile; floating substructure type.


-----


# 3.	Preliminary design 

1. 	Aerodynamic rotor design: \
    1.1	Aerofoil family selection, chord/twist distribution, root design constraint.\
    1.2	Optimize for AEP to loads, noise, transport constraints, and control stability. 


2.	Control design: \
    2.1	Basic set up: Cp tracking (power vs wind), pitch mapping and RPM limits. \
    2.2	Grid support functions and setpoint tracking strategy (active power, ramp rates, reactive power, voltage control).

3. 	Stability & frequency mapping:\
    3.1	Perform Campbell diagram analysis to ensure structural frequencies (tower 1st/2nd fore-aft) do not coincide with rotor 1p or 3p passing frequencies. \
    3.2	Assess aero-elastic damping.

4.	Define design load cases (DLC), based on IEC and run simulations.

5.	Load post processing and load feedback to components: \
    5.1	ULS and FLS.\
    5.2	Feed loads to blade, hub, main-shaft, tower, yaw, pitch.

6.	Initial design load envelope: Establish design load limit (e.g. max tip deflection, tower/blade root bending, main shaft torque).


-----

# 4.	Integrated component design
Based on the load inputs each component is developed further. 

1.	Blade: structural sizing (spar caps, shear webs), full-scale blade test.
2.	Tower: global buckling, local shell buckling, door openings, weld class, fatigue hotspots, transportation and erection constraints. 
3.	Drivetrain (hub, main shaft, main bearing): Bearing selection, shaft sizing for combined loads. 
4.	Generator: finalize gearbox ratios (if used), electromagnetic sizing, thermal design.
5.	Converter and electrical: (need help!).


-----

# 5. Load iteration & optimization
1.	Full load simulations with the updated components. 
2.	Previous steps repeat. 
3.	Optimization & load alleviations: if loads are below the envelope, reduce material; if over, apply control-based load redistribution. 
4.	Design freeze: final design load envelope; component design is frozen. 


-----


# 6. Type certification (not project specific)
1. Design basis evaluation -> Approved design basis document
2. Load calculation verification -> Load calculation review report
3. Structural design review -> Component design assessment report
4. Rotor blade testing -> Blade test certification
5. Control & Protection System Review -> Control system safety compliance report
6. Manufacturing Quality System Audit -> Manufacturing conformity statement
7. Prototype Testing -> Prototype validation report.



