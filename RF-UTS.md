# RF UTS design draft
## Pattern Description:
A model of modern rf persona entities and attributes
#### Material Entities
- car
- phone
- wearable tech
- service radio
- wallet contents
- inventory rfid
- implants
- medical devices
#### Material Entities' Qualities
- frequency
- power
- gain
- protocol
- duty cycle
#### Processes
- interface with devices
- interface with user
- charge/discharge
#### Realizable Entities (Properties that underwrite what the material entities can do)
- rf transmitter(s)
- power system
#### Generically Dependant Continuants (Info used to discuss 1-4)
- size
- weight
- signal properties
- processing capability
## Competency Questions
- Is subject being followed?
- What is subject transmitting?
- What is subject's normal RF pattern of life (POL)?
- Do collections indicate RF POL deviations?
 ```mermaid

graph LR
    A(Entity):::BFO --> |is a| B(Continuant)
    B(Continuant):::BFO --> D(Specifically Dependent<br /> Continuant)
    B(Continuant) --> E(Generically Dependent<br /> Continuant):::BFO
    B(Continuant) --> F(Independent<br /> Continuant)
    F(Independent<br /> Continuant):::BFO --> G(Material Entity)
    F(Independent<br /> Continuant) --> H(Immaterial<br /> Entity)
    D(Specifically Dependent<br /> Continuant):::BFO --> I(Quality)
    D(Specifically Dependent<br /> Continuant) --> J(Realizable<br /> Entity):::BFO
    I(Quality):::BFO --> K(Relational<br /> Quality):::BFO
    J(Realizable<br /> Entity):::BFO --> L(Role):::BFO
    J(Realizable<br /> Entity) --> M(Disposition):::BFO
    M(Disposition) --> N(Function):::BFO
    H(Immaterial<br /> Entity):::BFO --> O(Site):::BFO
    H(Immaterial<br /> Entity) --> P(Spatial<br /> Region):::BFO
    H(Immaterial<br /> Entity) --> Q(Continuant Fiat<br /> Boundary):::BFO
    Q(Continuant Fiat<br /> Boundary):::BFO --> R(Fiat<br /> Point):::BFO
    Q(Continuant Fiat<br /> Boundary) --> S(Fiat<br /> Surface):::BFO
    Q(Continuant Fiat<br /> Boundary) --> T(Fiat<br /> Line):::BFO
    P(Spatial<br /> Region):::BFO --> VD(Zero-Dimensional<br /> Spatial Region):::BFO
    P(Spatial<br /> Region):::BFO --> U(One-Dimensional<br /> Spatial Region):::BFO
    P(Spatial<br /> Region):::BFO --> V(Two-Dimensional<br /> Spatial Region):::BFO
    P(Spatial<br /> Region):::BFO --> W(Three-Dimensional<br /> Spatial Region):::BFO
    G(Material<br /> Entity):::BFO --> X(Fiat Object Part):::BFO
    G(Material<br /> Entity):::BFO --> Y(Object<br /> Aggregate):::BFO
    G(Material<br /> Entity):::BFO --> Z(Object):::BFO
    A(Entity):::BFO --> |is a| C(Occurrent):::BFO
    C(Occurrent):::BFO --> AA(Process):::BFO
    C(Occurrent) --> AB(Process<br /> Boundary):::BFO
    C(Occurrent) --> AC(Temporal<br /> Region):::BFO
    C(Occurrent) --> AD(Spatiotemporal<br /> Region):::BFO
    AA(Process):::BFO --> AE(History):::BFO
    AC(Temporal<br /> Region):::BFO --> AF(Zero-Dimensional<br /> Temporal Region):::BFO
    AC(Temporal<br /> Region) --> AI(One-Dimensional<br /> Temporal Region):::BFO
    AF(Zero-Dimensional<br /> Temporal Region):::BFO --> AG(Temporal<br /> Instant):::BFO
    AI(One-Dimensional<br /> Temporal Region):::BFO --> AH(Temporal<br /> Interval):::BFO
    	
    	E --> EA[size]
    	E --> EB[weight]
    	E --> EC[signal<br /> properties]
    	E --> ED[processing<br />capabilities]
    	
    	G --> GV[vehicle]
	G --> GP[phone]
	G --> GW[wearable tech]
	G --> G2[2way radio]
	G --> GC[wallet content]
	G --> RF[inventory rfid]
	G --> GI[implants]
	G --> GM[medical devices]
    	
    	J(Realizable<br />Entity) --> JA[rf transceivers]
    	J --> JB[power system]
	J --> JC[signal]
    	
	K(Relational<br /> Quality) <--> UE(signal properties)
		UE <--> UEA[frequency]
		UE <--> UEB[power]
		
		UE <--> UED[protocol]
		UE <--> UEF[duty cycle]
		


	AA(Process) --> AAC[interface with<br /> human]
	AA(Process) --> AAB[interface with<br /> devices]
	AA(Process) --> AAD[charge/<br /> discharge]
	
	
	N(Function) <--> NA[communication]
	        
	AF(0D Temporal Region) --> AFA[transmission<br />duration]
	AF(0D Temporal Region) --> AFB[reception<br />duration]


    classDef BFO fill:#F5AD27,color:#060606
