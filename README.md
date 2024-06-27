# UDHR-Ontology_2.0-Project---Knowledge-Representation


## Overview

The UDHR Ontology Project aims to create a structured representation of the basic legal concepts outlined in the Universal Declaration of Human Rights (UDHR). This ontology facilitates a better understanding, sharing, and interoperability of human rights concepts across various platforms and systems.

## Files

- **UDHR_Ontology.rdf**: RDF serialization of the UDHR ontology, including classes, subclasses, object properties, data properties, and individuals.
- **UDHR_Ontology.owl**: OWL serialization of the UDHR ontology, providing a formal representation of the legal concepts in OWL 2.0.

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

## Acknowledgments

This project was developed as part of the Knowledge Representation course at the University of Verona - Italy, based on guidelines provided by the course instructor.

