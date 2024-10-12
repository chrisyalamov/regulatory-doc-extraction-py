# Regulatory Document Data Extraction 

> [!NOTE]
> This project was done as part of a recruitment coding exercise.

This program extracts data from two tables in a regulatory document (.pdf) by the Thai FDA, containing various conditions for manufacture, distribution and importation of specially-controlled substances (cosmetics category).

The tables span multiple pages and contain inconsistencies in the way data is formatted or represented.

## Table 1

This table seems to set maximum levels for ‘specially controlled substances’ when used in particular types of cosmetic products. The same substance may be regulated differently in a different product category.
For example:

|   Type                  |   Specially-controlled substances  |   Maximum Lvel/allowed  |
|-------------------------|------------------------------------|-------------------------|
|   10. Mouthwash         |   formaldehyde                     |   - not more than 0.1%  |
|   …                     |                                    |                         |
|   14. Manicure product  |   formaldehyde                     |   - not more than 5.0%  |

There is a **many-to-many** relationship between substances and types, associated by the “Maximum Lvel/allowed.”

## Table 2

This table seems to set out rules for distribution in two different ways:
- **“Conditions”** and relevant **“Notification to a Minister of Public Health”** for distribution of particular categories of cosmetic products, e.g.:
  | Type                | ... | Condition                                                                                                      | Notification of Minister of Public Health |
  |---------------------|-----|----------------------------------------------------------------------------------------------------------------|-------------------------------------------|
  | 1. Sanitary Napkins | ... | - Those for external use must made cleanly and hygienically<br />  - Those for internal use must be sterilized | (No. 10) B.E. 2536                        |
- “Conditions” and relevant “Notification to a Minister of Public Health” for specially controlled substances, applicable at particular maximum concentrations, e.g.:
  | Type                                                   | Controlled substance | Volume Not exceed    | Condition                                              | Notification of Minister of Public Health     |
  |--------------------------------------------------------|----------------------|----------------------|--------------------------------------------------------|-----------------------------------------------|
  | 6. Hair Product that contain anti- dandruff substances | 1. Zinc Pyrithione   | 2.0%<br/>0.5%        | Use in rinse-off products<br/>Use in leave-on products | (No. 19) B.E. 2537<br/>(No. 19) B.E. 2537     |

