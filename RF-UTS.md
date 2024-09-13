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
- What is subject's normal RF pattern of life?
  
```mermaid
flowchart TD
    A(Entity):::BFO <--> |is a| B(Continuant)

	    B(Continuant):::BFO <--> D(Generically Dependant<br />Continuant):::BFO
	    B(Continuant):::BFO <--> E(Independant<br />Continuant):::BFO
		    E(Independant<br />Continuant):::BFO <--> F(material<br />entity):::BFO
		 	   F(Independant<br />Continuant):::BFO <--> G(object):::BFO
		    	   F(Independant<br />Continuant):::BFO <--> H(fiat object<br />part):::BFO
			   F(Independant<br />Continuant):::BFO <--> I(object<br />aggregate):::BFO
		    E(Independant<br />Continuant):::BFO <--> J(immaterial<br />entity):::BFO
		    	J <--> K(site):::BFO
		    		K<--> UD(sensor location)
		    	J <--> L(continuant<br />fiat boundary):::BFO
		    		L <--> M(fiat point<br />boundary):::BFO
		    		L <--> N(fiat line<br />boundary):::BFO
		    		L <--> O(fiat surface<br />boundary):::BFO
		    	J <--> P(spatial<br />region):::BFO
		    		P <--> Q(0D spatial<br />region):::BFO
		    		P <--> R(1D spatial<br />region):::BFO
		    			R <--> UF(position)
		    		P <--> S(2D spatial<br />region):::BFO
		    		P <--> T(3D spatial<br />region):::BFO	    		
	    B(Continuant):::BFO <--> U(Specifically Dependant<br />Continuant):::BFO
	    	U <--> V(quality):::BFO
	    		V <--> W(relational<br />quality):::BFO
				W <--> UE(signal properties)
					UE <--> [frequency]
					UE <--> [power]
					UE <--> [gain]
					UE <--> [protocol]
					UE <--> [duty cycle]
	    	U <--> X(realizable<br />entity):::BFO
	    		X <--> Y(role):::BFO
	    			Y <--> UA(signal)
	    		X <--> Z(disposition):::BFO
	    			Z <--> C(function):::BFO
	    				C <--> UB(communication)
	    			
	    			
    A(Entity) <--> |is a| AA(Occurrent):::BFO
	    AA(occurrent):::BFO <--> AB(process):::BFO
	    	AB <--> AC(history):::BFO
	    AA(occurrent):::BFO <--> AD(process<br />boundary):::BFO
	    AA(occurrent):::BFO <--> AE(temporal<br />region):::BFO
	    	AE <--> AF(0D temporal<br /> region):::BFO
	    		AF <--> AG(temporal<br />instant):::BFO
   		AE <--> AH(1D temporal<br /> region):::BFO
   			AH <--> AI(temporal<br />interval):::BFO
   				AI <--> UC(transmission<br />duration)
	    AA(occurrent):::BFO <--> AJ(spatiotemporal<br />region):::BFO
	      
  classDef BFO fill:#F4AD27,color:#000

