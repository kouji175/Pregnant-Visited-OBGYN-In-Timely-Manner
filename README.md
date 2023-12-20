# Pregnant-Visited-OBGYN-In-Timely-Manner

# Question

**The percentage of pregnant females who visited OBGYN provider in a timely manner?**

## Eligible Population

- **Ages:** >= 18 
- **Visiting Provider Specialty:** OBGYN
- **Pregnancy Status:** Must either have a due date populated on an encounter or an encounter with a pregnancy diagnosis.

## Administrative Specification

### Denominator

- The eligible population

### Numerator

- The number of patients with a completed visit to the OBGYN between 40 and 27 weeks prior to delivery. Pregnant member identified solely by diagnoses should have an encounter within 6 weeks of diagnosis.

## Data Dictionary

### Provider

This table contains 50 provider information.

- **Prov_id:** Provider ID 
- **Prov_name:** Provider Name
- **Prov_loc_id:** Providers location id
- **Prov_specialty:** Provider’s Specialty 

### Locations

This table contains location information for patients’ visit and providers’ location

- **Loc_id:** Location ID
- **Loc_name:** Location Name
- **Sa_name:** Service Area Name

### Patient

This table contains patient information

- **Unique_Patient_id:** Patient unique ID 
- **Gender_c:** Patient’s Gender (“M”, “F”) 
- **Birth_date:** Patients’ Birthdate 
- **Pat_loc_id:** The patient’s primary location 

### Pcp

This table contains patient’s primary care provider information

- **Unique_Patient_id:** Patient ID 
- **Pcp_prov_id:** Primary care provider id 

### Encounters

This table contains encounter information

- **Enc_id:** Encounter ID for every encounter visit 
- **Enc_Patient_id:** Patient ID associated with the encounter 
- **Visit_prov_id:** Provider id for encounter
- **Enc_Status_c:** Status of the encounter (“Completed”, “Cancelled”)
- **Enc_date:** Date associated with the visit 
- **Due_Date:** Recorded due date for pregnant patients

### Encounter_dx

This table contains diagnosis information related to the encounter

- **Enc_id:** Unique Encounter ID
- **Line:** The line number for the diagnosis associated with this record. Multiple pieces of diagnosis can be associated with this record. 
- **Icd_code:** ICD 10 diagnosis code regarding to the diagnosis 

### Pregnancy_Diagnosis

This table contains diagnosis information for identifying pregnancy diagnosis

- **Code:** Diagnosis code for pregnancy diagnosis
