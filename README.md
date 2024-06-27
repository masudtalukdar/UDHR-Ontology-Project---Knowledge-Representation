# UDHR-Ontology_2.0-Project---Knowledge-Representation

## Title: Basic legal concepts in the UDHR


## Overview

This project, known as the UDHR Ontology Project, contains an ontology designed to model various entities and their relationships within the domain of human rights as outlined in the Universal Declaration of Human Rights (UDHR). The ontology is represented in OWL (Web Ontology Language) and includes classes, properties, and individuals pertinent to this domain. It aims to create a structured representation of the basic legal concepts in the UDHR, facilitating better understanding, sharing, and interoperability of human rights concepts across various platforms and systems.

## Files

- **UDHR_Ontology.rdf**: RDF serialization of the UDHR ontology, including classes, subclasses, object properties, data properties, and individuals.
- **UDHR_Ontology.owl**: OWL serialization of the UDHR ontology, providing a formal representation of the legal concepts in OWL 2.0.

## Visualization

The `Radial_Ontology and Tree- Horizontal_Ontology` provides a visual representation of the ontology, illustrating the classes and their interrelationships. This diagram can help users understand the structure and the various connections between different elements.

## Structure

The ontology is organized into the following main classes, each with multiple levels of subclasses to capture the detailed aspects of human rights:

1. **HumanRights**
   - **CivilRights**
     - RightToLife
       - ProtectionAgainstArbitraryKilling
       - RightToSecurity
     - FreedomOfSpeech
       - FreedomOfPress
       - FreedomOfExpression
     - RightToPrivacy
       - ProtectionAgainstSurveillance
       - RightToPersonalDataProtection
     - RightToFairTrial
       - RightToLegalRepresentation
       - PresumptionOfInnocence
   - **PoliticalRights**
     - RightToVote
       - UniversalSuffrage
       - FreeAndFairElections
     - RightToPeacefulAssembly
       - RightToProtest
       - RightToPublicGatherings
     - FreedomOfAssociation
       - RightToFormTradeUnions
       - RightToPoliticalParties
     - RightToPoliticalParticipation
       - RightToStandForElection
       - RightToParticipateInGovernment
   - **EconomicRights**
     - RightToWork
       - RightToFairWages
       - RightToSafeWorkingConditions
     - RightToOwnProperty
       - RightToPersonalProperty
       - RightToIntellectualProperty
     - RightToSocialSecurity
       - RightToPension
       - RightToDisabilityBenefits
     - RightToJustAndFavorableConditionsOfWork
       - RightToEqualPayForEqualWork
       - RightToRestAndLeisure
   - **SocialRights**
     - RightToEducation
       - RightToPrimaryEducation
       - RightToSecondaryEducation
     - RightToHealthcare
       - RightToMedicalCare
       - RightToPreventiveHealthcare
     - RightToHousing
       - RightToAdequateHousing
       - ProtectionAgainstForcedEviction
     - RightToFamilyLife
       - RightToMarry
       - RightToParentalLeave
   - **CulturalRights**
     - RightToParticipateInCulturalLife
       - RightToAccessCulturalHeritage
       - RightToCulturalDiversity
     - RightToBenefitFromScience
       - RightToScientificAdvancements
       - RightToAccessScientificKnowledge
     - RightToCulturalIdentity
       - RightToSpeakMotherTongue
       - RightToCulturalPractices
     - RightToIntellectualProperty
       - RightToCopyright
       - RightToPatent
   - **EnvironmentalRights**
     - RightToCleanEnvironment
       - RightToCleanAir
       - RightToCleanWater
     - RightToSustainableDevelopment
       - RightToParticipateInEnvironmentalDecisionMaking
       - RightToInformationOnEnvironmentalMatters
     - RightToProtectionFromEnvironmentalHazards
       - RightToCompensationForEnvironmentalDamage
       - RightToProtectionFromToxicSubstances

## Properties

### Object Properties

- **isProtectedBy**: Links a right to the legal documents or entities that protect it.
- **isViolatedBy**: Links a right to instances of its violation.
- **isPromotedBy**: Links a right to organizations or entities promoting it.
- **isEnforcedBy**: Links a right to authorities responsible for enforcement.
- **isRecognizedBy**: Links a right to countries or regions recognizing it.
- **isPartOf**: Links a component right to a broader right.
- **hasComponent**: Links a broader right to its component rights.

### Data Properties

- **description**: A textual description of the right.
- **articleNumber**: The specific article number in the UDHR.
- **origin**: Historical context or origin of the right.
- **examples**: Real-world examples or cases illustrating the right.
- **legalDocuments**: References to specific legal documents that protect or define the right.
- **dateAdopted**: The date when the right was adopted in the UDHR.
- **relatedCases**: Related legal cases or instances.

## Individuals

The ontology includes specific instances to illustrate the rights:

- **Article1**: Instance of HumanRights with articleNumber = 1, description = "All human beings are born free and equal in dignity and rights."
- **FreedomOfSpeechInstance**: Instance of FreedomOfSpeech with description, articleNumber, origin, examples, and legalDocuments.
- **RightToEducationInstance**: Instance of RightToEducation with description, articleNumber, origin, examples, and legalDocuments.
- **RightToLifeInstance**: Instance of RightToLife with description, articleNumber, origin, examples, and legalDocuments.
- **RightToFairTrialInstance**: Instance of RightToFairTrial with description, articleNumber, origin, examples, and legalDocuments.
- **RightToVoteInstance**: Instance of RightToVote with description, articleNumber, origin, examples, and legalDocuments.
- **RightToWorkInstance**: Instance of RightToWork with description, articleNumber, origin, examples, and legalDocuments.
- **RightToOwnPropertyInstance**: Instance of RightToOwnProperty with description, articleNumber, origin, examples, and legalDocuments.
- **RightToHealthcareInstance**: Instance of RightToHealthcare with description, articleNumber, origin, examples, and legalDocuments.
- **RightToParticipateInCulturalLifeInstance**: Instance of RightToParticipateInCulturalLife with description, articleNumber, origin, examples, and legalDocuments.
- **RightToCleanEnvironmentInstance**: Instance of RightToCleanEnvironment with description, articleNumber, origin, examples, and legalDocuments.

## Usage

This ontology can be used in semantic web applications, legal information systems, educational tools, and human rights advocacy platforms to enable structured representation and reasoning over human rights concepts.

To load and explore the ontology, you can use various tools and libraries, such as:

- **Protege**: A free, open-source ontology editor and framework for building intelligent systems.
- **Owlready2**: A Python module for ontology-oriented programming. (Note: Ensure you have this library installed in your environment.)

### Example Code (Using Owlready2)

```python
from owlready2 import *

# Load the ontology
onto = get_ontology("path_to/UDHR_Ontology_2.0.owl").load()

# Explore classes
for cls in onto.classes():
    print(cls.name)

# Explore properties
for prop in onto.properties():
    print(prop.name)

# Explore individuals
for ind in onto.individuals():
    print(ind.name)
```


## Acknowledgments

This project was developed as part of the Knowledge Representation course at the University of Verona - Italy, based on guidelines provided by the course instructor, Prof. [Matteo Cristani](https://www.di.univr.it/?ent=persona&id=62&lang=en#tab-didattica).

