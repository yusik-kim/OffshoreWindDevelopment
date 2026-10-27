# Wind turbine generator (WTG) engineering

[Home](README.md) · [Development overview](OffshoreWindDevelopment_note.md) · [Foundation engineering](FOU.md)

## 1. Scope: platform development and project engineering

OEM platform development creates a turbine product and establishes its design envelope. Project engineering demonstrates that the selected configuration is suitable for a particular site and support structure. Type certification does not replace site-specific assessment or the agreed project certification scope; see the [reference register](REFERENCES.md).

Platform development may overlap project development. Neither a fixed two-year platform programme nor certification before project Year 1 is assumed. Track certificate scope, outstanding conditions, configuration changes, and the required completion dates as procurement risks.

## 2. OEM platform development: context

The developer normally assesses the maturity and suitability of these activities rather than performing them.

1. **Targets and architecture:** define target LCOE, rating, rotor diameter, wind/environmental envelope, drivetrain, generator, converter, pitch/yaw, braking, and tower interfaces.
2. **Preliminary design:** develop aerodynamics and controls; evaluate energy yield, loads, clearances, structural frequencies, damping, and operational limits.
3. **Component engineering:** size and verify blades, hub, shaft, bearings, gearbox where used, generator, tower, and connections. Coordinate mechanical and electrical interfaces.
4. **Converter and electrical engineering:** define converter topology and ratings, generator/converter thermal limits, transformer and switchgear interfaces, insulation, earthing, protection, power quality, and grid-support controls. Validate equipment and models against the declared platform envelope.
5. **Iteration and validation:** update coupled simulations, reconcile component loads, validate models against tests, and freeze a controlled configuration. Load mitigation changes require checks across components, controls, energy yield, and certification scope.
6. **Type certification:** complete the modules and close conditions required by the selected scheme, including design evaluation, testing, manufacturing evaluation, and final evaluation as applicable. Record exactly which turbine variants the certificate covers.

## 3. Project-specific selection and site suitability

Compare candidates on lifetime value and delivery risk, not rated power alone.

| Topic | Inputs and assessment | Expected output |
|---|---|---|
| Site envelope | Wind extremes, turbulence and wakes, metocean, temperature, corrosion exposure, and seismic/ice/tropical-cyclone conditions where relevant | Site suitability assessment and deviations from the platform envelope |
| Configuration | Rotor, hub height, tower, controls, electrical configuration, and consent constraints | Controlled project configuration and certificate applicability review |
| Energy and value | Yield, wake losses, availability assumptions, curtailment, support-structure cost, installation and maintenance constraints | Comparable AEP and lifetime-cost assessment with uncertainty |
| Grid interface | Connection requirements, electrical models, plant-controller responsibilities | Compliance study plan and agreed WTG/plant boundaries |
| Delivery and service | Manufacturing slots, ports, vessels, lifting, spares, access, warranty and service strategy | Deliverability assessment and residual-risk register |

A selection decision may remain conditional on survey results, load verification, certification, or commercial terms. Assign each condition an owner and closure date.

## 4. WTG–foundation integrated design

The tower–foundation boundary must be defined contractually; it is not identical for every turbine or foundation concept.

1. Agree the interface elevation, coordinate system, units, sign conventions, load reference points, and tower ownership.
2. Issue preliminary loads with their boundary-condition assumptions. A rigid-base load envelope is a screening input, not automatically the final foundation design load.
3. Exchange the structural representation, soil assumptions, damping, mass properties, and environmental inputs required by the agreed coupled-analysis method.
4. Run the agreed DLC matrix and exchange interface loads, time histories or other agreed representations, cycle information, and model revision identifiers.
5. Check turbine, tower, foundation, soil response, clearances, and dynamic behaviour; update the model and repeat where required.
6. Freeze the matched turbine/control and support-structure configuration only after the agreed convergence criteria and reviews are satisfied.

The party running the coupled model depends on the contract and tools. Avoid gaps or double counting of wave loading, damping, inertia, or safety factors. See the [foundation workflow](FOU.md#5-integrated-load-analysis-and-convergence).

## 5. Deliverables and readiness checks

Responsibilities below are illustrative and must be confirmed in the contracts.

| Decision | Evidence | Typical responsibility | Readiness check |
|---|---|---|---|
| Preferred WTG | Candidate comparison, site screening, configuration and certification status | Developer with OEM inputs | Selection rationale documented; material conditions owned and scheduled |
| FEED load basis | Preliminary loads, model assumptions, interface definition, DLC plan | OEM and foundation designer; developer coordinates | Both parties use compatible revisions; limitations and remaining surveys recorded |
| Detailed design freeze | Final integrated loads, turbine/tower suitability, foundation checks, review records | OEM and foundation designer; independent review per agreed scope | Project-defined convergence met; material comments closed or formally dispositioned |
| Manufacturing / installation release | Released drawings and specifications, change status, installation limits, required approvals | Package owners and developer | Required approvals available; configuration matches the verified design |

A later change to controls, tower, soil model, or foundation stiffness triggers an impact assessment. Record whether loads, design checks, certification, manufacturing, or installation documents need revision.

## 6. Minimal interface register

Maintain this as a project record, with actual revision identifiers and due dates.

| Exchange | Issuer → receiver | Record with each issue |
|---|---|---|
| Turbine configuration and preliminary loads | OEM → foundation designer | Configuration, coordinate system, boundary assumptions, limitations |
| Support-structure model | Foundation designer → load-analysis party | Geometry, mass, stiffness, damping, soil/scour assumptions, validity range |
| Integrated load package | Load-analysis party → both designers | DLC coverage, model versions, load format, factors, missing cases |
| Interface geometry and connections | Tower/foundation owners → each other | Elevations, tolerances, flange/connection definition, access constraints |
| Design changes and acceptance | Both designers → developer/reviewer | Impact assessment, action owner, due date, approval status |

Use the [worked example](WTG_Foundation_example.md) to follow one iteration through these exchanges.
