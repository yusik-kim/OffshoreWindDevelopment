This is tutorial for OSS concept design : 

0) What 2.2.4.1 is trying to achieve

By the end of 2.2.4.1 you should be able to produce a concept package that answers:

What is the collection voltage? (typically 66 kV now)
Will there be an offshore export substation? (yes/no, and how many)
What export voltage and technology? (HVAC 220/275/330 kV, or HVDC for long distances)
How many transformers and what redundancy?
GIS or AIS?
What reactive power / voltage control equipment is needed?
How do you ground/earth and protect everything?
What auxiliary and emergency power philosophy is used?

Your deliverable: Single Line Diagram (SLD) Rev 0, plus a short Design Basis and an equipment list.

1) Step 1 — Start with three “project drivers”

Before you pick voltage levels, you need these three inputs:

A. Project scale
Total capacity: 1 GW (your case)
Turbine rating: e.g., 15 MW → ~67 turbines
B. Export distance and landfall constraints
Export route length offshore + onshore
Landfall HDD complexity can push you toward fewer cables/higher voltage
C. Grid connection requirements
Point of interconnection voltage (often 220/230/275/330 kV in APAC grids)
Utility demands for reactive support, fault ride-through, harmonic limits, SCADA protocol

If you don’t have grid code detail yet, you can still concept-design using a conservative “typical” grid requirement approach, but keep it flagged as a risk.

2) Step 2 — Choose inter-array (collection) voltage level
Most common today: 66 kV

Why 66 kV is now standard offshore:

Lower current for same power vs 33 kV → fewer cables or longer strings
Better suited for 12–20 MW turbines
Reduces I²R losses and voltage drop
Makes 1 GW feasible without insane cable counts
When 33 kV still shows up
Small projects, short strings, legacy turbines, limited 66 kV switchgear availability, or local supply constraints.
Practical example

If each turbine is 15 MW:

At 33 kV: current ≈ 15 MW / (√3 × 33 kV) ≈ 262 A
At 66 kV: current ≈ 131 A

So at 66 kV:

You can put more turbines per string before hitting thermal/voltage-drop limits.
Your cable cross-sections may be smaller for the same string power.

Rule of thumb:
If turbine rating ≥ 10 MW and project ≥ 500 MW → default to 66 kV unless the market/supply chain blocks it.

3) Step 3 — Decide HVAC vs HVDC and choose export voltage level
HVAC is typical if:
Export distance is moderate (commonly up to ~80–120 km depending on cable size and grid, and number of cables).
Grid is nearby and reactive compensation is manageable.
HVDC becomes attractive if:
Export distance is long (often >120–150 km) and cable charging currents become a major issue.
Grid integration prefers DC injection.

In APAC, most early projects are HVAC because HVDC offshore is more complex and cost-heavy, but long-distance markets may push HVDC.

Choosing the HVAC export voltage

Typical export voltages:

220 kV: common and widely supported
275 kV: also common in some grids
330 kV: for higher transfer per cable / fewer circuits

Rule of thumb approach (concept stage):

If you need many export cables at 220 kV, consider going up to 275/330 kV to reduce circuit count.
Match the onshore grid voltage if possible (minimize transformer stages).
Practical example (1 GW, HVAC)

You want export cable circuits that are not too many (installation risk and cost).

At 220 kV, depending on cable rating and assumptions, you might end up with ~3–4 export circuits.
At 275/330 kV, you might reduce the number of circuits.

Your concept decision becomes:

“Two OSS each exporting 500 MW with 2 export circuits total?” (bigger equipment, fewer cables)
“One OSS exporting 1 GW with 3–4 export circuits?” (single-point risk)
4) Step 4 — Decide OSS count and topology (1 OSS vs 2 OSS)

This is a critical concept decision.

One OSS (single)

Pros:

Lower CAPEX (one topside, one foundation)
Fewer offshore assets and O&M complexity

Cons:

Single point of failure
More IAC complexity in one collection hub
Larger/heavier topside (harder lift, fewer vessels can do it)
Two OSS (split into two ~500 MW hubs)

Pros:

Better redundancy and availability (a failure hits half the farm)
Smaller topsides easier to fabricate, transport, lift
IAC strings shorter (often)

Cons:

Higher CAPEX (two substations)
More interfaces, more commissioning complexity

Rule of thumb:
At ~1 GW scale, it’s common to seriously evaluate 2 OSS, especially where heavy lift vessel availability is constrained.

5) Step 5 — Transformer configuration (how many, what size, what redundancy)

You are stepping up from 66 kV to export voltage (e.g., 220/275/330 kV).

Common configurations:

Option A: 2 transformers, each 50% (N-1)
Each transformer can carry ~50% (or slightly more) of total station load
If one fails, you curtail but keep generating

Example for 500 MW OSS:

2 × 300 MVA transformers (allows some overload margin)

Pros:

Better availability
Easier maintenance strategy

Cons:

Higher weight and cost
Option B: 1 transformer, 100%

Example:

1 × 600–700 MVA transformer

Pros:

Lowest CAPEX, simplest
Cons:
Major single point failure → huge revenue risk

Developer reality: lenders and insurers often dislike “single transformer per OSS” for large hubs unless you have strong spares strategy.

Practical selection logic

For concept stage:

Decide if you are designing for N-1 at OSS level.
Decide allowable curtailment on single failure.

For a first-timer:

If you can afford it and vessels can lift it, 2 transformers per OSS is the safest concept.
6) Step 6 — GIS vs AIS (switchgear technology)
GIS (Gas Insulated Switchgear)

Pros:

Compact (critical offshore)
Better in salty, humid, contaminated environments
Lower footprint and smaller building volume

Cons:

Higher cost
SF₆ management requirements and environmental scrutiny
AIS (Air Insulated Switchgear)

Pros:

Cheaper, simpler gas management
Cons:
Bigger footprint (often not practical offshore)
More sensitive to corrosion and contamination

Offshore rule of thumb:
Use GIS for offshore substations unless you have a very special reason not to.

7) Step 7 — Reactive power / voltage control concept

Why you need it:

HVAC export cables generate reactive power (charging current)
Grid codes require voltage control and reactive capability at POI

Typical building blocks:

Shunt reactors (common offshore and/or onshore)
STATCOM / SVC (where dynamic reactive support is required)
Capacitor banks (less common offshore now, depends on design)
Practical concept approach

At FEED concept stage:

Assume you’ll need reactive compensation for the export system.
Decide where it sits:
Offshore (space/weight penalty)
Onshore (often preferred if grid operator allows)

Common arrangement:

Main reactive compensation onshore, with smaller offshore reactors if needed for energization steps.
8) Step 8 — Earthing / bonding concept

You need to define:

Earthing philosophy for HV and MV systems
Lightning protection bonding approach
Touch/step voltage requirements
How the OSS connects to seabed earthing system and export cable screens

Practical tip:

Offshore earthing is not the same as onshore — corrosion, seawater return paths, and cable screen bonding require careful consistency across OEMs and cable suppliers.

At concept stage, produce:

Earthing single line philosophy + bonding diagram principles.
9) Step 9 — Auxiliary power and emergency power philosophy

OSS needs power for:

HVAC systems
lighting
control systems
pumps
cranes
fire systems
communications

Typical concept:

Normal aux power from the 66 kV system via station service transformers
Emergency backup via:
diesel generator
UPS for critical control and protection
battery-backed emergency lighting

Key concept decision:

Black-start / energization sequence expectations (utility-dependent)
10) Output you should produce (as an entry engineer)

For 2.2.4.1, produce a small “concept pack”:

SLD Rev 0 showing:
66 kV switchgear sections
transformer(s)
export switchgear (GIS)
reactive equipment blocks (placeholders if not final)
station service transformers and emergency power
Equipment list:
MV GIS panels count estimate
transformer rating and quantity
HV GIS bays count estimate
reactors/STATCOM placeholders
auxiliaries (UPS, diesel gen)
Concept narrative:
why 66 kV
why 1 vs 2 OSS
transformer redundancy rationale
export voltage selection logic
reactive compensation philosophy
11) A simple “starter example” architecture (for a 1 GW HVAC concept)

One reasonable FEED concept you can use as a starting point:

Collection: 66 kV
Topology: 2 OSS × 500 MW
Transformers per OSS: 2 × ~300 MVA (N-1 concept)
Export: 220/275 kV HVAC (matched to grid POI where possible)
HV switchgear: GIS
Reactive: onshore primary, offshore allowance placeholder
Aux power: MV-fed station service + UPS + diesel gen

You’d then refine based on:

export distance and cable charging
local grid code requirements
available transformer/GIS manufacturing slots
heavy lift vessel constraints