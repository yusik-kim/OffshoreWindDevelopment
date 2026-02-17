[Offshore Wind Development Structure](./OffshoreWindDevelopment_note.md)

# Design process of Foundation (FOU)


-----


# Summary 
It describes design process of bottom-fixed offshore wind foundation. 


-----


# 1.	Design basis / design input list / decision log
    a.	Metocean data: statistics of wind, waves, current, water level, directionalities, joint probability. 
    b.	Geotechnical interpretation report (GIR): soil stratifications, geotechnical properties (strength/stiffness profile), cyclic degradation effects, seismic data.
    c.	WTG data: 
        i.	Specifications for WTG including blades, hub, nacelle, tower. 
        ii.	Operational control parameter: wind vs power, pitch, RPM. 
        iii.	Preliminary loads at FOU-WTG interface based on fixed bottom, without hydro loads.
    d.	Governing standards 
    e.	Design input list (DIL): complete list of design inputs from all stakeholders. 
    f.	Decision log: all design decisions agreed and approved by the client.


-----


# 2.	FOU concept sizing and frequency tuning
The target system frequency (FOU+WTG) shall be between 1P and 3P. 

    a.	Monopile (MP):
        i.	Set outer diameter (OD) and wall thickness (t) driven by buckling and global bending stiffness. 
        ii.	Set embedment length (L) driven by lateral stiffness.
        iii.	Adjust OD, t, L to tune frequency and also consider installation constraint. 
    b.	Jacket (JKT): 
        i.	Set number of bays depending on the water depth.
        ii.	Set footprint driven by global torsion and bending stiffness. 
        iii.	To tune frequency, adjust variables in a following order: geometry (footprint, number of bay) > member size (OD and t for leg and braces) > pile (penetration length). 
    c.	What to consider to select MP vs. Jacket: 
        i.	Water depth. 
        ii.	Manufacturability of piles with large OD.
        iii.	Soil stiffness and Drivability.


-----



# 3.	Clustering: 
    a.	Grouping WTG positions based on water depth, geotech properties, and dynamic behaviour. Typically, 2-3 groupings are adopted for utility scale wind farms. 
    b.	Select representative position at each group. Generally, softest location is selected. 


-----


# 4.	Define FOU specific design load cases (DLCs) with WTG supplier: 
    a.	FLS: 12, 64, 72.
    b.	ULS: 13, 16, 61, (Seismic cases if needed).


-----


# 5.	Integrated Load Analysis (ILA):
    a.	Model update: FOU model is build based on structural geometry, soil condition, and interface load. These are inter-connected, and thus they are updated simultaneously as the design iteration progresses. 
    b.	Wave generation. 
    c.	Soil spring modelling. 
    d.	Natural frequency analysis (NFA).
    e.	Superelement generation at the tower(TWR)-FOU interface and wave load generation. These feed to the WTG supplier. 
    f.	[Externally done] WTG supplier runs “external” ILA. 
    g.	Receive updated interface load from the WTG supplier. 


-----


# 6.	Structural design check (Code check): 
    a.	Ultimate Limit State (ULS): 
        i.	MP: buckling, bending/axial.
        ii.	JKT: member axial/bending, joint utilization.
    b.	Fatigue Limit State (FLS): 
        i.	MP: Circumferential welds at can transitions, TP flange.
        ii.	JKT: welded tubular joint.
    c.	Serviceability Limit State (SLS): 
        i.	Deflection and rotation limit. 
    d.	Accidental Limit State (ALS): 
        i.	Ship impact.


-----


# 7.	Geotechnical design check
    a.	Pile design 
        i.	MP: Determining the embedment length.
        ii.	JKT: Axial capacity check.
    b.	Pile Drivability Analysis (PDA): fatigue during driving. 


----


# 8.	Connection check 
    a.	Transition piece (TP) to MP: bolted flange, grouted connection. 
    b.	JKT connection: leg-to-pile.


## ** Repeat the above process until design converges. In practice, this iteration corresponds to Concept, FEED, and Detailed design. Each iteration, scope for each discipline expands and uncertainties decrease. The following design processes are also inter-linked but are not necessary repeated every iteration. 


-----


# 9.	Scour and seabed mobility 
    a.	Scour: assess scour depth for each WTG location. Design scour protection if needed. 
    b.	Seabed mobility: assess min/max seabed elevation change. Its impact on JKT pile stick-up is assessed. 


-----


# 10.	Transportation and installation (T&I): 
    a.	Assess loads induced by T&I activities including storage, transport, lifting, upending.


-----


# 11.	Secondary structure design:
    a.	Design working area and access system: external platform, laydown area, Davit crane, boat landing, access ladder, rest platform.
    b.	Design internal layout: flange access platform, internal working platform, cable hang-off platform, and airtight platform (for MP). 
    c.	Define railing and grating.
    d.	Define material used and consider Health, Safety, and Environment (HSE) requirement. 


-----


# 12.	Electrical design: 
    a.	Design low voltage (LV) panel and power distribution. 
    b.	Define and layout electrical devices on external platform. 
    c.	Internal and external light analysis. 
    d.	Design LV cable routing and high voltage (LV) cable support system. 


-----

# 13.	Corrosion protection: 
coating spec, cathodic protection design, corrosion allowance.
