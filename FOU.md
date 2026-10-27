# Foundation (FOU) engineering

[Home](README.md) · [Development overview](OffshoreWindDevelopment_note.md) · [WTG engineering](WTG.md)

## 1. Scope and design basis

This guide covers bottom-fixed WTG foundations, including monopiles (MP) and jackets (JKT). It describes a workflow rather than a complete design specification. Agree the governing requirements and editions using the [reference register](REFERENCES.md).

Before sizing, establish a controlled design input list and decision log containing:

- Metocean conditions: wind, waves, currents, water levels, directional distributions, joint occurrence, and uncertainties.
- Ground model and geotechnical interpretation: stratigraphy, strength, stiffness, cyclic response, and seismic conditions where relevant.
- WTG configuration: rotor–nacelle assembly, tower, controls, mass properties, interface geometry, and preliminary loads with their boundary assumptions.
- Design life, limit states, safety factors, fatigue methodology, tolerances, corrosion allowances, scour/seabed scenarios, and inspection assumptions.
- Fabrication, transport, installation, operation, access, and eventual removal constraints.

For every input, record its owner, revision, maturity, limitations, and required update date. Resolve missing inputs through explicit assumptions with closure actions.

## 2. Concept selection and dynamic behaviour

Compare monopile and jacket options against water depth, ground conditions, loads, fatigue, fabrication capacity, installation equipment, vessel access, environmental constraints, inspection needs, and lifetime cost.

- **Monopile:** investigate diameter, wall thickness, embedment, transition arrangement, lateral response, buckling, fatigue, and installation feasibility together.
- **Jacket:** investigate footprint, bays, member/joint geometry, pile arrangement, axial/lateral response, fabrication, and installation together. There is no universal order for optimizing these variables.

A first natural frequency between the rotor's 1P and blade-passing 3P ranges is a possible design strategy for a three-bladed turbine, not a universal requirement. Agree allowable frequency ranges and separation margins with the OEM and governing design basis. Assess the operating speed range, relevant modes, wave excitation, damping, soil uncertainty, and scour scenarios. A single nominal frequency check is insufficient to establish dynamic suitability.

**Output:** concept selection report with assumptions, governing constraints, rejected alternatives, and actions needed before FEED closure.

## 3. Location grouping and design envelopes

Grouping locations can reduce repeated design work, but do not prescribe a fixed number of clusters. Group using water depth, environmental exposure, soil response, loads, dynamic behaviour, and installation constraints.

The softest soil location does not necessarily govern every check. Select representative locations or bounding cases for distinct responses, such as fatigue, ultimate loading, frequency, rotation, axial capacity, and drivability. Demonstrate that every location is covered by the chosen envelope; split groups or verify individual locations where it is not.

**Output:** location-to-design mapping and evidence supporting each envelope.

## 4. Design load-case matrix

Agree a project-specific DLC matrix with the OEM, foundation designer, and reviewer. Use the applicable IEC requirements and project design basis; the [IEC 61400-3-1 reference](REFERENCES.md) identifies the offshore framework.

Do not use the former shorthand lists (`12`, `64`, etc.) as a design load specification. Record exact identifiers, standard edition, physical conditions, and applicability. If using identifiers such as `1.2`, preserve the decimal and confirm its meaning against the selected edition.

| Matrix field | What to record |
|---|---|
| Operating condition | Production, faults, start/stop, parked, or other applicable state |
| Environment | Wind/wave/current/water-level combinations, directions, and joint assumptions |
| Assessment | ULS, FLS, SLS, ALS as applicable; fatigue occurrence and exposure duration |
| Model and method | Turbine/control and support-structure revisions, soil/scour cases, damping, seeds/durations |
| Additional situations | Installation, maintenance, seismic, ice, collision, or other applicable hazards |
| Coverage and approval | Responsible party, exclusions with justification, reviewer status |

This table defines the information to capture, not a complete load-case list.

## 5. Integrated load analysis and convergence

1. **Agree the exchange:** define the interface point, coordinates, units, factors, load formats, model scope, and responsibilities using the [WTG interface register](WTG.md#6-minimal-interface-register).
2. **Prepare the support model:** include geometry, masses, stiffness, damping, soil response, and seabed/scour assumptions. Supply a reduced model or superelement only where compatible with the agreed analysis method.
3. **Verify model compatibility:** check modes, boundary conditions, environmental load application, and consistent turbine/control revisions. Avoid duplicated or missing hydrodynamic, inertial, or damping contributions.
4. **Run integrated simulations:** the contractually assigned party runs the agreed matrix. Exchange loads and supporting information sufficient for both turbine and foundation verification.
5. **Check and update:** assess the limit states and installation constraints below. Revise geometry, soil representation, controls, or assumptions when required, with both designers assessing the impact.
6. **Close the iteration:** demonstrate the project-defined load/stiffness convergence tolerances, acceptable design checks, location coverage, and closure of material review comments. Archive a matched model/load/design revision set.

Set convergence tolerances and acceptance limits in the design basis before using them for release; this guide does not prescribe numerical values. A new survey result or configuration change can reopen an earlier iteration.

## 6. Structural, geotechnical, and connection checks

| Area | Examples of checks to define in the project scope |
|---|---|
| ULS | Member and shell strength, buckling, combined loading, jacket joints, and connections |
| FLS | Welds, tubular joints, flanges and other details; lifetime operational and temporary-phase damage |
| SLS | Deflection, rotation, settlement, and equipment/interface limits |
| ALS | Applicable accidental situations, such as vessel collision, and agreed performance requirements |
| Geotechnical | MP lateral/axial response and embedment; jacket pile axial/lateral capacity, group effects, cyclic response, and deformations as applicable |
| Installation | Drivability, hammer and pile compatibility, refusal risk, driving stresses and fatigue, installation tolerances |
| Connections | Applicable bolted, grouted, or other connections, including TP–MP and jacket leg–pile details |

Demonstrate acceptance against the agreed criteria, including sensitivity to uncertain inputs. Geotechnical verification is broader than selecting embedment length, and drivability is broader than driving fatigue.

## 7. Linked design activities

These activities feed back into concept and detailed design; do not defer them automatically until the primary structure is frozen.

- **Scour and seabed mobility:** assess relevant seabed levels and protection scenarios; reflect their effects on soil support, exposed length, loads, and cable interfaces.
- **Transport and installation:** assess storage, load-out, transport, lifting, upending, driving, and temporary supports, including cumulative fatigue where applicable.
- **Secondary steel and access:** define platforms, boat landing, ladders, crane/laydown areas, grating, railings, maintainability, and safe access/evacuation interfaces.
- **Electrical interfaces:** define LV distribution, lighting, earthing/bonding, cable routing, and high-voltage (HV) cable support/hang-off requirements with electrical and cable designers.
- **Corrosion protection:** coordinate coatings, cathodic protection, corrosion allowance, electrical interfaces, design life, inspection, and maintenance assumptions.

## 8. Deliverables and release checks

| Stage | Main evidence | Typical ownership | Readiness check |
|---|---|---|---|
| Concept | Design basis, option comparison, initial dynamics and installation screening | Foundation designer; developer decision | Feasible option identified; uncertainties and survey needs owned |
| FEED | Preliminary sizing, ground model, load iteration, grouping plan, cost and installation basis | Foundation designer with OEM/site inputs | Governing assumptions traceable; material feasibility risks addressed or assigned |
| Detailed design | Integrated loads, limit-state reports, location coverage, drawings/specifications, review records | Foundation designer and OEM; review per agreed scope | Matched revisions verified; acceptance criteria met; material comments dispositioned |
| Fabrication / installation release | Approved release documents, tolerances, installation limits, change register | Designer and package owners; developer coordinates | Released configuration matches verification; required approvals and limitations communicated |

Keep an action log with decision, evidence, owner, due date, and approval status. The [worked example](WTG_Foundation_example.md) illustrates the handoffs without adding WBS levels.
